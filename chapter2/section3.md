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
    <!-- opaque-flash - Same as opaque but only for the Flashplayer (will be ignored by the HTML5 viewer - see the HTML5 notes below) -->
    * **opaque-flash** - 与opaque相似，但是仅仅针对flashplayer(HTML5视图将被忽略 - 参见下面的HTML5注意)
    <!-- transparent - Make the Flashplayer background transparent to allow seeing html elements behind the Flashplayer and additionally also allow other html elements to overlap the Flashplayer (depending on the system and browser this can cause slower and jerky rendering). -->
    * **transparent** - 使flashplayer背景透明，允许看到flashplayer后面到html元素，此外还允许其他到html元素与flashplayer重叠(取决于系统和浏览器，这可能导致更慢到和抖动到渲染)。
    <!-- transparent-flash - Same as transparent but only for the Flashplayer (will be ignored by the HTML5 viewer - see the HTML5 notes below). -->
    * **transparent-flash** - 与transparent相似，但是仅仅针对flashplayer(HTML5视图将被忽略 - 参见下面的HTML5)。
    <!-- direct - Best performance, hardware accelerated presentation, no html overlapping on many systems and browsers (this is typically the fastest mode but on incompatible or older systems and browsers this can cause slowdowns). -->
    * ** direct ** - 最佳性能，硬件加速，在许多系统和浏览器上没有重叠(者通常是是最快的方式，但是在不兼容和较久的浏览器上可能会导致不可用)。
<!-- krpano will use wmode=direct by default, except for Chrome - there wmode=window will be used by default (better performance and no black window during resizing). -->
* 默认情况下krapno将使用**wmode=direct**，除了Chrome - 默认使用**wmode=window**(在改变尺寸的时候拥有更好的性能并且没有黑屏)。
<!-- HTML5 notes: The wmode setting is typically a Flashplayer setting, but wmode=opaque and wmode=transparent will be evaluated also by the krpano HTML5 viewer and make the viewer background transparent there too. Overlapping html elements itself are always possible when using the HTML5 viewer. -->
* HTML5注意：**wmode**通常是flashplayer的设置，但是**wmode=opaque**和**wmode=transparent**也计算html5视图并使其背景透明。当使用html5视图时html元素自身可以重叠。  
  
