---
hide:
  - navigation
  - toc
---
# Xiiiing 
<style>
/* ======================
   基础样式
====================== */
body {
  font-family: 'Segoe UI', sans-serif;
  line-height: 1.8;
  color: var(--md-default-fg-color);
  margin: 0;
  padding: 0;
}

.md-main__inner {
  display: flex;
  height: 100%;
  margin-top: 0rem;
}

.md-content {
  flex-grow: 1;
  min-width: 0;
}

.md-content__inner {
  margin: 0rem 0rem;
  padding-top: 0rem;
}

.md-content__inner:before {
  content: "";
  display: block;
  height: 0rem;
}

.container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0px 0px;
}

.md-typeset h1 {
  display: none; /* 完全隐藏，不占据空间 */
}

/* ======================
   布局容器
====================== */
.flex-container {
  display: flex;
  flex-wrap: wrap;
  gap: 30px;
  margin-top: 60px;
}

.text-section {
  flex: 1 1 60%;
  min-width: 0;
}

.map-section {
  flex: 1 1 35%;
  min-width: 0;
  position: relative;
}

/* ======================
   板块通用样式
====================== */
.section {
  margin-bottom: 40px;
  padding: 20px;
  border-radius: 8px;
  transition: transform 0.3s ease, box-shadow 0.3s ease;
  box-shadow: 0 2px 15px rgba(0, 0, 0, 0.05);
}

.section:hover {
  transform: translateY(-5px);
  box-shadow: 0 10px 25px -5px rgba(0, 0, 0, 0.08);
}

.section h3 {
  font-size: 1.8em;
  color: var(--md-default-fg-color);
  margin: 0 0 25px;
  position: relative;
  padding-left: 20px;
}

.section h3::before {
  content: '';
  position: absolute;
  left: 0;
  top: 50%;
  transform: translateY(-50%);
  width: 8px;
  height: 80%;
  background-color: #1e3a8a;
}

/* ======================
   文字段落样式
====================== */
.text-section p {
  padding-left: 30px;
}

.text-section ul {
  margin: 15px 0;
  padding-left: 20px;
  list-style: none;             
}

.text-section ul li {
  padding-left: 0px;
  margin-bottom: 10px;
  position: relative;
}

.text-section ul li::before {
  content: attr(data-icon);
  display: inline-block;
  width: 1em;
  margin-left: -1.5em;
  color: #1e3a8a;
  font-weight: bold;
}

/* ======================
   地图模块样式
====================== */
.map-wrapper {
  position: relative;
  width: 100%;
  height: 500px;
  border-radius: 8px;
  overflow: hidden;
  box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.05);
  transition: box-shadow 0.3s ease;
}

.map-wrapper:hover {
  box-shadow: 0 10px 25px -5px rgba(0, 0, 0, 0.08);
}

#map-container {
  width: 100%;
  height: 100%;
  z-index: 1;
}

.map-overlay {
  position: absolute;
  bottom: 0;
  left: 0;
  right: 0;
  background: rgba(30, 58, 138, 0.8);
  color: #fff;
  padding: 15px 20px;
  transform: translateY(100%);
  transition: transform 0.3s ease;
  z-index: 2;
}

.map-wrapper:hover .map-overlay {
  transform: translateY(0);
}

/* ======================
   响应式设计
====================== */
@media (max-width: 768px) {
  .md-typeset h1 {
    font-size: 2.8em;
    margin-bottom: 10px;
  }

  .flex-container {
    flex-direction: column;
  }

  .text-section, 
  .map-section {
    flex: 1 1 100%;
  }

  #map-container {
    height: 400px;
  }

  .section h3 {
    font-size: 1.5em;
  }
}

/* ======================
   原有样式保留
====================== */
.highlight {
  color: var(--md-typeset-a-color);
  font-weight: 600;
}

.emphasis {
  font-style: italic;
  color: var(--md-typeset-a-color);
}

.intro-meta {
  color: var(--md-typeset-a-color);
  font-weight: 600;
  position: relative;
  text-decoration: none;
}

.intro-meta::after {
  content: '';
  position: absolute;
  left: 0;
  bottom: -2px;
  width: 100%;
  height: 2px;
  background: #bfdbfe;
  transition: width 0.3s ease;
}

.intro-meta:hover::after {
  width: 0;
}
</style>

<div class="container">
  <div class="flex-container">
    <div class="text-section">
      <div class="section">
        <h3>关于我</h3>
        <p>
          <span class="intro-meta">计算机硕士 | esfj -> istj</span><br>
          专注于通过 <span class="highlight">GitHub</span> 构建个人知识体系，<br>
          追求学习过程的 <strong>可视化</strong> 与 <strong>系统化</strong>。<br>
          秉持「<span class="emphasis">知识流动促成长，记录沉淀筑认知</span>」理念，<br>
          希望通过技术博客 <a href="https://xiiiing.github.io" class="highlight">分享经验</a>，<br>
          连接更多 <span style="color: #22c55e; font-weight: 600;">同频创作者</span>。
        </p>
      </div>

      <div class="section">
        <h3>技术栈</h3>
        <ul>
          <li data-icon="💻"> 编程语言：Python、JavaScript、Java</li>
          <li data-icon="🛠️"> 工具链：Git、Nginx、GitHub Actions</li>
          <li data-icon="🌐"> 领域：计算机视觉、Web 开发、数据结构与算法</li>
        </ul>
      </div>

      <div class="section">
        <h3>兴趣爱好</h3>
        <ul>
          <li data-icon="🌍"> 地图收集与地理探索</li>
          <li data-icon="📚"> 技术博客写作与知识整理</li>
          <li data-icon="🎨"> 极简主义设计</li>
          <li data-icon="🏓"> 室内运动</li>
        </ul>
      </div>
    </div>

    <div class="map-section">
      <div class="map-wrapper">
        <div id="map-container"></div>
        <div class="map-overlay">
          <h4>求学轨迹地图</h4>
          <p>标记了我的教育旅程中重要的地理位置和经历</p>
        </div>
      </div>
    </div>
  </div>
</div>
