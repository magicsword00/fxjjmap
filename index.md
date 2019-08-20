## Welcome to GitHub Pages

You can use the [editor on GitHub](https://github.com/magicsword00/fxjjmap/edit/master/index.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
<!doctype html>
<html>
<head>
    <meta charset="utf-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="initial-scale=1.0, user-scalable=no, width=device-width">
    <title>信息窗体内的事件交互</title>
    <link rel="stylesheet" href="https://a.amap.com/jsapi_demos/static/demo-center/css/demo-center.css"/>
    <style>
        html, body, #container {
            height: 100%;
            width: 100%;
        }
        .btn {
            position: relative;
            width: 12rem;
            left: 3.6rem;
            margin: 10px 0 0 0;
        }
    </style>
</head>
<body>
<div id="container"></div>
<script type="text/javascript"
        src="https://webapi.amap.com/maps?v=1.4.15&key=您申请的key值"></script>
<script type="text/javascript">
    var lnglat = new AMap.LngLat(116.397,39.918);

    // 创建地图实例
    var map = new AMap.Map("container", {
        zoom: 14,
        center: lnglat,
        resizeEnable: true
    });

    // infowidnow 的 innerHTML
    var infoWindowContent =
        '<div className="custom-infowindow input-card">' +
            '<label style="color:grey">故宫博物院</label>' +
            '<div class="input-item">' +
                '<div class="input-item-prepend">' +
                    '<span class="input-item-text" >经纬度</span>' +
                '</div>' +
                '<input id="lnglat" type="text" />' +
            '</div>' +
            // 为 infowindow 添加自定义事件
            '<input id="lnglat2container" type="button" class="btn" value="获取该位置经纬度" onclick="getLngLat()"/>' +
        '</div>';

    // 创建一个自定义内容的 infowindow 实例
    var infoWindow = new AMap.InfoWindow({
        position: lnglat,
        offset: new AMap.Pixel(0, -35),
        content: infoWindowContent
    });

    infoWindow.open(map);

    // 将当前经纬度展示在 infowindow 的 input 中
    function getLngLat(){
        var lnglatInput = document.getElementById('lnglat');

        lnglatInput.setAttribute('value', lnglat.toString());
    }

</script>
</body>
</html>
# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/magicsword00/fxjjmap/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
