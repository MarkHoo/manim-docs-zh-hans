

Configuration[#](#configuration "Permalink to this heading")
============================================================

Manim provides an extensive configuration system that allows it to adapt to many different use cases. There are many configuration options that can be configured at different times during the scene rendering process. Each option can be configured programmatically via [the ManimConfig class](#the-manimconfig-class), at the time of command invocation via [command-line arguments](#command-line-arguments), or at the time the library is first imported via [the config files](#the-config-files).

The most common, simplest, and recommended way to configure Manim is via the command-line interface (CLI), which is described directly below.

Command-line arguments[#](#command-line-arguments "Permalink to this heading")
------------------------------------------------------------------------------

By far the most commonly used command in the CLI is the `render` command, which is used to render scene(s) to an output file. It is used with the following arguments:

Manim Community v0.16.0.post0

Usage: manim render \[OPTIONS\] FILE \[SCENE_NAMES\]...

  Render SCENE(S) from the input FILE.

  FILE is the file path of the script or a config file.

  SCENES is an optional list of scenes in the file.
...

Copy to clipboard

However, since Manim defaults to the `render` command whenever no command is specified, the following form is far more common and can be used instead:

manim \[OPTIONS\] FILE \[SCENES\]

Copy to clipboard

An example of using the above form is:

manim -qm file.py SceneOne

Copy to clipboard

This asks Manim to search for a Scene class called `SceneOne` inside the file `file.py` and render it with medium quality (specified by the `-qm` flag).

Another frequently used flag is `-p` (“preview”), which makes manim open the rendered video after it’s done rendering.

Note

The `-p` flag does not change any properties of the global `config` dict. The `-p` flag is only a command-line convenience.

### Advanced examples[#](#advanced-examples "Permalink to this heading")

To render a scene in high quality, but only output the last frame of the scene instead of the whole video, you can execute

manim -sqh <file.py> SceneName

Copy to clipboard

The following example specifies the output file name (with the `-o` flag), renders only the first ten animations (`-n` flag) with a white background (`-c` flag), and saves the animation as a `.gif` instead of as a `.mp4` file (`--format=gif` flag). It uses the default quality and does not try to open the file after it is rendered.

manim -o myscene --format=gif -n 0,10 -c WHITE <file.py> SceneName

Copy to clipboard

### A list of all CLI flags[#](#a-list-of-all-cli-flags "Permalink to this heading")

$ manim --help
Manim Community v0.16.0.post0

Usage: manim \[OPTIONS\] COMMAND \[ARGS\]...

  Animation engine for explanatory math videos.

Options:
  --version  Show version and exit.
  --help     Show this message and exit.

Commands:
  cfg      Manages Manim configuration files.
  init     Create a new project or insert a new scene.
  new      (Deprecated) Create a new project or insert a new scene.
  plugins  Manages Manim plugins.
  render   Render SCENE(S) from the input FILE.

See 'manim <command>' to read about a specific subcommand.

Note: the subcommand 'manim render' is called if no other subcommand is
specified. Run 'manim render --help' if you would like to know what the '-ql' or
'-p' flags do, for example.

Made with <3 by Manim Community developers.

Copy to clipboard

$ manim render --help
Manim Community v0.16.0.post0

Usage: manim render \[OPTIONS\] FILE \[SCENE_NAMES\]...

  Render SCENE(S) from the input FILE.

  FILE is the file path of the script or a config file.

  SCENES is an optional list of scenes in the file.

Global options:
  -c, --config_file TEXT         Specify the configuration file to use for
                                 render settings.
  --custom\_folders               Use the folders defined in the \[custom\_folders\]
                                 section of the config file to define the output
                                 folder structure.
  --disable_caching              Disable the use of the cache (still generates
                                 cache files).
  --flush_cache                  Remove cached partial movie files.
  --tex_template TEXT            Specify a custom TeX template file.
  -v, --verbosity \[DEBUG|INFO|WARNING|ERROR|CRITICAL\]
                                 Verbosity of CLI output. Changes ffmpeg log
                                 level unless 5+.
  --notify\_outdated\_version / --silent
                                 Display warnings for outdated installation.
  --enable_gui                   Enable GUI interaction.
  --gui_location TEXT            Starting location for the GUI.
  --fullscreen                   Expand the window to its maximum possible size.
  --enable_wireframe             Enable wireframe debugging mode in opengl.
  --force_window                 Force window to open when using the opengl
                                 renderer, intended for debugging as it may
                                 impact performance
  --dry_run                      Renders animations without outputting image or
                                 video files and disables the window

Output options:
  -o, --output_file TEXT         Specify the filename(s) of the rendered
                                 scene(s).
  -0, --zero_pad INTEGER RANGE   Zero padding for PNG file names.  \[0<=x<=9\]
  --write\_to\_movie               Write the video rendered with opengl to a file.
  --media_dir PATH               Path to store rendered videos and latex.
  --log_dir PATH                 Path to store render logs.
  --log\_to\_file                  Log terminal output to file.

Render Options:
  -n, --from\_animation\_number TEXT
                                 Start rendering from n\_0 until n\_1. If n_1 is
                                 left unspecified, renders all scenes after n_0.
  -a, --write_all                Render all scenes in the input file.
  --format \[png|gif|mp4|webm|mov\]
  -s, --save\_last\_frame
  -q, --quality \[l|m|h|p|k\]      Render quality at the follow resolution
                                 framerates, respectively: 854x480 15FPS,
                                 1280x720 30FPS, 1920x1080 60FPS, 2560x1440
                                 60FPS, 3840x2160 60FPS
  -r, --resolution TEXT          Resolution in (W,H) for when 16:9 aspect ratio
                                 isn't possible.
  --fps, --frame_rate FLOAT      Render at this frame rate.
  --renderer \[cairo|opengl\]      Select a renderer for your Scene.
  --use\_opengl\_renderer          Render scenes using OpenGL (Deprecated).
  -g, --save_pngs                Save each frame as png (Deprecated).
  -i, --save\_as\_gif              Save as a gif (Deprecated).
  --save_sections                Save section videos in addition to movie file.
  -s, --save\_last\_frame          Save last frame as png (Deprecated).
  -t, --transparent              Render scenes with alpha channel.
  --use\_projection\_fill_shaders  Use shaders for OpenGLVMobject fill which are
                                 compatible with transformation matrices.
  --use\_projection\_stroke_shaders
                                 Use shaders for OpenGLVMobject stroke which are
                                 compatible with transformation matrices.

Ease of access options:
  --progress_bar \[display|leave|none\]
                                 Display progress bars and/or keep them
                                 displayed.
  -p, --preview                  Preview the Scene's animation. OpenGL does a
                                 live preview in a popup window. Cairo opens the
                                 rendered video file in the system default media
                                 player.
  -f, --show\_in\_file_browser     Show the output file in the file browser.
  --jupyter                      Using jupyter notebook magic.

Other options:
  --help                         Show this message and exit.

Made with <3 by Manim Community developers.

Copy to clipboard

$ manim cfg --help
Manim Community v0.16.0.post0

Usage: manim cfg \[OPTIONS\] COMMAND \[ARGS\]...

  Manages Manim configuration files.

Options:
  --help  Show this message and exit.

Commands:
  export
  show
  write

Made with <3 by Manim Community developers.

Copy to clipboard

$ manim plugins --help
Manim Community v0.16.0.post0

Usage: manim plugins \[OPTIONS\]

  Manages Manim plugins.

Options:
  -l, --list  List available plugins.
  --help      Show this message and exit.

Made with <3 by Manim Community developers.

Copy to clipboard

The ManimConfig class[#](#the-manimconfig-class "Permalink to this heading")
----------------------------------------------------------------------------

The most direct way of configuring Manim is through the global `config` object, which is an instance of [`ManimConfig`](../reference/manim._config.utils.ManimConfig.html#manim._config.utils.ManimConfig "manim._config.utils.ManimConfig"). Each property of this class is a config option that can be accessed either with standard attribute syntax or with dict-like syntax:

>>\> from manim import *
>>\> config.background_color = WHITE
>>\> config\["background_color"\] = WHITE

Copy to clipboard

Note

The former is preferred; the latter is provided for backwards compatibility.

Most classes, including [`Camera`](../reference/manim.camera.camera.Camera.html#manim.camera.camera.Camera "manim.camera.camera.Camera"), [`Mobject`](../reference/manim.mobject.mobject.Mobject.html#manim.mobject.mobject.Mobject "manim.mobject.mobject.Mobject"), and [`Animation`](../reference/manim.animation.animation.Animation.html#manim.animation.animation.Animation "manim.animation.animation.Animation"), read some of their default configuration from the global `config`.

>>\> Camera({}).background_color
<Color white>
>>\> config.background_color = RED  \# 0xfc6255
>>\> Camera({}).background_color
<Color #fc6255>

Copy to clipboard

[`ManimConfig`](../reference/manim._config.utils.ManimConfig.html#manim._config.utils.ManimConfig "manim._config.utils.ManimConfig") is designed to keep internal consistency. For example, setting `frame_y_radius` will affect `frame_height`:

>>\> config.frame_height
8.0
>>\> config.frame\_y\_radius = 5.0
>>\> config.frame_height
10.0

Copy to clipboard

The global `config` object is meant to be the single source of truth for all config options. All of the other ways of setting config options ultimately change the values of the global `config` object.

The following example illustrates the video resolution chosen for examples rendered in our documentation with a reference frame.

Example: ShowScreenResolution [¶](#showscreenresolution)

![../_images/ShowScreenResolution-1.png](../_images/ShowScreenResolution-1.png)

from manim import *

class ShowScreenResolution(Scene):
    def construct(self):
        pixel_height = config\["pixel_height"\]  \#  1080 is default
        pixel_width = config\["pixel_width"\]  \# 1920 is default
        frame_width = config\["frame_width"\]
        frame_height = config\["frame_height"\]
        self.add(Dot())
        d1 = Line(frame_width * LEFT / 2, frame_width * RIGHT / 2).to_edge(DOWN)
        self.add(d1)
        self.add(Text(str(pixel_width)).next_to(d1, UP))
        d2 = Line(frame_height * UP / 2, frame_height * DOWN / 2).to_edge(LEFT)
        self.add(d2)
        self.add(Text(str(pixel_height)).next_to(d2, RIGHT))

Copy to clipboard

The config files[#](#the-config-files "Permalink to this heading")
------------------------------------------------------------------

As the last example shows, executing Manim from the command line may involve using many flags simultaneously. This may become a nuisance if you must execute the same script many times in a short time period, for example, when making small incremental tweaks to your scene script. For this reason, Manim can also be configured using a configuration file. A configuration file is a file ending with the suffix `.cfg`.

To use a local configuration file when rendering your scene, you must create a file with the name `manim.cfg` in the same directory as your scene code.

Warning

The config file **must** be named `manim.cfg`. Currently, Manim does not support config files with any other name.

The config file must start with the section header `[CLI]`. The configuration options under this header have the same name as the CLI flags and serve the same purpose. Take, for example, the following config file.

\[CLI\]
\# my config file
output_file  =  myscene
save\_as\_gif  =  True
background_color  =  WHITE

Copy to clipboard

Config files are parsed with the standard python library `configparser`. In particular, they will ignore any line that starts with a pound symbol `#`.

Now, executing the following command

manim -o myscene -i -c WHITE <file.py> SceneName

Copy to clipboard

is equivalent to executing the following command, provided that `manim.cfg` is in the same directory as <file.py>,

manim <file.py> SceneName

Copy to clipboard

Tip

The names of the configuration options admissible in config files are exactly the same as the **long names** of the corresponding command- line flags. For example, the `-c` and `--background_color` flags are interchangeable, but the config file only accepts `background_color` as an admissible option.

Since config files are meant to replace CLI flags, all CLI flags can be set via a config file. Moreover, any config option can be set via a config file, whether or not it has an associated CLI flag. See the bottom of this document for a list of all CLI flags and config options.

Manim will look for a `manim.cfg` config file in the same directory as the file being rendered, and **not** in the directory of execution. For example,

manim -o myscene -i -c WHITE <path/to/file.py> SceneName

Copy to clipboard

will use the config file found in `path/to/file.py`, if any. It will **not** use the config file found in the current working directory, even if it exists. In this way, the user may keep different config files for different scenes or projects, and execute them with the right configuration from anywhere in the system.

The file described here is called the **folder-wide** config file because it affects all scene scripts found in the same folder.

### The user config file[#](#the-user-config-file "Permalink to this heading")

As explained in the previous section, a `manim.cfg` config file only affects the scene scripts in its same folder. However, the user may also create a special config file that will apply to all scenes rendered by that user. This is referred to as the **user-wide** config file, and it will apply regardless of where Manim is executed from, and regardless of where the scene script is stored.

The user-wide config file lives in a special folder, depending on the operating system.

*   Windows: `UserDirectory`/AppData/Roaming/Manim/manim.cfg
    
*   MacOS: `UserDirectory`/.config/manim/manim.cfg
    
*   Linux: `UserDirectory`/.config/manim/manim.cfg
    

Here, `UserDirectory` is the user’s home folder.

Note

A user may have many **folder-wide** config files, one per folder, but only one **user-wide** config file. Different users in the same computer may each have their own user-wide config file.

Warning

Do not store scene scripts in the same folder as the user-wide config file. In this case, the behavior is undefined.

Whenever you use Manim from anywhere in the system, Manim will look for a user-wide config file and read its configuration.

### Cascading config files[#](#cascading-config-files "Permalink to this heading")

What happens if you execute Manim and it finds both a folder-wide config file and a user-wide config file? Manim will read both files, but if they are incompatible, **the folder-wide file takes precedence**.

For example, take the following user-wide config file

\# user-wide
\[CLI\]
output_file  =  myscene
save\_as\_gif  =  True
background_color  =  WHITE

Copy to clipboard

and the following folder-wide file

\# folder-wide
\[CLI\]
save\_as\_gif  =  False

Copy to clipboard

Then, executing `manim <file.py> SceneName` will be equivalent to not using any config files and executing

manim -o myscene -c WHITE <file.py> SceneName

Copy to clipboard

Any command-line flags have precedence over any config file. For example, using the previous two config files and executing `manim -c RED <file.py> SceneName` is equivalent to not using any config files and executing

manim -o myscene -c RED <file.py> SceneName

Copy to clipboard

There is also a **library-wide** config file that determines Manim’s default behavior and applies to every user of the library. It has the least precedence, so any config options in the user-wide and any folder-wide files will override the library-wide file. This is referred to as the _cascading_ config file system.

Warning

**The user should not try to modify the library-wide file**. Contributors should receive explicit confirmation from the core developer team before modifying it.

Order of operations[#](#order-of-operations "Permalink to this heading")
------------------------------------------------------------------------

Failed to execute 'serializeToString' on 'XMLSerializer': parameter 1 is not of type 'Node'.

With so many different ways of configuring Manim, it can be difficult to know when each config option is being set. In fact, this will depend on how Manim is being used.

If Manim is imported from a module, then the configuration system will follow these steps:

1.  The library-wide config file is loaded.
    
2.  The user-wide and folder-wide files are loaded if they exist.
    
3.  All files found in the previous two steps are parsed in a single `ConfigParser` object, called `parser`. This is where _cascading_ happens.
    
4.  `logging.Logger` is instantiated to create Manim’s global `logger` object. It is configured using the “logger” section of the parser, i.e. `parser['logger']`.
    
5.  `ManimConfig` is instantiated to create the global `config` object.
    
6.  The `parser` from step 3 is fed into the `config` from step 5 via `ManimConfig.digest_parser()`.
    
7.  Both `logger` and `config` are exposed to the user.
    

If Manim is being invoked from the command line, all of the previous steps happen, and are complemented by:

8.  The CLI flags are parsed and fed into `config` via `digest_args()`.
    
9.  If the `--config_file` flag was used, a new `ConfigParser` object is created with the contents of the library-wide file, the user-wide file if it exists, and the file passed via `--config_file`. In this case, the folder-wide file, if it exists, is ignored.
    
10.  The new parser is fed into `config`.
    
11.  The rest of the CLI flags are processed.
    

To summarize, the order of precedence for configuration options, from lowest to highest precedence is:

1.  Library-wide config file,
    
2.  user-wide config file, if it exists,
    
3.  folder-wide config file, if it exists OR custom config file, if passed via `--config_file`,
    
4.  other CLI flags, and
    
5.  any programmatic changes made after the config system is set.
    

A list of all config options[#](#a-list-of-all-config-options "Permalink to this heading")
------------------------------------------------------------------------------------------

\['aspect\_ratio', 'assets\_dir', 'background\_color', 'background\_opacity',
'bottom', 'custom\_folders', 'disable\_caching', 'dry_run',
'ffmpeg\_loglevel', 'flush\_cache', 'frame\_height', 'frame\_rate',
'frame\_size', 'frame\_width', 'frame\_x\_radius', 'frame\_y\_radius',
'from\_animation\_number', \`fullscreen\`, 'images\_dir', 'input\_file', 'left_side',
'log\_dir', 'log\_to\_file', 'max\_files\_cached', 'media\_dir', 'media_width',
'movie\_file\_extension', 'notify\_outdated\_version', 'output\_file', 'partial\_movie_dir',
'pixel\_height', 'pixel\_width', 'plugins', 'preview',
'progress\_bar', 'quality', 'right\_side', 'save\_as\_gif', 'save\_last\_frame',
'save\_pngs', 'scene\_names', 'show\_in\_file\_browser', 'sound', 'tex\_dir',
'tex\_template', 'tex\_template\_file', 'text\_dir', 'top', 'transparent',
'upto\_animation\_number', 'use\_opengl\_renderer', 'verbosity', 'video_dir',
'window\_position', 'window\_monitor', 'window\_size', 'write\_all', 'write\_to\_movie',
'enable\_wireframe', 'force\_window'\]

Copy to clipboard

Accessing CLI command options[#](#accessing-cli-command-options "Permalink to this heading")
--------------------------------------------------------------------------------------------

Entering `manim`, or `manim --help`, will open the main help page.

Usage: manim \[OPTIONS\] COMMAND \[ARGS\]...

  Animation engine for explanatory math videos.

Options:
  --version  Show version and exit.
  --help     Show this message and exit.

Commands:
  cfg      Manages Manim configuration files.
  init     Sets up a new project in current working directory with default
           settings.

           It copies files from templates directory and pastes them in the
           current working dir.
  new      Create a new project or insert a new scene.
  plugins  Manages Manim plugins.
  render   Render SCENE(S) from the input FILE.

See 'manim <command>' to read about a specific subcommand.

Made with <3 by Manim Community developers.

Copy to clipboard

Each of the subcommands has its own help page which can be accessed similarly:

manim render
manim render --help

Copy to clipboard