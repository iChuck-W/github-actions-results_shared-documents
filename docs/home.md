# My **Open Publishing** Space

## Create, Share and Collaborate

![Photo of Mountain](images/mountain.jpg)

[Docsify](https://docsify.js.org/#/) can generate article, portfolio and documentation websites on the fly. Unlike Docusaurus, Hugo and many other Static Site Generators (SSG), it does not generate static html files. Instead, it smartly loads and parses your Markdown content files and displays them as a website.

## Website Pages
- [Introduction](introduction.md)
- [Topic One](topic-one.md)
- [Topic Two](topic-two.md)
- Topic Three
    - [Overview](topic-three-overview.md)
    - [Subtopic One](topic-three-subtopic-one.md)
    - [Subtopic Two](topic-three-subtopic-two.md)

 <!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>实时时钟</title>
<script>
function showTime() {
    var date = new Date(); // 获取当前时间
    var h = date.getHours(); // 获取小时
    var m = date.getMinutes(); // 获取分钟
    var s = date.getSeconds(); // 获取秒数

    // 如果小时、分钟或秒数小于10，前面补0
    h = checkTime(h);
    m = checkTime(m);
    s = checkTime(s);

    // 将时间显示在网页上
    document.getElementById('clock').innerHTML = h + ":" + m + ":" + s;

    // 1000毫秒后再次执行showTime函数，实现时间更新
    setTimeout(showTime, 1000);
}

// 补0函数
function checkTime(i) {
    if (i < 10) {
        i = "0" + i;
    }
    return i;
}
</script>
</head>
<body onload="showTime()">
    <h1>当前时间:</h1>
    <div id="clock"></div> <!-- 时间将显示在这里 -->
</body>
</html>
