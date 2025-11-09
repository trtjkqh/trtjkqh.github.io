---
layout: default
title: 包装下单流程
permalink: /pages/packaging/
icon: fas fa-box
---

<div class="media-container">
  <div class="media-nav">
    <div class="nav-highlight"></div>
    <button class="nav-btn active" data-tab="stage1">前期准备</button>
    <button class="nav-btn" data-tab="stage2">设计准备</button>
    <button class="nav-btn" data-tab="stage3">供应商寻源</button>
    <button class="nav-btn" data-tab="stage4">合同签订</button>
    <button class="nav-btn" data-tab="stage5">生产跟单</button>
    <button class="nav-btn" data-tab="stage6">验收结算</button>
  </div>

  <div class="tab-content">
    <!-- 第一阶段 -->
    <div id="stage1" class="tab-pane active">
      <h3>前期准备与需求定义</h3>
      <ul>
        <li>明确产品信息：尺寸、重量、形状、易碎性、防潮、防震需求</li>
        <li>市场定位：包装风格（高端、环保、经济）</li>
        <li>预算管理：单件成本、总预算、设计打样、运输成本</li>
        <li>时间规划：倒推设计、打样、生产、物流节点</li>
        <li>数量规划：首次订单量及未来采购计划</li>
      </ul>
      <p><strong>风险项：</strong> 信息不完整、时间不合理、数量估算错误</p>
    </div>

    <!-- 第二阶段 -->
    <div id="stage2" class="tab-pane">
      <h3>设计与文件准备</h3>
      <ul>
        <li>结构设计：合理、保护性强、便于操作</li>
        <li>平面设计：矢量文件，出血3mm，CMYK模式，文字转曲</li>
        <li>标注材质和工艺要求（烫金、UV、专色等）</li>
        <li>提供刀模图（Die-line）</li>
        <li>内部评审：市场、销售、物流确认设计稿</li>
        <li>合规检查：食品信息、条码、环保标识</li>
      </ul>
      <p><strong>风险项：</strong> 设计稿不标准、法规信息缺失、未内部确认</p>
    </div>

    <!-- 第三阶段 -->
    <div id="stage3" class="tab-pane">
      <h3>供应商寻源与报价</h3>
      <ul>
        <li>渠道选择：展会、B2B 平台、朋友推荐、现有供应商</li>
        <li>筛选标准：专业领域、生产能力、质量口碑、MOQ、地理位置</li>
        <li>RFQ：需求说明、设计稿、刀模文件、材质工艺、样品要求</li>
        <li>样品评估：数字样确认内容颜色，实体样确认材质工艺尺寸</li>
        <li>多家报价对比，关注总成本、交期、服务</li>
      </ul>
      <p><strong>风险项：</strong> 样品不符合要求、沟通低效、隐性费用、MOQ不满足</p>
    </div>

    <!-- 第四阶段 -->
    <div id="stage4" class="tab-pane">
      <h3>决策与合同签订</h3>
      <ul>
        <li>内部评审综合选择供应商</li>
        <li>合同/PO 包含：产品描述、价格、付款方式、交货日期、质量标准、违约责任</li>
        <li>确认样作为大货验收标准</li>
      </ul>
      <p><strong>风险项：</strong> 付款方式不合理、合同条款不明确、未保留确认样</p>
    </div>

    <!-- 第五阶段 -->
    <div id="stage5" class="tab-pane">
      <h3>生产与跟单</h3>
      <ul>
        <li>支付定金，安排生产</li>
        <li>生产过程跟进：产前会议、生产中期验货、定期沟通</li>
        <li>大货样确认与确认样一致</li>
      </ul>
      <p><strong>风险项：</strong> 生产变更未确认、延迟或异常、不符合确认样</p>
    </div>

    <!-- 第六阶段 -->
    <div id="stage6" class="tab-pane">
      <h3>验收与结算</h3>
      <ul>
        <li>到厂/到货验货：抽样检查数量、外观、工艺、包装完整性</li>
        <li>尾款支付，确认物流信息</li>
        <li>仓库验收：抽检数量、外箱/内包装质量、色差、瑕疵</li>
        <li>归档合同、PO、设计稿、确认样、沟通记录</li>
      </ul>
      <p><strong>风险项：</strong> 到货问题未及时发现、仓库管理不当、发票金额错误</p>
    </div>
  </div>
</div>

<style>
.media-container {
  max-width: 800px;
  margin: 0 auto;
}

.media-nav {
  position: relative;
  display: flex;
  justify-content: center;
  margin: 2rem 0;
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
  position: relative;
  z-index: 1;
}

.nav-btn:hover {
  color: #111;
  background-color: #f3f3f3;
  transform: translateY(-1px);
  box-shadow: 0 2px 5px rgba(0,0,0,0.08);
}

.nav-btn.active {
  color: #000;
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

.tab-content {
  margin: 2rem 0;
  min-height: 400px;
}

.tab-pane {
  display: none;
  animation: fadeIn 0.3s ease;
}

.tab-pane.active {
  display: block;
}

@keyframes fadeIn {
  from { opacity: 0; }
  to { opacity: 1; }
}

.tab-pane ul {
  padding-left: 1.2rem;
}

.tab-pane li {
  margin-bottom: 0.5rem;
  line-height: 1.5;
}

@media (max-width: 768px) {
  .media-nav { justify-content: flex-start; padding: 6px; }
  .nav-btn { font-size: 0.8rem; padding: 0.4rem 0.8rem; }
  .media-container { padding: 0 10px; }
}
</style>

<script>
document.addEventListener("pjax:complete", initTabs);
document.addEventListener("DOMContentLoaded", initTabs);

function initTabs() {
  const navButtons = document.querySelectorAll(".nav-btn");
  const tabPanes = document.querySelectorAll(".tab-pane");
  const highlight = document.querySelector(".nav-highlight");
  if (!navButtons.length || !tabPanes.length || !highlight) return;

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