```
localfallback:"http://localhost:8090"
```
<!-- When running HTML5 content locally with file:// urls several browsers (especially Chrome and Safari) are restricting the dynamic loading of data files! In the krpano HTML5 viewer this affects the xml and plugin loading. -->
* 当以本地文件**file:// urls**的方式运行html5时，一些浏览器(尤其是Chrome和Safari)限制加载动态的数据文件！这将影响xml和plugin在html5视图上的加载。
<!-- For more information about this case please see here - Local Usage. -->
* 这种情况下更多的信息请参见这里 - [本地使用](https://krpano.com/docu/localusage/#top)
<!-- To avoid just getting a xml loading error in this case, the embedding script checks in this case if loading would be possible and if not, it offers some alternative solutions. -->
* 为了避免这种加载xml错误，嵌入脚本检查并在不允许的情况下提供一些代替方案。
<!-- Possible settings: -->
* 可能的设置：
    <!-- An url of the krpano Testing Server (by default http://localhost:8090) -->
    * **krpano测试服务(默认http://localhost:8090)**
        <!-- When the localfallback setting will be set to an url of the krpano Testing Server (the default case) and the server is currently already running, then the current page will be automatically redirected to the testing server to allow a full featured local usage. -->
        * 当localfallback设置为一个url(默认情况)并且服务已经运行，那么当前页将会自动重定向到测试服务器，允许完整的本地使用。
        <!-- When the server is not running, the error fallback case will be used. -->
        * 如果服务没有运行，将使用错误回退。
    <!-- flash - Use the krpano Flash viewer instead. The Flashplayer is not affected by the local browser restrictions. -->
    * **flash** - 使用flash视图替代。flashplayer不受浏览器本地限制的影响。
    <!-- error - Show an error and information message about local usage. The error message could be customized by using the onerror callback. -->
    * **error** - 显示一条本地使用的错误信息。该信息可以使用onerror回调函数定制。
    <!-- none - Ignore that they are local restrictions and start the HTML5 viewer anyway... -->
    * **none** - 忽略本地限制并启动html5视图。。。  

```
vars:{...}
```
<!-- Pass a Javascript Object with krpano variable:value pairs. -->
* 传入一个js对象**属性:值** ==> krpano **变量:值**
<!-- The variables will be set AFTER the xml file has been be loaded and parsed. So these variables can be used to add new settings or to overwrite settings that were already defined in the xml. -->
* 这些变量将被之后的xml文件加载和解析。它们可以用于在xml中添加设置或者覆盖已有的设置。
<!-- Example: -->
* 比如：
    ```
    var settings = {};
    settings["onstart"] = "trace('on start...')";
    settings["view.hlookat"] = 30;
    embedpano({xml:"pano.xml", target:"pano", vars:settings});
    ```
      
```
initvars:{...}
```
<!-- Pass a Javascript Object with krpano variable:value pairs. -->
* 传入一个js对象**属性:值** ==> krpano **变量:值**
<!-- This is basically the same as the vars setting, but these variables will be set BEFORE the xml file wil be loaded and parsed. -->
* 这基本上时和vars一样的设置，但是这些变量将在xml之前加载和解析。
<!-- The main usage of this setting will be to set custom path variables that can be used as placeholders inside url paths in the xml files and / or to set variables that can be used inside xml-if-checks for <include> elements. -->
* 主要用于设置自定义路径变量，然后在xml文件中替换内部占位符。或者用于xml内部的[if检查和include元素](https://krpano.com/docu/xml/#if)
* 比如：
    ```
    JS:
    embedpano({..., initvars:{mypath:"./panos1/"} });
    XML:
    url="%$mypath%image.jpg"

    JS:
    embedpano({..., initvars:{design:"flat"}, ...});
    XML:
    <include url="design_default.xml" if="design == default" />
    <include url="design_flat.xml"    if="design == flat"    />
    ```
<!-- To be able to pass initvars variables via http queries directly at the url of the html file this syntax need to be used: -->
* 可以直接通过html的url查询传入initvars变量
    ```
    tour.html?initvars.variable=value
    ```
      
```
basepath:...
```
<!-- Sets a custom base-path for resolving paths that are relative to the krpano swf file. -->
* 设置自定义的基础路径解析相对于swf文件的路径
<!-- Can be used in Flash and HTML5 for adjusting relative paths in the xml. -->
* 用于在xml中调整相对路径
  
```
consolelog:false
```
<!-- A Boolean setting that defines if krpano log/trace-messages should be sent also to the browser Javascript console. -->
* 用来设置是否krpano的日志跟踪消息发送到浏览器的js控制台
  
```
mwheel:true
```
<!-- A Boolean setting to control the mouse-wheel usage. -->
* 控制鼠标滚轮的使用。
<!-- When set to true (the default), then the mouse-wheel events will be captured and can be used in the viewer (e.g. for zooming). -->
* 当设置为true(默认)，鼠标滚轮事件将被捕获并可以用于视图(比如：缩放)。
<!-- When set to false, then any mouse-wheel usage will be ignored and the browser will do its default mouse-wheel handling (typically scrolling the webpage). -->
* 当设置为false，鼠标滚轮的使用将被忽略，并且浏览器将会执行默认的鼠标滚轮处理(通常是滚动页面)。
  
```
capturetouch:true
```
<!-- A Boolean setting to control the captureing of touch events. -->
* 控制触摸事件的捕获。
<!-- When set to true (the default), then the touch events will be captured and can be used in the viewer (e.g. for panning and zooming). -->
* 当设置为true(默认)，触摸事件将被捕获并可以用于视图(比如：平移和缩放)。 
<!-- When set to false, then touch events itself will be still used by the viewer, but their default event processing will be not stopped. That means in this case the browser might pan or zoom the webpage. -->
* 当设置为false，触摸事件本身仍然可用于视图，但是它们的默认事件处理会停止。这一位置在这种情况下浏览器可能拖动或缩放页面。
  
```
focus:true
```
<!-- A Boolean setting to give the viewer the input / keyboard focus on startup. -->
* 在启动时自动让视图获取到输入设备的焦点。
<!-- When not set, the setting will be set automatically depending on the viewer size - when the viewer will cover the whole webpage, focus will be set to true, otherwise to false. -->
* 当不设置时，将根据视图尺寸自动设置 - 当视图覆盖整个web页面时，focus将设置为true，否则为false。
<!-- This works only in HTML5 (all browsers) and in the Chrome Flashplayer. In other browsers the Flash element requires an initial click by the user for getting the focus. -->
* 只在html5(所有浏览器)和chrome的flashplayer中有效。在其他的浏览器中，flash元素需要用户的初始点击才能获取到焦点。
  
```
webglsettings:{preserveDrawingBuffer:false, depth:false, stencil:false}
```
<!-- Pass an object with special settings for the WebGL context creation. -->
* 为创建webgl上下文而传入的特殊设置。
<!-- The WebGL context will be created at startup and can't be changed at runtime, therefore these settings need to be specified already during embedding. -->
* webgl上下文需要在启动时创建并且不能在运行时修改，因此这些设置需要在嵌入时制定。
<!-- Available settings: -->
* 可用设置：
    <!-- preserveDrawingBuffer - Keep the drawing buffer content. Would need to be enabled for when trying to make screenshots of the WebGL canvas via toDataURL or readPixels, false by default. -->
    * **preserveDrawingBuffer** - 保留绘图缓冲区内容。在尝试通过toDataUrl或readPixels制作WebGL画布截屏时需要启动它，默认是false。
    <!-- depth - Create a depth buffer, false by default. Would need to be enabled for the correct ThreeJS plugin usage. -->
    * **depth** - 创建一个深度缓冲区，默认是false。使用[ThreeJS](https://krpano.com/forum/wbb/index.php?page=Thread&threadID=12479)插件时需要启用它。
    <!-- stencil - Create a stencil buffer, false by default. -->
    * **stencil** - 创建一个模板缓冲区，默认false。
    <!-- failIfMajorPerformanceCaveat - Don't use WebGL when the rendering performance would be dramatically lower than the OpenGL rendering performance of a native application, false by default. -->
    * **failIfMajorPerformanceCaveat** - 在原生应用中当webgl渲染性能明显低于opengl时不使用webgl，默认是false。
<!-- All these settings are disabled by default for performance and memory reasons (especially on mobile devices). -->
* 考虑到性能和内存的原因，这些设置默认都是被禁用的(尤其是在移动设备)。
  
```
mobilescale:0.5
```
<!-- By default all krpano content on mobile devices will be scaled by 0.5. -->
* krpano内容在移动设备上默认被缩放0.5倍。
<!-- To disable that scaling, set the mobilescale setting to 1.0. -->
* 禁止缩放，设置为1.0。
<!-- This can be useful for implementing responsive webdesigns. -->
* 这将用于实现响应式设计。
<!-- See also the xml stagescale setting. -->
* 参见[stagescale](https://krpano.com/docu/actions/#stagescale)设置。
  
```
fakedevice:""
```
<!-- Fake the krpano device detection settings. -->
* 伪装设备检测
<!-- Available settings: "mobile", "tablet", "desktop". -->
* 可用的设置："mobile", "tablet", "desktop".
<!-- Note - This setting should be only used for internal testing, never for publishing! -->
* **注意：-这个设置仅仅应仅用于内部测试，不要用于生产发布**
  
```
onready:...Javascript-Function...
```
<!-- The onready setting can be used to set a call-back-function to get notified when the embedding is done and the krpano viewer is ready for usage. -->
* 嵌入完成并且krpano视图可用时的回调函数。
<!-- The given function will be called with the krpano Javascript-Interface object. -->
* 该函数将被krpano的[Javascript-Interface](https://krpano.com/docu/js/#interfaceobject)对象调用。
* 例如：
    ```
    embedpano({target:"krpanoDIV", onready:krpanoReady});

    function krpanoReady(krpano)
    {
        krpano.call("trace(krpano is ready...)");
    }
    ```
<!-- Flashplayer Notes: This function requires the External Interface of the Flashplayer! This means the call-back will work offline/locally only when the security settings of the Flashplayer were adjusted. See here for more detatils - Local / Offline Usage. -->
* Flashplayer注意：这个函数需要flashplayer外部接口。这意味着只有调整为安全的设置才可以在离线/本地可用。了解更多[Local / Offline Usage](https://krpano.com/docu/localusage/#top)。
  
```
onerror:...Javascript-Function...
```
<!-- The onerror setting can be used to set a custom embedding-error-handling function. -->
* 设置自定义的嵌入错误处理。
<!-- The given function will be called with an error-message string as parameter. -->
* 该函数被调用时会传入一个错误信息的字符串参数。
  
```
passQueryParameters:false
```
<!-- A Boolean setting. When set to true, all query parameters from the html url will be passed to the viewer as variables. -->
* 当设置为true，所有的urlquery参数会作为变量传入视图。
<!-- When enabled, it will be also possible to pass the html5, flash, wmode, mobilescale, fakedevice and initvars settings directly at the html url. -->
* 当可用时，它也可以直接在html的url中传入html5、flash、wmode、mobilescale、fakedevice和initvars设置。
* 使用方式：
    ```
    tour.html?html5=only&startscene=scene2&initvars.design=flat
    ```
