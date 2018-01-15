#嵌入HTML
<!-- 
    Embedding into HTML
        1. For embedding the krpano viewer into a HTML page the core 'krpano.js' script file (the filename can differ) need to be included and the embedpano() function be called.
        2. The embedpano function detects the browser support and decides which krpano viewer to use (the krpano HTML5 or krpano Flash viewer).
        3. When using the krpano Flash viewer, the embedding script also applies several Flashplayer and Browser fixes and workarounds (e.g. to enable the Mouse-wheel usage inside Flash on systems where this isn't supported).
        4. This makes the embedding of the krpano viewer easy and simple - just one script include and one line embedding code.
-->
***
1. 为了能过将全景嵌入HTML，需要将核心脚本**krpano.js**(文件名可以不同)，包含到HTML页面，并调用**embedpano()**函数。
2. embedpano函数会检查浏览器的支持情况，并决定使用哪种全景视图(HTML5或者FLASH)。
3. 在使用**krpano Flash**查看器时，嵌入脚本还应用了几个Flashplayer和浏览器补丁和变通方法(例如，在不支持Flash的系统中能够使用鼠标滚轮)。
4. 这使得krpano的嵌入变得简单和易用————只需包含一个脚本和一行嵌入代码。

##文档细目
***
<!-- Script Including -->
* [引入脚本](./section1.md)
<!-- Viewer Embedding -->
* [嵌入视图](./section2.md)
<!-- Embedding Parameters -->
* [嵌入参数](./section3.md)
<!-- Viewer Removing -->
* [移除视图](./section4.md)