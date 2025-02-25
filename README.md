<!DOCTYPE html>
<html>
<head>
<style>
.nav-control {
  position: fixed;
  top: 50%;
  right: 20px;
  transform: translateY(-50%);
  z-index: 999;
}

.nav-btn {
  display: block;
  width: 40px;
  height: 40px;
  margin: 15px 0;
  background: rgba(0,0,0,0.7);
  color: white;
  border: none;
  border-radius: 50%;
  cursor: pointer;
  transition: all 0.3s;
}

.nav-btn:hover {
  background: #4CAF50;
  transform: scale(1.1);
}

.page-container {
  display: none;
  padding: 80px 20px 60px;
}

.active-page {
  display: block;
  animation: fadeIn 0.5s;
}

@keyframes fadeIn {
  from { opacity: 0; }
  to { opacity: 1; }
}
</style>
</head>
<body>

<!-- 导航按钮 -->
<div class="nav-control">
  <button class="nav-btn" onclick="switchPage(-1)">↑</button>
  <button class="nav-btn" onclick="switchPage(1)">↓</button>
</div>

<!-- 页面容器 -->
<div id="page1" class="page-container active-page">
  <!-- 原页面内容 -->
  <div class="platform-header">页面1 - 飞天BV平台</div>
  <!-- 保持原有页面结构 -->
</div>

<div id="page2" class="page-container">
  <div class="platform-header">页面2 - 客服系统</div>
  <!-- 其他页面内容 -->
</div>

<div id="page3" class="page-container">
  <div class="platform-header">页面3 - 用户中心</div>
  <!-- 其他页面内容 -->
</div>

<script>
let currentPage = 1;
const totalPages = 3;

function switchPage(step) {
  const newPage = Math.max(1, Math.min(totalPages, currentPage + step));
  if(newPage === currentPage) return;
  
  document.getElementById(`page${currentPage}`).classList.remove('active-page');
  document.getElementById(`page${newPage}`).classList.add('active-page');
  currentPage = newPage;
  
  // 自动滚动到顶部
  window.scrollTo({ top: 0, behavior: 'smooth' });
}
</script>

</body>
</html>
 
