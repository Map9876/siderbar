首先，看一下当前的代码结构。用户使用Flex布局，body设置为display:flex,子元素有.main-content, .spacer 和.sidebar。.main-content的宽度是100vw,.spacer的宽度是calc(90vw),而.sidebar的宽度是300px。这里的.spacer可能是用来将.sidebar推到右侧，但由于.main-content是100vw,可能覆盖了其他元素，导致需要水平滚动才能看到侧边栏。


就是刚好需要水平滚动才能看到侧边栏。
，充当侧边栏
n.cn

对于一个网站，我希望的是画面右侧，在打开网站时候刚好隐藏在画面的右侧范围内，但是其实可以左右滑动屏幕显示出来 给我这个html css 一体文件

https://github.com/copilot/c/4a8ca16a-0b15-45fe-a443-12b7734693c3

# siderbar
侧边栏菜单html
<!DOCTYPE html>
<html lang="en">
<head>
    <!-- 缓存控制标签保持不变 -->
    <meta http-equiv="Cache-Control" content="no-cache, no-store, must-revalidate">
    <meta http-equiv="Pragma" content="no-cache">
    <meta http-equiv="Expires" content="0">
    
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Static Sidebar</title>
    <style>
        body {
            margin: 0;
            overflow-x: scroll;
            display: flex;
        }
 
        .main-content {
            width: 90vw;
            height: 100vh;
            background-color: #f0f0f0;
            flex-shrink: 0;
        }
 
        .sidebar {
            width: 300px;
            height: 100vh;
            background-color: #333;
            color: white;
            flex-shrink: 0;
            padding: 20px;
            border-left: 3px solid #ff9900;
            box-shadow: -4px 0 10px rgba(0,0,0,0.2);
            display: flex;
            flex-direction: column;
        }
 
        /* 新增竖排文字样式 */
        .sidebar h2 {
            writing-mode: vertical-rl;
            text-orientation: upright;
            margin: 0 20px 0 0;
            padding: 15px 0;
            letter-spacing: 5px;
            transform: rotate(180deg);
            align-self: flex-start;
        }
 
        .sidebar a {
            color: white;
            text-decoration: none;
            display: block;
            margin: 10px 0;
        }
 
        .sidebar a:hover {
            text-decoration: underline;
        }
    </style>
</head>
<body>
    <div class="main-content">
        <h1>Welcome to My Website</h1>
    </div>
    <div class="sidebar">
        <h2>菜单栏</h2>
        <a href="#">新闻</a>
        <a href="#">关于</a>
        <a href="#">Bluray</a>
    </div>
</body>
</html>
