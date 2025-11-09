---
layout: default
title: 包装下单流程
permalink: /pages/packaging/
icon: fas fa-box
---

<!-- ✅ 页面顶部 Banner -->
<div class="media-banner">
  <img src="{{ '/assets/banner/packagingbanner.jpg' | relative_url }}" alt="Packaging Banner">
</div>

<div class="media-container">
  <!-- 进度条 -->
  <div class="process-progress">
    <div class="progress-bar"></div>
  </div>

  <div class="media-nav">
    <div class="nav-highlight"></div>
    <button class="nav-btn active" data-tab="phase1" data-color="#FF6B6B">前期准备</button>
    <button class="nav-btn" data-tab="phase2" data-color="#FFA94D">寻源与询价</button>
    <button class="nav-btn" data-tab="phase3" data-color="#FFD43B">决策与签约</button>
    <button class="nav-btn" data-tab="phase4" data-color="#51CF66">生产与跟单</button>
    <button class="nav-btn" data-tab="phase5" data-color="#339AF0">验收与结算</button>
  </div>

  <div class="tab-content">
    <!-- 阶段 1 -->
    <div id="phase1" class="tab-pane active">
      <div class="media-item"><span class="item-name">明确需求</span><span class="item-info">产品尺寸、材质、防护要求、数量、预算</span></div>
      <div class="media-item"><span class="item-name">设计文件准备</span><span class="item-info">结构设计、平面设计稿、刀模图、材质与工艺说明</span></div>
    </div>

    <!-- 阶段 2 -->
    <div id="phase2" class="tab-pane">
      <div class="media-item"><span class="item-name">寻找供应商</span><span class="item-info">渠道、能力评估、口碑、MOQ、地理位置</span></div>
      <div class="media-item"><span class="item-name">发送询价包 (RFQ)</span><span class="item-info">清晰需求说明、设计稿、样品要求</span></div>
    </div>

    <!-- 阶段 3 -->
    <div id="phase3" class="tab-pane">
      <div class="media-item"><span class="item-name">内部评审与供应商确定</span><span class="item-info">根据价格、质量、交期、服务选择供应商</span></div>
      <div class="media-item"><span class="item-name">签订合同或PO</span><span class="item-info">合同内容：金额、付款方式、交期、质量标准、样品确认</span></div>
    </div>

    <!-- 阶段 4 -->
    <div id="phase4" class="tab-pane">
      <div class="media-item"><span class="item-name">预付定金</span><span class="item-info">按合同支付定金，通知供应商生产</span></div>
      <div class="media-item"><span class="item-name">过程跟进</span><span class="item-info">产前会议、中期跟进、定期沟通</span></div>
    </div>

    <!-- 阶段 5 -->
    <div id="phase5" class="tab-pane">
      <div class="media-item"><span class="item-name">安排验货</span><span class="item-info">第三方或内部QC出具验货报告</span></div>
      <div class="media-item"><span class="item-name">尾款支付与物流安排</span><span class="item-info">验货通过后支付尾款并确认物流</span></div>
    </div>
  </div>
</div>

<style>
/* ✅ Banner 样式 */
.media-banner {
  position: relative;
  width: 100%;
  height: 240px;
  overflow: hidden;
  border-radius: 12px;
  margin-bottom: 2rem;
}
.media-banner img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  filter: brightness(0.85);
}

/* 主体布局 */
.media-container {
  max-width: 800px;
  margin: 0 auto;
}

/* 进度条样式 */
.process-progress {
  width: 100%;
  height: 6px;
  background: #e0e0e0;
  border-radius: 3px;
  margin-bottom: 1rem;
  overflow: hidden;
}
.progress-bar {
  height: 100%;
  width: 20%;
  background: #FF6B6B;
  transition: all 0.3s ease;
}

/* Tab 导航 */
.media-nav {
  position: relative;
  display: flex;
  justify-content: center;
  margin: 1rem 0 2rem;
  overflow-x: auto;
  white-space: nowrap;
  background: #f8f9fa;
  border-radius: 8px;
  padding: 8px;
}

.nav-btn {
  padding: 0.6rem 1.2rem;
  margin: 0 0.25rem;
  background: white;
  border: 1px solid #e0e0e0;
  cursor: pointer;
  font-size: 0.85rem;
  color: #666;
  border-radius: 6px;
  transition: all 0.3s ease;
  box-shadow: 0 1px 3px rgba(0,0,0,0.05);
  position: relative;
  z-index: 1;
}
.nav-btn.active {
  font-weight: 600;
}
.nav-highlight {
  position: absolute;
  bottom: 5px;
  height: 3px;
  background: linear-gradient(90deg, #000, #444);
  border-radius: 2px;
  transition: all 0.3s ease;
  z-index: 0;
}

/* Tab 内容 */
.tab-content {
  margin: 0 0 2rem;
}
.tab-pane { display: none; animation: fadeIn 0.3s ease; }
.tab-pane.active { display: block; }

@keyframes fadeIn { from { opacity: 0; } to { opacity: 1; } }

.media-item {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 1rem 0;
  border-bottom: 1px solid #f0f0f0;
  transition: background-color 0.3s ease;
}
.media-item:hover { background-color: #fafafa; }

.item-name { font-weight: 500; color: #333; }
.item-info { color: #666; font-size: 0.9rem; }

/* 响应式 */
@media (max-width: 768px) {
  .media-nav { justify-content: flex-start; padding: 6px; }
  .nav-btn { font-size: 0.8rem; padding: 0.4rem 0.8rem; }
  .media-container { padding: 0 10px; }
  .media-banner { height: 180px; }
}
</style>

<script>
document.addEventListener("pjax:complete", initMediaTabs);
document.addEventListener("DOMContentLoaded", initMediaTabs);

function initMediaTabs() {
  const navButtons = document.querySelectorAll(".nav-btn");
  const tabPanes = document.querySelectorAll(".tab-pane");
  const highlight = document.querySelector(".nav-highlight");
  const progressBar = document.querySelector(".progress-bar");
  if (!navButtons.length || !tabPanes.length || !highlight || !progressBar) return;

  navButtons.forEach(btn => {
    const newBtn = btn.cloneNode(true);
    btn.parentNode.replaceChild(newBtn, btn);
  });

  const newButtons = document.querySelectorAll(".nav-btn");

  const moveHighlight = (btn) => {
    const rect = btn.getBoundingClientRect();
    const containerRect = btn.parentElement.getBoundingClientRect();
    highlight.style.width = rect.width + "px";
    highlight.style.left = rect.left - containerRect.left + "px";

    // 更新进度条
    const index = Array.from(newButtons).indexOf(btn);
    const percent = ((index + 1) / newButtons.length) * 100;
    progressBar.style.width = percent + "%";
    progressBar.style.background = btn.dataset.color;
  };

  newButtons.forEach(button => {
    button.addEventListener("click", e => {
      e.preventDefault();
      const targetTab = button.getAttribute("data-tab");
      newButtons.forEach(b => b.classList.remove("active"));
      button.classList.add("active");

      tabPanes.forEach(p => p.classList.remove("active"));
      const targetPane = document.getElementById(targetTab);
      if (targetPane) targetPane.classList.add("active");
    
      moveHighlight(button);
    });
  });

  const activeButton = document.querySelector(".nav-btn.active") || newButtons[0];
  if (activeButton) moveHighlight(activeButton);
}
</script>