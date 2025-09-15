---
layout: default
---

<div class="profile-section">
  <div class="profile-image">
    <img src="{{ '/assets/images/profile.jpg' | relative_url }}" alt="胡慧琦" />
    <h2>胡慧琦</h2>
    <p><strong>{{ site.author.position }}</strong></p>
    <p>{{ site.author.department }}</p>
    <p>{{ site.author.institution }}</p>
    <p>📧 {{ site.author.email }}</p>
  </div>
  
  <div class="profile-info">
    <h2>个人简介</h2>
    <p>
      欢迎来到我的学术主页！我是一名计算机科学领域的研究者，专注于人工智能、机器学习和数据科学等前沿技术的研究与应用。
      我致力于通过创新的研究推动科技进步，并培养下一代优秀的科研人才。
    </p>
    
    <p>
      在我的学术生涯中，我主持和参与了多项国家级和省部级科研项目，在国际顶级期刊和会议上发表了多篇高质量论文。
      我相信科学研究的价值在于解决实际问题，推动社会进步。
    </p>

    <h3>研究兴趣</h3>
    <div class="skills-tags">
      <span class="skill-tag">人工智能</span>
      <span class="skill-tag">机器学习</span>
      <span class="skill-tag">深度学习</span>
      <span class="skill-tag">数据挖掘</span>
      <span class="skill-tag">计算机视觉</span>
      <span class="skill-tag">自然语言处理</span>
    </div>
  </div>
</div>

<div class="content-card">
  <h3>最新动态</h3>
  <ul class="item-list">
    <li>
      <div class="item-title">🎉 论文被 AAAI 2024 接收</div>
      <div class="item-meta">2024年1月</div>
      <p>我们关于多模态学习的最新研究成果被人工智能顶级会议 AAAI 2024 接收。</p>
    </li>
    <li>
      <div class="item-title">🏆 获得优秀青年科学基金</div>
      <div class="item-meta">2023年8月</div>
      <p>很荣幸获得国家自然科学基金优秀青年科学基金项目资助，将继续深入研究AI理论与应用。</p>
    </li>
    <li>
      <div class="item-title">👨‍🎓 指导学生获得最佳论文奖</div>
      <div class="item-meta">2023年6月</div>
      <p>指导的研究生在国际会议上获得最佳论文奖，为学校和实验室争得荣誉。</p>
    </li>
  </ul>
</div>

<div class="content-card">
  <h3>学术履历</h3>
  <ul class="item-list">
    <li>
      <div class="item-title">{{ site.author.position }}</div>
      <div class="item-meta">{{ site.author.institution }} | 2020年至今</div>
      <p>负责人工智能相关课程教学，主持多项科研项目，指导硕博研究生。</p>
    </li>
    <li>
      <div class="item-title">博士后研究员</div>
      <div class="item-meta">清华大学 | 2018-2020</div>
      <p>在计算机科学与技术系进行博士后研究，专注于深度学习理论与应用。</p>
    </li>
    <li>
      <div class="item-title">博士学位</div>
      <div class="item-meta">北京大学 | 2013-2018</div>
      <p>获得计算机科学与技术博士学位，研究方向为机器学习与数据挖掘。</p>
    </li>
  </ul>
</div>
