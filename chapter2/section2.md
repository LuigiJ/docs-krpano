#嵌入视图
<!-- Viewer Embedding -->
***
<!-- Create anywhere on the html page a <div> element where the viewer should be embedded, give that div element an unique 'id' name and define its size via css styles: -->
在HTML页面的任意位置创建一个**div**标签用来嵌入视图，给该**div**元素一个唯一的**id**名并通过css来定义它的大小:

`<div id="pano" style="width:100%;height:100%;"></div>`

<!-- After defining the <div> element, create a <script> element with the embedding script code.
For the embedding itself there is the global embedpano() function:  -->
在定义了div元素之后，创建一个`<script>`元素。对于嵌入本身，它是一个全局函数embedpano():

1. embedpano({...embedding parameters...});
    <!-- The embedpano() function needs an object with the embedding parameters. -->
2. embedpano()函数需要一个带有嵌入参数的对象
3. 完整的例子
    ```
    <script src="krpano.js"></script>
    <div id="pano" style="width:600px; height:400px;"></div>
    <script>
        embedpano({swf:"krpano.swf", xml:"pano.xml", target:"pano"});
    </script>
    ```
