# 移除视图
<!-- Viewer Removing -->
***
<!-- For removing the pano viewer from the html page the removepano() function need to be used! The removepano() function will remove all internally attached mouse-fixes (Flash) and all DOM elements and events (HTML5). -->
需要使用removepano函数从html页面中移除视图。
  
removepano函数将会移除所有内部附加的mouse-fixes(Flash)、DOM元素、events(HTML5)。
  
```
removepano(id);
```
<!-- The removepano() function need to be called with the unique id of the viewer object. -->
* removepano函数需要在调用时传入唯一的视图对象id
* 例如：
    ```
    embedpano({target:"panoDIV", id:"pano1"});

    ...

    removepano("pano1");
    ```