<section id="animationgroup">
<h1><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">动画组</font></font><a class="headerlink" href="#animationgroup" title="此标题的固定链接"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">#</font></font></a></h1>
<p><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">合格名称：</font></font><code class="docutils literal notranslate"><span class="pre">manim.animation.composition.AnimationGroup</span></code></p>
<dl class="py class">
<dt class="sig sig-object py" id="manim.animation.composition.AnimationGroup">
<em class="property"><span class="pre"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">类</font></font></span><span class="w"> </span></em><span class="sig-name descname"><span class="pre"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">AnimationGroup</font></font></span></span><span class="sig-paren"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;"> ( </font></font></span><em class="sig-param"><span class="n"><span class="pre"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">mobject </font></font></span></span><span class="o"><span class="pre"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">= </font></font></span></span><span class="default_value"><span class="pre"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">None</font></font></span></span></em><font style="vertical-align: inherit;"><font style="vertical-align: inherit;"> ,</font></font><em class="sig-param"><span class="o"><span class="pre"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;"> * </font></font></span></span><span class="n"><span class="pre"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">args</font></font></span></span></em><font style="vertical-align: inherit;"><font style="vertical-align: inherit;"> ,</font></font><em class="sig-param"><span class="n"><span class="pre"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;"> use_override </font></font></span></span><span class="o"><span class="pre"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">= </font></font></span></span><span class="default_value"><span class="pre"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">True</font></font></span></span></em><font style="vertical-align: inherit;"><font style="vertical-align: inherit;"> ,</font></font><em class="sig-param"><span class="o"><span class="pre"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;"> ** </font></font></span></span><span class="n"><span class="pre"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">kwargs</font></font></span></span></em><span class="sig-paren"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;"> )</font></font></span><a class="reference internal" href="../_modules/manim/animation/composition.html#AnimationGroup"><span class="viewcode-link"><span class="pre"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">[来源]</font></font></span></span></a><a class="headerlink" href="#manim.animation.composition.AnimationGroup" title="此定义的固定链接"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">#</font></font></a></dt>
<dd><p><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">基地：</font></font><a class="reference internal" href="manim.animation.animation.Animation.html#manim.animation.animation.Animation" title="manim.animation.animation.Animation"><code class="xref py py-class docutils literal notranslate"><span class="pre">Animation</span></code></a></p>
<p><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">播放一组或一系列的</font></font><a class="reference internal" href="manim.animation.animation.Animation.html#manim.animation.animation.Animation" title="manim.animation.animation.Animation"><code class="xref py py-class docutils literal notranslate"><span class="pre">Animation</span></code></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">.</font></font></p>
<dl class="field-list simple">
<dt class="field-odd"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">参数</font></font></dt>
<dd class="field-odd"><ul class="simple">
<li><p><strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">动画</font></font></strong><font style="vertical-align: inherit;"></font><a class="reference internal" href="manim.animation.animation.Animation.html#manim.animation.animation.Animation" title="manim.animation.animation.Animation"><code class="xref py py-class docutils literal notranslate"><span class="pre">Animation</span></code></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">–要播放的对象</font><font style="vertical-align: inherit;">序列。</font></font></p></li>
<li><p><strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">组</font></font></strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">– 一组多个</font></font><a class="reference internal" href="manim.mobject.mobject.Mobject.html#manim.mobject.mobject.Mobject" title="manim.mobject.mobject.Mobject"><code class="xref py py-class docutils literal notranslate"><span class="pre">Mobject</span></code></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">.</font></font></p></li>
<li><p><strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">run_time</font></font></strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;"> – 动画的持续时间（以秒为单位）。</font></font></p></li>
<li><p><strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">rate_func</font></font></strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;"> – 根据相对运行时间定义动画进度的函数（请参阅</font></font><a class="reference internal" href="manim.utils.rate_functions.html#module-manim.utils.rate_functions" title="manim.utils.rate_functions"><code class="xref py py-mod docutils literal notranslate"><span class="pre">rate_functions</span></code></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">）。</font></font></p></li>
<li><p><strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">滞后比率</font></font></strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">–</font></font></p><p><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">定义动画应用于子对象之前的延迟。</font><font style="vertical-align: inherit;">lag_ratio
</font></font><code class="docutils literal notranslate"><span class="pre">n.nn</span></code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">表示当前动画播放完毕后将播放</font></font><code class="docutils literal notranslate"><span class="pre">nnn%</span></code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">下一个动画。</font><font style="vertical-align: inherit;">默认为 0.0，表示所有动画将一起播放。</font></font></p>
<p><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">这不会影响动画的总运行时间。</font><font style="vertical-align: inherit;">相反，会调整各个动画的运行时间，以便完整的动画具有定义的运行时间。</font></font></p>
<p></p></li>
</ul>
</dd>
</dl>
<p class="rubric"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">方法</font></font></p>
<div class="table-wrapper autosummary longtable docutils container">
<table class="autosummary longtable docutils align-default">
<colgroup>
<col style="width: 10%">
<col style="width: 90%">
</colgroup>
<tbody>
<tr class="row-odd"><td><p><a class="reference internal" href="#manim.animation.composition.AnimationGroup.begin" title="manim.animation.composition.AnimationGroup.begin"><code class="xref py py-obj docutils literal notranslate"><span class="pre">begin</span></code></a></p></td>
<td><p><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">开始动画。</font></font></p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="#manim.animation.composition.AnimationGroup.build_animations_with_timings" title="manim.animation.composition.AnimationGroup.build_animations_with_timings"><code class="xref py py-obj docutils literal notranslate"><span class="pre">build_animations_with_timings</span></code></a></p></td>
<td><p><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">创建 (anim, start_time, end_time) 形式的三元组列表。</font></font></p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="#manim.animation.composition.AnimationGroup.clean_up_from_scene" title="manim.animation.composition.AnimationGroup.clean_up_from_scene"><code class="xref py py-obj docutils literal notranslate"><span class="pre">clean_up_from_scene</span></code></a></p></td>
<td><p><font style="vertical-align: inherit;"></font><a class="reference internal" href="manim.scene.scene.Scene.html#manim.scene.scene.Scene" title="手动场景.场景.场景"><code class="xref py py-class docutils literal notranslate"><span class="pre">Scene</span></code></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">完成动画后</font><font style="vertical-align: inherit;">清理。</font></font></p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="#manim.animation.composition.AnimationGroup.finish" title="manim.animation.composition.AnimationGroup.finish"><code class="xref py py-obj docutils literal notranslate"><span class="pre">finish</span></code></a></p></td>
<td><p><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">完成动画。</font></font></p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="#manim.animation.composition.AnimationGroup.get_all_mobjects" title="manim.animation.composition.AnimationGroup.get_all_mobjects"><code class="xref py py-obj docutils literal notranslate"><span class="pre">get_all_mobjects</span></code></a></p></td>
<td><p><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">获取动画中涉及的所有 mobject。</font></font></p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="#manim.animation.composition.AnimationGroup.init_run_time" title="manim.animation.composition.AnimationGroup.init_run_time"><code class="xref py py-obj docutils literal notranslate"><span class="pre">init_run_time</span></code></a></p></td>
<td><p><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">如果与 不同，则计算动画的运行时间</font></font><code class="docutils literal notranslate"><span class="pre">run_time</span></code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">。</font></font></p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="#manim.animation.composition.AnimationGroup.interpolate" title="manim.animation.composition.AnimationGroup.interpolate"><code class="xref py py-obj docutils literal notranslate"><span class="pre">interpolate</span></code></a></p></td>
<td><p><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">设置动画进度。</font></font></p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="#manim.animation.composition.AnimationGroup.update_mobjects" title="manim.animation.composition.AnimationGroup.update_mobjects"><code class="xref py py-obj docutils literal notranslate"><span class="pre">update_mobjects</span></code></a></p></td>
<td><p><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">更新诸如starting_mobject和（对于变换）target_mobject之类的内容。</font></font></p></td>
</tr>
</tbody>
</table>
</div>
<dl class="py method">
<dt class="sig sig-object py" id="manim.animation.composition.AnimationGroup.begin">
<span class="sig-name descname"><span class="pre"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">开始</font></font></span></span><span class="sig-paren"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">( </font></font></span><span class="sig-paren"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">)</font></font></span><a class="reference internal" href="../_modules/manim/animation/composition.html#AnimationGroup.begin"><span class="viewcode-link"><span class="pre"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">[来源]</font></font></span></span></a><a class="headerlink" href="#manim.animation.composition.AnimationGroup.begin" title="此定义的固定链接"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">#</font></font></a></dt>
<dd><p><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">开始动画。</font></font></p>
<p><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">该方法在动画播放时被调用。</font><font style="vertical-align: inherit;">尽可能多的初始化，尤其是任何 mobject 复制，应该存在于这个方法中。</font></font></p>
<dl class="field-list simple">
<dt class="field-odd"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">返回类型</font></font></dt>
<dd class="field-odd"><p><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">没有任何</font></font></p>
</dd>
</dl>
</dd></dl>

<dl class="py method">
<dt class="sig sig-object py" id="manim.animation.composition.AnimationGroup.build_animations_with_timings">
<span class="sig-name descname"><span class="pre"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">build_animations_with_timings</font></font></span></span><span class="sig-paren"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;"> ( </font></font></span><span class="sig-paren"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">)</font></font></span><a class="reference internal" href="../_modules/manim/animation/composition.html#AnimationGroup.build_animations_with_timings"><span class="viewcode-link"><span class="pre"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">[来源]</font></font></span></span></a><a class="headerlink" href="#manim.animation.composition.AnimationGroup.build_animations_with_timings" title="此定义的固定链接"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">#</font></font></a></dt>
<dd><p><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">创建 (anim, start_time, end_time) 形式的三元组列表。</font></font></p>
<dl class="field-list simple">
<dt class="field-odd"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">返回类型</font></font></dt>
<dd class="field-odd"><p><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">没有任何</font></font></p>
</dd>
</dl>
</dd></dl>

<dl class="py method">
<dt class="sig sig-object py" id="manim.animation.composition.AnimationGroup.clean_up_from_scene">
<span class="sig-name descname"><span class="pre"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">clean_up_from_scene</font></font></span></span><span class="sig-paren"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">（</font></font></span><em class="sig-param"><span class="n"><span class="pre"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">场景</font></font></span></span></em><span class="sig-paren"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">）</font></font></span><a class="reference internal" href="../_modules/manim/animation/composition.html#AnimationGroup.clean_up_from_scene"><span class="viewcode-link"><span class="pre"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">[来源]</font></font></span></span></a><a class="headerlink" href="#manim.animation.composition.AnimationGroup.clean_up_from_scene" title="此定义的固定链接"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">#</font></font></a></dt>
<dd><p><font style="vertical-align: inherit;"></font><a class="reference internal" href="manim.scene.scene.Scene.html#manim.scene.scene.Scene" title="手动场景.场景.场景"><code class="xref py py-class docutils literal notranslate"><span class="pre">Scene</span></code></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">完成动画后</font><font style="vertical-align: inherit;">清理。</font></font></p>
<p><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">如果动画是移除器，则这包括</font></font><a class="reference internal" href="manim.scene.scene.Scene.html#manim.scene.scene.Scene.remove" title="manim.scene.scene.Scene.remove"><code class="xref py py-meth docutils literal notranslate"><span class="pre">remove()</span></code></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">动画
</font></font><a class="reference internal" href="manim.mobject.mobject.Mobject.html#manim.mobject.mobject.Mobject" title="manim.mobject.mobject.Mobject"><code class="xref py py-class docutils literal notranslate"><span class="pre">Mobject</span></code></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">。</font></font></p>
<dl class="field-list simple">
<dt class="field-odd"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">参数</font></font></dt>
<dd class="field-odd"><p><strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">scene</font></font></strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;"> ( </font></font><a class="reference internal" href="manim.scene.scene.Scene.html#manim.scene.scene.Scene" title="手动场景.场景.场景"><em><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Scene</font></font></em></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;"> ) – 应清除动画的场景。</font></font></p>
</dd>
<dt class="field-even"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">返回类型</font></font></dt>
<dd class="field-even"><p><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">没有任何</font></font></p>
</dd>
</dl>
</dd></dl>

<dl class="py method">
<dt class="sig sig-object py" id="manim.animation.composition.AnimationGroup.finish">
<span class="sig-name descname"><span class="pre"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">完成</font></font></span></span><span class="sig-paren"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">( </font></font></span><span class="sig-paren"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">)</font></font></span><a class="reference internal" href="../_modules/manim/animation/composition.html#AnimationGroup.finish"><span class="viewcode-link"><span class="pre"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">[来源]</font></font></span></span></a><a class="headerlink" href="#manim.animation.composition.AnimationGroup.finish" title="此定义的固定链接"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">#</font></font></a></dt>
<dd><p><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">完成动画。</font></font></p>
<p><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">动画结束时会调用此方法。</font></font></p>
<dl class="field-list simple">
<dt class="field-odd"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">返回类型</font></font></dt>
<dd class="field-odd"><p><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">没有任何</font></font></p>
</dd>
</dl>
</dd></dl>

<dl class="py method">
<dt class="sig sig-object py" id="manim.animation.composition.AnimationGroup.get_all_mobjects">
<span class="sig-name descname"><span class="pre"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">获取所有对象</font></font></span></span><span class="sig-paren"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">( </font></font></span><span class="sig-paren"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">)</font></font></span><a class="reference internal" href="../_modules/manim/animation/composition.html#AnimationGroup.get_all_mobjects"><span class="viewcode-link"><span class="pre"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">[来源]</font></font></span></span></a><a class="headerlink" href="#manim.animation.composition.AnimationGroup.get_all_mobjects" title="此定义的固定链接"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">#</font></font></a></dt>
<dd><p><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">获取动画中涉及的所有 mobject。</font></font></p>
<p><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">顺序必须与 interpolate_submobject 的参数顺序匹配</font></font></p>
<dl class="field-list simple">
<dt class="field-odd"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">退货</font></font></dt>
<dd class="field-odd"><p><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">mobject 的序列。</font></font></p>
</dd>
<dt class="field-even"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">返回类型</font></font></dt>
<dd class="field-even"><p><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">序列[ </font></font><a class="reference internal" href="manim.mobject.mobject.Mobject.html#manim.mobject.mobject.Mobject" title="manim.mobject.mobject.Mobject"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Mobject</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;"> ]</font></font></p>
</dd>
</dl>
</dd></dl>

<dl class="py method">
<dt class="sig sig-object py" id="manim.animation.composition.AnimationGroup.init_run_time">
<span class="sig-name descname"><span class="pre"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">初始化运行时间</font></font></span></span><span class="sig-paren"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">（</font></font></span><em class="sig-param"><span class="n"><span class="pre"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">运行时间</font></font></span></span></em><span class="sig-paren"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">）</font></font></span><a class="reference internal" href="../_modules/manim/animation/composition.html#AnimationGroup.init_run_time"><span class="viewcode-link"><span class="pre"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">[来源]</font></font></span></span></a><a class="headerlink" href="#manim.animation.composition.AnimationGroup.init_run_time" title="此定义的固定链接"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">#</font></font></a></dt>
<dd><p><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">如果与 不同，则计算动画的运行时间</font></font><code class="docutils literal notranslate"><span class="pre">run_time</span></code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">。</font></font></p>
<dl class="field-list simple">
<dt class="field-odd"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">参数</font></font></dt>
<dd class="field-odd"><p><strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">run_time</font></font></strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;"> – 动画的持续时间（以秒为单位）。</font></font></p>
</dd>
<dt class="field-even"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">退货</font></font></dt>
<dd class="field-even"><p><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">动画的持续时间（以秒为单位）。</font></font></p>
</dd>
<dt class="field-odd"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">返回类型</font></font></dt>
<dd class="field-odd"><p><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">运行</font></font></p>
</dd>
</dl>
</dd></dl>

<dl class="py method">
<dt class="sig sig-object py" id="manim.animation.composition.AnimationGroup.interpolate">
<span class="sig-name descname"><span class="pre"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">插值</font></font></span></span><span class="sig-paren"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">(</font></font></span><em class="sig-param"><span class="n"><span class="pre"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">阿尔法</font></font></span></span></em><span class="sig-paren"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">)</font></font></span><a class="reference internal" href="../_modules/manim/animation/composition.html#AnimationGroup.interpolate"><span class="viewcode-link"><span class="pre"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">[来源]</font></font></span></span></a><a class="headerlink" href="#manim.animation.composition.AnimationGroup.interpolate" title="此定义的固定链接"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">#</font></font></a></dt>
<dd><p><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">设置动画进度。</font></font></p>
<p><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">动画期间的每一帧都会调用此方法。</font></font></p>
<dl class="field-list simple">
<dt class="field-odd"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">参数</font></font></dt>
<dd class="field-odd"><p><strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">alpha</font></font></strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;"> ( </font></font><em><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">float</font></font></em><font style="vertical-align: inherit;"><font style="vertical-align: inherit;"> ) – 设置动画的相对时间，0 表示开始，1 表示结束。</font></font></p>
</dd>
<dt class="field-even"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">返回类型</font></font></dt>
<dd class="field-even"><p><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">没有任何</font></font></p>
</dd>
</dl>
</dd></dl>

<dl class="py method">
<dt class="sig sig-object py" id="manim.animation.composition.AnimationGroup.update_mobjects">
<span class="sig-name descname"><span class="pre"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">update_mobjects</font></font></span></span><span class="sig-paren"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;"> ( </font></font></span><em class="sig-param"><span class="n"><span class="pre"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">dt</font></font></span></span></em><span class="sig-paren"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;"> )</font></font></span><a class="reference internal" href="../_modules/manim/animation/composition.html#AnimationGroup.update_mobjects"><span class="viewcode-link"><span class="pre"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">[来源]</font></font></span></span></a><a class="headerlink" href="#manim.animation.composition.AnimationGroup.update_mobjects" title="此定义的固定链接"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">#</font></font></a></dt>
<dd><p><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">更新诸如starting_mobject和（对于变换）target_mobject之类的内容。</font><font style="vertical-align: inherit;">请注意，由于通常（总是？） self.mobject 会在动画期间暂停其更新，因此这对 self.mobject 没有任何作用。</font></font></p>
<dl class="field-list simple">
<dt class="field-odd"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">参数</font></font></dt>
<dd class="field-odd"><p><strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">dt</font></font></strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">（</font></font><em><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">浮动</font></font></em><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">）–</font></font></p>
</dd>
<dt class="field-even"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">返回类型</font></font></dt>
<dd class="field-even"><p><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">没有任何</font></font></p>
</dd>
</dl>
</dd></dl>

</dd></dl>

</section>