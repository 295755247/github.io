---
layout: page
title: 主权指数测评
permalink: /assessment/
---

<style>
.assessment-form {
  max-width: 600px;
  margin: 0 auto;
}

.form-section {
  margin-bottom: 30px;
  padding: 20px;
  background: #f8f9fa;
  border-radius: 8px;
}

.form-section h3 {
  margin-bottom: 15px;
  color: #333;
}

.form-group {
  margin-bottom: 15px;
}

.form-group label {
  display: block;
  margin-bottom: 5px;
  font-weight: 500;
}

.form-group input {
  width: 100%;
  padding: 8px 12px;
  border: 1px solid #ddd;
  border-radius: 4px;
}

.submit-btn {
  background: #007bff;
  color: white;
  padding: 12px 30px;
  border: none;
  border-radius: 4px;
  font-size: 16px;
  cursor: pointer;
  width: 100%;
}

.submit-btn:hover {
  background: #0056b3;
}

.result-box {
  margin-top: 30px;
  padding: 20px;
  background: #e8f5e9;
  border-radius: 8px;
  display: none;
}

.score-display {
  font-size: 36px;
  font-weight: bold;
  color: #2e7d32;
  text-align: center;
}

.progress-bar {
  width: 100%;
  height: 20px;
  background: #e0e0e0;
  border-radius: 10px;
  margin: 20px 0;
  overflow: hidden;
}

