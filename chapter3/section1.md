# XML结构
***
<!-- Here a structured listing of all krpano xml elements: (click on an element to get more information) -->
这是所有的xml元素结构列表：
  
* **[&lt;krpano&gt;](./section3.md?#krpano)**  
    * **[&lt;include&gt;](./section3.md?#include)**
    * **[&lt;preview&gt;](./section3.md?#preview)**
    * **[&lt;image&gt;](./section3.md?#image)**
    * **[&lt;view&gt;](./section3.md?#view)**
    * **[&lt;area&gt;](./section3.md?#area)**
    * **[&lt;display&gt;](./section3.md?#display)**
    * **[&lt;control&gt;](./section3.md?#control)**
    * **[&lt;cursors&gt;](./section3.md?#cursors)**
    * **[&lt;autorotate&gt;](./section3.md?#autorotate)**
    * **[&lt;plugin&gt;](./section3.md?#plugin)**
    * **[&lt;layer&gt;](./section3.md?#layer)**
    * **[&lt;hotspot&gt;](./section3.md?#hotspot)**
    * **[&lt;style&gt;](./section3.md?#style)**
    * **[&lt;events&gt;](./section3.md?#events)**
    * **[&lt;action&gt;](./section3.md?#action)**
    * **[&lt;contextmenu&gt;](./section3.md?#contextmenu)**
    * **[&lt;network&gt;](./section3.md?#network)**
    * **[&lt;memory&gt;](./section3.md?#memory)**
    * **[&lt;security&gt;](./section3.md?#security)**
    * **[&lt;textstyle&gt;](./section3.md?#textstyle)**
    * **[&lt;lensflareset&gt;](./section3.md?#lensflareset)**
    * **[&lt;lensflare&gt;](./section3.md?#lensflare)**
    * **[&lt;data&gt;](./section3.md?#data)**
    * **[&lt;scene&gt;](./section3.md?#scene)**
    * **[&lt;set&gt;](./section3.md?#set)**
    * **[&lt;debug&gt;](./section3.md?#debug)**

<!-- The root element of the xml file need to be the <krpano> element. All other elements must be placed inside this element. -->
**&lt;krpano&gt;**是xml文件的根元素。所有的其他元素必须被放在krpano元素内。  

<!-- All xml elements and attributes in the krpano xml are optionally and can be defined a several times and in any order. When the same element will be defined again two or more times, then the later/following declarations will overwrite the previous ones. -->
所有的xml元素和属性都是可选的。可以以任意顺序定义很多次。当相同的内容被定义多次，后面的内容将覆盖前面的内容。  

<!-- It's also possible to define additional <krpano> elements inside the root <krpano> element itself for declaring additional settings at the krpano scope. -->
可以在根krpano元素中定义额外的krpano元素，用以说明在krpano作用域内额外的设置。  

<!-- The xml itself is just a transport-format - that means it will be only used to transport the data for the krpano viewer. When the xml will parsed, then the xml elements will be transformed/mapped into the krpano internal data structures. That means after parsing there is internally no xml anymore. -->
xml本身只是传输格式 - 也就是说他仅仅被用来向krpano视图传递数据。当xml被解析，这些xml元素将被转换/映射到krpano内部数据结构。这意味着在内部解析之后不在需要xml。