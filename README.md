<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>个人主页 | 个人作品集</title>
    <style>
        /* 全局重置与全局样式 */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: "Segoe UI", "Microsoft YaHei", sans-serif;
        }

        body {
            background-color: #f8fafc;
            color: #222;
            line-height: 1.8;
        }

        /* 导航栏 磨砂透明风格 */
        nav {
            width: 100%;
            background: rgba(255,255,255,0.85);
            backdrop-filter: blur(8px);
            box-shadow: 0 2px 10px #00000010;
            position: sticky;
            top: 0;
            z-index: 99;
        }

        .nav-container {
            max-width: 1100px;
            margin: 0 auto;
            display: flex;
            justify-content: center;
            gap: 40px;
            padding: 16px;
            flex-wrap: wrap;
        }

        .nav-container a {
            text-decoration: none;
            color: #234e9d;
            font-weight: 500;
            transition: 0.3s;
        }

        .nav-container a:hover {
            color: #2575fc;
        }

        /* 头部个人Banner */
        .hero {
            width: 100%;
            padding: 70px 20px;
            text-align: center;
            background: linear-gradient(120deg, #f0f6ff, #ffffff);
        }

        .hero-avatar {
            width: 150px;
            height: 150px;
            border-radius: 50%;
            background: linear-gradient(135deg, #2575fc, #4299ff);
            margin: 0 auto 20px;
            display: flex;
            align-items: center;
            justify-content: center;
            color: #fff;
            font-size: 50px;
            font-weight: bold;
            box-shadow: 0 8px 20px #2575fc40;
        }

        .hero h1 {
            color: #1e3a8a;
            font-size: 34px;
        }

        .hero p {
            color: #555;
            margin-top: 8px;
        }

        /* 通用容器 */
        .wrap {
            max-width: 1100px;
            margin: 60px auto;
            padding: 0 20px;
        }

        .title {
            font-size: 24px;
            color: #1e3a8a;
            border-left: 4px solid #2575fc;
            padding-left: 12px;
            margin-bottom: 20px;
        }

        /* 关于我 */
        #about p {
            color: #444;
            text-indent: 2em;
        }

        /* 技能进度条新版样式 */
        .skill {
            margin-bottom: 25px;
        }

        .skill-top {
            display: flex;
            justify-content: space-between;
            margin-bottom: 6px;
        }

        .skill-bar-bg {
            width: 100%;
            height: 12px;
            background: #e2e8f0;
            border-radius: 10px;
            overflow: hidden;
        }

        .skill-bar {
            height: 100%;
            background: linear-gradient(90deg, #2575fc, #42b9ff);
            border-radius: 10px;
            transition: all 1.2s ease;
            width: 0;
        }

        /* 项目卡片 磨砂卡片风格 */
        .project-box {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 20px;
        }

        .project-card {
            background: #fff;
            padding: 25px;
            border-radius: 14px;
            box-shadow: 0 4px 12px #0000000c;
            transition: 0.3s;
        }

        .project-card:hover {
            transform: translateY(-8px);
            box-shadow: 0 10px 25px #2575fc20;
        }

        .project-card h3 {
            color: #1e3a8a;
            margin-bottom: 10px;
        }

        /* 联系表单 */
        form {
            max-width: 650px;
        }

        .input-item {
            margin-bottom: 18px;
        }

        .input-item label {
            display: block;
            margin-bottom: 5px;
            color: #333;
        }

        .input-item input,
        .input-item textarea {
            width: 100%;
            padding: 12px 16px;
            border: 1px solid #ddd;
            border-radius: 8px;
            font-size: 15px;
            transition: 0.3s;
        }

        .input-item input:focus,
        .input-item textarea:focus {
            border-color: #2575fc;
            outline: none;
            box-shadow: 0 0 0 3px #2575fc18;
        }

        button {
            padding: 12px 30px;
            background-color: #2575fc;
            color: #fff;
            border: none;
            border-radius: 8px;
            cursor: pointer;
            font-size: 16px;
            transition: 0.3s;
        }

        button:hover {
            background-color: #1e61d8;
        }

        /* 页脚 */
        footer {
            text-align: center;
            padding: 30px;
            background: #1e3a8a;
            color: #fff;
            margin-top: 40px;
        }

        /* 移动端适配 */
        @media(max-width:600px){
            .nav-container{gap:20px;}
            .hero h1{font-size:26px;}
        }
    </style>
</head>
<body>

    <!-- 导航栏 -->
    <nav>
        <div class="nav-container">
            <a href=" ">首页</a >
            <a href="#about">关于我</a >
            <a href="#skill">专业技能</a >
            <a href="#project">项目展示</a >
            <a href="#contact">联系方式</a >
        </div>
    </nav>

    <!-- 头部Banner -->
    <section class="hero" id="home">
        <div class="hero-avatar">X</div>
        <h1>个人自我介绍</h1>
        <p>热爱前端开发｜专注网页设计｜积极进取的计算机学生</p >
    </section>

    <!-- 关于我 -->
    <div class="wrap" id="about">
        <h2 class="title">关于我</h2>
        <p>我是一名计算机专业在读学生，在校期间系统学习了网页设计、前端开发、计算机基础等课程。我热爱网页制作，喜欢简约干净的设计风格。本个人网站为课程期末作业，采用原生HTML、CSS、JavaScript开发，无任何外部框架与资源依赖，结构清晰、适配移动端，具备完整的展示与交互功能。</p >
    </div>

    <!-- 技能进度条 -->
    <div class="wrap" id="skill">
        <h2 class="title">专业技能</h2>

        <div class="skill">
            <div class="skill-top"><span>HTML 网页结构搭建</span><span>92%</span></div>
            <div class="skill-bar-bg"><div class="skill-bar" data-width="92%"></div></div>
        </div>

        <div class="skill">
            <div class="skill-top"><span>CSS 样式布局美化</span><span>88%</span></div>
            <div class="skill-bar-bg"><div class="skill-bar" data-width="88%"></div></div>
        </div>

        <div class="skill">
            <div class="skill-top"><span>JavaScript 交互开发</span><span>75%</span></div>
            <div class="skill-bar-bg"><div class="skill-bar" data-width="75%"></div></div>
        </div>

        <div class="skill">
            <div class="skill-top"><span>响应式网页设计</span><span>80%</span></div>
            <div class="skill-bar-bg"><div class="skill-bar" data-width="80%"></div></div>
        </div>
    </div>

    <!-- 项目展示 -->
    <div class="wrap" id="project">
        <h2 class="title">项目展示</h2>
        <div class="project-box">
            <div class="project-card">
                <h3>个人单页展示网站</h3>
                <p>采用原生前端技术开发，包含导航、技能、项目、表单完整模块，支持移动端自适应，动画流畅，结构规范。</p >
            </div>
            <div class="project-card">
                <h3>静态课程展示页面</h3>
                <p>多区块布局设计，配色简洁舒适，适合课程作业展示，代码整洁、注释完善，可直接部署上线。</p >
            </div>
            <div class="project-card">
                <h3>交互式留言表单</h3>
                <p>原生JS实现表单验证与提交提示，界面简约高级，交互友好，符合现代网页设计标准。</p >
            </div>
        </div>
    </div>

    <!-- 联系表单 -->
    <div class="wrap" id="contact">
        <h2 class="title">联系我</h2>
        <form id="form">
            <div class="input-item">
                <label>姓名</label>
                <input type="text" placeholder="请输入姓名" required>
            </div>
            <div class="input-item">
                <label>邮箱</label>
                <input type="email" placeholder="请输入邮箱" required>
            </div>
            <div class="input-item">
                <label>留言内容</label>
                <textarea rows="5" placeholder="请输入留言内容" required></textarea>
            </div>
            <button type="submit">提交留言</button>
        </form>
    </div>

    <!-- 页脚 -->
    <footer>
        <p>© 2026 个人主页 | 前端期末作业 原创设计</p >
    </footer>

    <script>
        // 进度条滚动动画
        window.onload = function(){
            let bars = document.querySelectorAll(".skill-bar");
            bars.forEach(item=>{
                item.style.width = item.dataset.width;
            })
        }

        // 平滑滚动
        let aTags = document.querySelectorAll(".nav-container a");
        aTags.forEach(a=>{
            a.onclick = function(e){
                e.preventDefault();
                document.querySelector(this.getAttribute("href")).scrollIntoView({behavior:"smooth"});
            }
        })

        // 表单提交提示
        document.getElementById("form").onsubmit = function(e){
            e.preventDefault();
            alert("提交成功！感谢您的留言！");
            this.reset();
        }
    </script>

</body>
</html>