.progress-fill {
  height: 100%;
  background: linear-gradient(90deg, #ff6b6b, #ffd93d, #6bcf7f);
  transition: width 1s ease;
}
</style>

<div class="assessment-form">
  <p>通过这个测评了解你当前的职业主权状态。测评包含12个问题，覆盖知识、决策、资产三个维度。</p>
  
  <form id="sovereigntyForm">
    <div class="form-section">
      <h3>📚 知识主权</h3>
      
      <div class="form-group">
        <label>1. 你的学习内容主要由谁决定？(0-25分)</label>
        <input type="range" name="k1" min="0" max="25" value="12" oninput="this.nextElementSibling.textContent = this.value">
        <span>12</span>
      </div>
      
      <div class="form-group">
        <label>2. 你是否有系统的知识管理方法？(0-25分)</label>
        <input type="range" name="k2" min="0" max="25" value="12" oninput="this.nextElementSibling.textContent = this.value">
        <span>12</span>
      </div>
      
      <div class="form-group">
        <label>3. 你的知识来源多样性如何？(0-25分)</label>
        <input type="range" name="k3" min="0" max="25" value="12" oninput="this.nextElementSibling.textContent = this.value">
        <span>12</span>
      </div>
      
      <div class="form-group">
        <label>4. 你的知识能影响多少人？(0-25分)</label>
        <input type="range" name="k4" min="0" max="25" value="12" oninput="this.nextElementSibling.textContent = this.value">
        <span>12</span>
      </div>
    </div>
    
    <div class="form-section">
      <h3>🎯 决策主权</h3>
      
      <div class="form-group">
        <label>5. 重要决定需要他人同意吗？(0-25分)</label>
        <input type="range" name="d1" min="0" max="25" value="12" oninput="this.nextElementSibling.textContent = this.value">
        <span>12</span>
      </div>
      
      <div class="form-group">
        <label>6. 你有清晰的决策框架吗？(0-25分)</label>
        <input type="range" name="d2" min="0" max="25" value="12" oninput="this.nextElementSibling.textContent = this.value">
        <span>12</span>
      </div>
      
      <div class="form-group">
        <label>7. 决策时考虑多元视角吗？(0-25分)</label>
        <input type="range" name="d3" min="0" max="25" value="12" oninput="this.nextElementSibling.textContent = this.value">
        <span>12</span>
      </div>
      
      <div class="form-group">
        <label>8. 你的决策能影响多少人？(0-25分)</label>
        <input type="range" name="d4" min="0" max="25" value="12" oninput="this.nextElementSibling.textContent = this.value">
        <span>12</span>
      </div>
    </div>
    
    <div class="form-section">
      <h3>💰 资产主权</h3>
      
      <div class="form-group">
        <label>9. 收入来源的自主性如何？(0-25分)</label>
        <input type="range" name="a1" min="0" max="25" value="12" oninput="this.nextElementSibling.textContent = this.value">
        <span>12</span>
      </div>
      
      <div class="form-group">
        <label>10. 是否有资产管理策略？(0-25分)</label>
        <input type="range" name="a2" min="0" max="25" value="12" oninput="this.nextElementSibling.textContent = this.value">
        <span>12</span>
      </div>
      
      <div class="form-group">
        <label>11. 资产的多样性如何？(0-25分)</label>
        <input type="range" name="a3" min="0" max="25" value="12" oninput="this.nextElementSibling.textContent = this.value">
        <span>12</span>
      </div>
      
      <div class="form-group">
        <label>12. 资产的影响力如何？(0-25分)</label>
        <input type="range" name="a4" min="0" max="25" value="12" oninput="this.nextElementSibling.textContent = this.value">
        <span>12</span>
      </div>
    </div>
    
    <button type="submit" class="submit-btn">计算我的主权指数</button>
  </form>
  
  <div id="result" class="result-box">
    <h2>你的主权指数</h2>
    <div class="score-display" id="finalScore">0</div>
    <div class="progress-bar">
      <div class="progress-fill" id="progressBar"></div>
    </div>
    <p id="scoreLevel"></p>
    <p id="scoreAdvice"></p>
    
    <h3>各维度得分</h3>
    <ul>
      <li>知识主权：<span id="knowledgeScore"></span>/100</li>
      <li>决策主权：<span id="decisionScore"></span>/100</li>
      <li>资产主权：<span id="assetScore"></span>/100</li>
    </ul>
  </div>
</div>

<script>
document.getElementById('sovereigntyForm').addEventListener('submit', function(e) {
  e.preventDefault();
  
  // 收集数据
  const formData = new FormData(this);
  let knowledge = 0, decision = 0, asset = 0;
  
  // 计算各维度得分
  for(let i = 1; i <= 4; i++) {
    knowledge += parseInt(formData.get('k' + i));
    decision += parseInt(formData.get('d' + i));
    asset += parseInt(formData.get('a' + i));
  }
  
  // 计算总分（简化版，未加入风险因子）
  const totalScore = Math.round((knowledge * 0.3 + decision * 0.4 + asset * 0.3));
  
  // 显示结果
  document.getElementById('finalScore').textContent = totalScore;
  document.getElementById('knowledgeScore').textContent = knowledge;
  document.getElementById('decisionScore').textContent = decision;
  document.getElementById('assetScore').textContent = asset;
  
  // 进度条
  document.getElementById('progressBar').style.width = totalScore + '%';
  
  // 评级
  let level, advice;
  if(totalScore < 30) {
    level = "依赖阶段";
    advice = "你目前高度依赖外部系统。建议：1）每天花30分钟学习新技能；2）尝试创建第一个数字产品；3）加入相关社群获得支持。";
  } else if(totalScore < 60) {
    level = "起步阶段";
    advice = "你已有主权意识。建议：1）建立个人知识管理系统；2）启动副业项目；3）每月增加一个收入来源。";
  } else if(totalScore < 80) {
    level = "运营阶段";
    advice = "你正在构建自己的系统。建议：1）优化并自动化现有流程；2）扩大影响力范围；3）帮助他人实现转型。";
  } else {
    level = "主权阶段";
    advice = "恭喜！你已实现较高的职业主权。考虑：1）分享你的经验；2）构建可传承的系统；3）探索更大的可能性。";
  }
  
  document.getElementById('scoreLevel').textContent = `当前阶段：${level}`;
  document.getElementById('scoreAdvice').textContent = advice;
  document.getElementById('result').style.display = 'block';
  
  // 滚动到结果
  document.getElementById('result').scrollIntoView({ behavior: 'smooth' });
});
</script>
