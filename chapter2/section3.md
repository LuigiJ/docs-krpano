# 嵌入参数
<!-- Embedding Parameters -->
***
<!--
    The embedpano() function needs a Javascript object as argument. 
-->
**embedpano**函数需要一个js对象作为参数。  
<!--
    This object is used to pass all parameters (in random order) by using parametername:value pairs. 
-->
这个对象被用来传递所需的所有参数，参数的形式是该对象的属性名:值对。  
<!--
    Almost all parameters (except the target parameter) are optional - when they were not defined, their default values will be used.
-->
几乎所有的参数(除了target参数)都是可选的，当他们没有被定义时，将使用默认的值。  
  

<!-- The parameters object provides the following settings: -->
参数对象提供以下设置：  
```
xml:"krpano.xml"
```
<!-- Name and path to the startup xml file (relative to the html file). -->
* 启动xml文件的名称和路径(相对于html文件)。
<!-- When not set, the filename of .swf file will be used (e.g. 'krpano.xml' for 'krpano.swf'). -->
* 当没有设置时，将会使用.swf文件的文件名(例如：'krpano.xml'对应'krpano.swf')。
<!-- When no xml file should be loaded on startup, the value null can be used. -->
* 当启动时不加载xml文件时，可以使用null。
  

```
target:"...pano-div-id..."
```
<!-- The #id of the html element where the viewer should be embedded. -->
* 嵌入视图的HTML元素的id。
<!-- There will be an 'alert()' error when no target will be set. -->
* 当没有设置target时，将会`alert()`错误。
  
  
```
swf:"krpano.swf"
```
<!-- Name and path to the viewer '.swf' file (relative to the html file). -->
* 视图的'.swf'文件的名称和路径(相对于html文件)
<!-- The default is "krpano.swf". -->
* 默认值是`"krpano.swf"`
<!-- This file will be only used for the Flashplayer, when using only HTML5 this file will be not required. -->
* 这个文件仅仅用于Flashplayer，当只使用HTML5时不需要这个文件。
  
  
```
id:"krpanoSWFObject"
```
<!-- The id of the internal viewer object. -->
* 内部视图对象的id
<!-- This will be the object for interfacing the viewer via the Javascript-Interface. -->
* 这是通过js接口与视图交互的对象。
<!-- The default id is "krpanoSWFObject". -->
* 默认id是`"krpanoSWFObject"`。
<!-- It is important that each viewer will have an unique id! -->
* 每个视图拥有一个唯一的id是非常重要的。
<!-- When there already exists an object with the given id, then the embedding script will automatically add numbers at the end of the id until it is unique. -->
* 当已经存在具有给定id的对象时，嵌入脚本将自动在id的末尾添加数字，直到它是惟一的。
  

```
bgcolor:"#000000"
```
<!-- The background color of the viewer (in html color format). -->
* 视图的背景色(html颜色格式)
<!-- The default is "#000000" (=Black) -->
* 默认值是`"#000000"`(黑色)
  

```
html5:"auto"
```
<!-- Set the krpano HTML5 Viewer usage. -->
* 设置html5视图的用法
<!-- Possible settings: -->
* 可能的设置：
    <!-- auto - The default setting - automatically use the krpano HTML5 viewer.
        With that setting, the krpano HTML5 viewer will be used when possible by default (since version 1.19, in older versions Flash was used as default)! When HTML5 will be not possible, then the Flash viewer will be used as fallback. -->
    * **auto** - 默认设置 - 自动使用html5视图。使用此设置，html5视图将在默认情况下使用(自1.19版本以后，而在旧版本中Flash是默认使用的)！当html不可用时，Flash视图将作为备选。
    <!-- prefer - Prefer the usage of the krpano HTML5 viewer when possible, otherwise use Flash (same as auto since version 1.19). -->
    * **prefer** - 在html5视图可用时优先使用html5，否则使用Flash(与1.19版本之后的**auto**相同)
    <!-- fallback - Prefer the usage of the krpano Flash viewer when possible. Use the krpano HTML5 viewer only as fallback when Flash is not available. -->
    * **fallback** - 在Flash视图可用时优先使用Flash，只有当Flash不可用时，才使用html5。
    <!-- only - Only use the krpano HTML5 viewer - never use the krpano Flash viewer.
    With that setting, the krpano HTML5 viewer will be used when possible. When the system/browser is not HTML5-compatible, then an error message will be shown. -->
    * **only** - 仅仅使用html5视图 - 永远不会使用Flash视图。使用此设置，在html5视图可用时使用html5视图。当系统/浏览器不兼容HTML5时，将显示一条错误信息。
    <!-- always - Always use the krpano HTML5 viewer, regardless if the system and browser are  supporting the therefore necessary capabilities!
    Note - This setting should be only used for internal testing, never for publishing! -->
    * **always** - 始终使用html5视图，不管系统和浏览器是否能够支持！
        * **注意** - 这个测试应该只用于内部测试，永远不要用于发布！
    <!-- never - Never use the krpano HTML5 viewer, force using the krpano Flash viewer. -->
    * **never** - 永远不使用html5视图，强制使用Flash视图。
