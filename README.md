<!-- 头部保留原始结构 -->
<!DOCTYPE html>
<html>
<head>
  <!-- 元标签和CSS链接（已调整顺序） -->
  <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
  <!-- 其他CSS -->
  <link type="text/css" rel="stylesheet" href="./BV澳门娱乐_files/chatStyle.css">
</head>
<body>
  <!-- 页面内容 -->

  <!-- 修正后的Swiper轮播（仅保留一个） -->
  <div class="ban swiper-container">
    <ul class="swiper-wrapper">
      <li class="swiper-slide"><img src="./BV澳门娱乐_files/1.jpg" alt=""></li>
      <li class="swiper-slide"><img src="./BV澳门娱乐_files/4.jpg" alt=""></li>
      <li class="swiper-slide"><img src="./BV澳门娱乐_files/2.jpg" alt=""></li>
    </ul>
  </div>

  <!-- 其他内容 -->

  <!-- 修正后的脚本加载 -->
  <script src="./BV澳门娱乐_files/jquery-1.11.1.min.js"></script>
  <script src="./BV澳门娱乐_files/swiper.min.js"></script>
  <script src="./BV澳门娱乐_files/cesu.js"></script>
  <script>
    // Swiper初始化
    var swiper = new Swiper('.swiper-container', {
      loop: true,
      autoplay: { delay: 3000 }
    });
  </script>
</body>
</html>
