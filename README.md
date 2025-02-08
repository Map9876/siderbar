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
