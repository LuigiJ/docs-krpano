#引入脚本
<!-- Script Including -->
***
<!-- The krpano script file need to be included once anywhere (but before the embedpano() usage) in the html page: -->
krpano脚本文件只要在HTML页面的任意位置引入一次(但是必须在调用embedpano()函数之前引入):
`<script src="krpano.js"></script>`

<!-- Some details and notes: -->
细节和说明
<!-- The 'krpano.js' file can be named different - e.g. when using the MAKE PANO or MAKE VTOUR droplets it's typically named 'pano.js' or 'tour.js'. -->
* krpano.js文件可以使用其他名字 —— 比如：当使用 *MAKE PANO* 或者 *MAKE VTOUR* 制作droplets的时候，他通常被命名为pano.js或者tour.js
<!-- The file itself contains two parts - the krpano embedding script and the krpano HTML5 viewer. The krpano Flash viewer is a separate external file (e.g. the 'krpano.swf' file). -->
* 文件本身包含两部分内容：
    * krpano嵌入脚本
    * krpano的HTML5视图
    * Flash视图是一个单独的外部文件(比如：krpano.swf)
<!--
The file is always the same, it doesn't contain any pano or tour specific information, that means it could be shared across several panos/tours or projects.
E.g. to make later updates easier just use only one global folder for the krpano viewer and plugins files and link from all other projects to them. Then all projects can be updated by only updating the global krpano files.
-->
* 该文件始终是相同的，它不包含任何的pano或者tour的特定信息，这说明它能够在多个panos/tours或者项目中共享。(例如：为了使以后的更新更容易，只需使用一个全局文件夹放置krpano视图和插件文件，并将所有其他项目链接到它们。然后，所有的项目都可以通过更新全局krpano文件来更新。)