<!-- Additional extensions settings (for controlling the rendering method): -->
* 额外的扩展设置(用于控制渲染方法):
    <!-- +webgl - Use the krpano HTML5 viewer only when WebGL is available.
    Note - some features are only available when WebGL is available - e.g. panoramic-video-support, WebVR-support, stereo-rendering, spherical and cylindrical images, view distortions (fisheye, littleplanet), ... -->
    * **+webgl** - 只在webgl可用时使用html5视图。
        * **注意** - 有些功能只有在webgl可用时才可用 - 比如：全景视频支持，webvr支持，立体渲染，球面和柱面图像，视图失真(鱼眼、小行星)等等
    <!-- +css3d - Prefer the usage of CSS3D rendering instead of WebGL rendering (by default WebGL will be preferred when available). The css3d setting should be only used for internal testing, never for publishing! -->
    * **+css3d** - 优先使用css3d渲染代替webgl渲染(默认是webgl渲染)
        * **注意** - css3d设置应该只用于内部测试，而不要用于发布！
    <!-- Usage examples: -->
    * **使用案例:**
        <!-- prefer+webgl - Use the krpano HTML5 viewer only when WebGL is available, otherwise use Flash. -->
        * **prefer+webgl** - 仅仅当webgl可用时使用html5视图，否则使用Flash
        <!-- only+webgl - Use the krpano HTML5 viewer only when WebGL is available, otherwise show an error message. -->
        * **only+webgl** - 只有当webgl可用时使用html5视图，否则显示一条错误信息
  

```
flash:""
```
<!-- Set the krpano Flash Viewer usage. -->
* 设置Flash视图的用法
<!-- This is a basically the same as the html5 setting, just the inverse. It can be used for nicer urls, e.g. by using flash=prefer instead of html5=fallback. -->
* 这个基本上和html5的设置一样，不过正好相反。它可以用于良好的url，比如：使用`flash=prefer`代替`html5=fallback`
<!-- When the flash setting will be set, it will be mapped to a html5 setting and overwrite it. -->
* 当设置flash时，它将映射到html5设置并覆盖它
<!-- Possible settings: -->
* 可能的设置：
    <!-- auto or no setting - use the html5 setting. -->
    * **auto**或者不设置 - 应用html5设置
    <!-- prefer - Prefer the usage of the krpano Flash viewer when possible.
    Use the krpano HTML5 Viewer only when there is no Flashplayer and the system/browser is HTML5-compatible.
    This setting will be mapped to html5=fallback. -->
    * **prefer** - 如果可能的话，优先使用Flash视图。只有在没有flashplayer并且系统/浏览器对html5兼容时才使用html5视图。这个设置将映射到`html5=fallback`。
    <!-- fallback - Prefer the usage of the krpano HTML5 viewer when possible. Use the krpano Flash viewer only as fallback when HTML5 is not available.
    This setting will be mapped to html5=prefer. -->
    * **fallback** - 如果可能的话，优先使用html5视图。只有当html5不能使用时，使用flash视图。这个设置将映射到`html5=prefer`。
    <!-- only - Only use the krpano Flash viewer - never use the krpano HTML5 viewer.
    With that setting, the krpano Flash viewer will be used when possible. When there is no Flashplayer, then an error message will be shown.
    This setting will be mapped to html5=never. -->
    * **only** - 只是用Flash视图 - 永远不使用html5视图。有了这个设置，flash视图将在可用时被使用。当没有flashplayer时，将像是一条错误信息。这个设置将映射到`html5=never`。
    <!-- never - Never use the krpano Flash viewer, only use the krpano html5（原文错误） viewer.
    This setting will be mapped to html5=only. -->
    * **never** - 从不使用flash视图，只使用html5视图。这个设置将映射到`html5=only`。
  

```
wmode:"..."
```
<!-- Set the Flashplayer wmode setting. -->
* [flashplayer wmode](https://helpx.adobe.com/flash/kb/flash-object-embed-tag-attributes.html#main_Using_Window_Mode__wmode__values_)设置
<!-- Possible settings: -->
* 可能的设置:
    <!-- window - The Flashplayer default, a compromise between system support and performance. Note - on some systems and browsers html elements can't overlap the Flashplayer in this mode! See this wmode link for details. -->
    * **window** - 默认设置，在系统支持和性能之间的折衷。注意:在某些系统和浏览器上，html元素不能在此模式下与Flashplayer重叠!有关详细信息，请参见此[wmode](https://helpx.adobe.com/flash/kb/flash-object-embed-tag-attributes.html#main_Using_Window_Mode__wmode__values_)链接。
    <!-- opaque - Allow other html elements to overlap the Flashplayer (depending on the system and browser this can cause slower and jerky rendering). -->
    * **opaque** - 允许其他html元素与Flashplayer重叠(这取决于系统和浏览器，这可能导致更慢的和抖动的渲染)。