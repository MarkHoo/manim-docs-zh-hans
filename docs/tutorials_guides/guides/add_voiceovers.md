# 为视频添加旁白

创建带有画外音的完整视频比创建纯粹的视觉 Manim 场景要复杂一些。 在视频渲染后，必须使用[视频编辑程序添加画外音。](https://en.wikipedia.org/wiki/List_of_video_editing_software)这个过程可能很困难且耗时，因为它需要大量的计划和准备。

为了简化向视频添加画外音的过程，我们创建了 [Manim Voiceover](https://voiceover.manim.community)，这是一个插件，可让您直接在 Python 中向场景添加画外音。要安装它，请运行

```sh
pip install "manim-voiceover[azure,gtts]"
```

请访问[安装页面，](https://voiceover.manim.community/en/latest/installation.html) 了解有关如何安装 Manim Voiceover 的更多详细信息。

## 基本用法

Manim配音让您...

- 直接在 Python 中向 Manim 视频添加配音，无需使用视频编辑器。
- 通过简单的命令行界面在渲染过程中使用麦克风录制配音。
- 使用来自各种免费和专有服务的自动生成的 AI 语音来开发动画。

它提供了一个非常简单的 API，可让您指定配音脚本，然后在渲染期间录制它：

```py
from manim import *
from manim_voiceover import VoiceoverScene
from manim_voiceover.services.recorder import RecorderService

# Simply inherit from VoiceoverScene instead of Scene to get all the
# voiceover functionality.
class RecorderExample(VoiceoverScene):
    def construct(self):
        # You can choose from a multitude of TTS services,
        # or in this example, record your own voice:
        self.set_speech_service(RecorderService())

        circle = Circle()

        # Surround animation sections with with-statements:
        with self.voiceover(text="This circle is drawn as I speak.") as tracker:
            self.play(Create(circle), run_time=tracker.duration)
            # The duration of the animation is received from the audio file
            # and passed to the tracker automatically.

        # This part will not start playing until the previous voiceover is finished.
        with self.voiceover(text="Let's shift it to the left 2 units.") as tracker:
            self.play(circle.animate.shift(2 * LEFT), run_time=tracker.duration)
```

要开始使用 Manim Voiceover，请访问[快速入门指南](https://voiceover.manim.community/en/latest/quickstart.html)。

访问[示例库](https://voiceover.manim.community/en/latest/examples.html) 以查看 Manim Voiceover 的一些实际示例。
