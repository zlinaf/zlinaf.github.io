---
title: "Gallery"
collection: gallery
permalink: /gallery/gallery
redirect_from: 
  - /gallery/
---

<!-- 引入 Glide.js CSS & JS -->
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/@glidejs/glide/dist/css/glide.core.min.css">
<script src="https://cdn.jsdelivr.net/npm/@glidejs/glide/dist/glide.min.js"></script>

<!-- 引入 SimpleLightbox CSS & JS -->
<link href="https://cdn.jsdelivr.net/npm/simplelightbox@2.12.1/dist/simple-lightbox.min.css" rel="stylesheet">
<script src="https://cdn.jsdelivr.net/npm/simplelightbox@2.12.1/dist/simple-lightbox.min.js"></script>

<!-- 轮播容器 -->
<div class="glide" style="max-width:800px; margin:0 auto;">
  <div class="glide__track" data-glide-el="track">
    <ul class="glide__slides">

      <!-- 图片卡片循环生成 -->
      <!-- 格式：<li class="glide__slide"> <a href="大图URL" title="标题"> <img src="缩略图URL"> </a> <div>说明</div> </li> -->

      <li class="glide__slide" style="text-align:center;">
        <a href="http://zlinaf.github.io/images/photo-groupdinner2026-1.jpg" title="Group dinner2026-1">
          <img src="http://zlinaf.github.io/images/photo-groupdinner2026-1.jpg" style="width:100%; max-height:900px; height:auto; object-fit:contain; border-radius:4px; box-shadow:0 4px 8px rgba(0,0,0,0.1);">
        </a>
        <div style="margin-top:8px; font-size:14px; color:#333; font-weight:bold;">Group dinner at Spring 2026.</div>
      </li>

      <li class="glide__slide" style="text-align:center;">
        <a href="http://zlinaf.github.io/images/photo-groupdinner3.jpg" title="Group dinner1">
          <img src="http://zlinaf.github.io/images/photo-groupdinner3.jpg" style="width:100%; max-height:900px; height:auto; object-fit:contain; border-radius:4px; box-shadow:0 4px 8px rgba(0,0,0,0.1);">
        </a>
        <div style="margin-top:8px; font-size:14px; color:#333; font-weight:bold;">Group dinner at Winter 2025.</div>
      </li>

      <li class="glide__slide" style="text-align:center;">
        <a href="http://zlinaf.github.io/images/photo-groupdinner1.jpg" title="Group dinner2">
          <img src="http://zlinaf.github.io/images/photo-groupdinner1.jpg" style="width:100%; max-height:900px; height:auto; object-fit:contain; border-radius:4px; box-shadow:0 4px 8px rgba(0,0,0,0.1);">
        </a>
        <div style="margin-top:8px; font-size:14px; color:#333; font-weight:bold;">Group dinner at Summer 2025.</div>
      </li>

      <li class="glide__slide" style="text-align:center;">
        <a href="http://zlinaf.github.io/images/photo-visit1.jpg" title="groupvisit1">
          <img src="http://zlinaf.github.io/images/photo-visit1.jpg" style="width:100%; max-height:900px; height:auto; object-fit:contain; border-radius:4px; box-shadow:0 4px 8px rgba(0,0,0,0.1);">
        </a>
        <div style="margin-top:8px; font-size:14px; color:#333; font-weight:bold;">Group visit at Huawei.</div>
      </li>

      <li class="glide__slide" style="text-align:center;">
        <a href="http://zlinaf.github.io/images/photo-talk1.jpg" title="talk1">
          <img src="http://zlinaf.github.io/images/photo-talk1.jpg" style="width:100%; max-height:900px; height:auto; object-fit:contain; border-radius:4px; box-shadow:0 4px 8px rgba(0,0,0,0.1);">
        </a>
        <div style="margin-top:8px; font-size:14px; color:#333; font-weight:bold;">Research talk at ISEDA 2025.</div>
      </li>

      <li class="glide__slide" style="text-align:center;">
        <a href="http://zlinaf.github.io/images/photo-talk2.jpg" title="talk2">
          <img src="http://zlinaf.github.io/images/photo-talk2.jpg" style="width:100%; max-height:900px; height:auto; object-fit:contain; border-radius:4px; box-shadow:0 4px 8px rgba(0,0,0,0.1);">
        </a>
        <div style="margin-top:8px; font-size:14px; color:#333; font-weight:bold;">Research talk at Huawei.</div>
      </li>

      <li class="glide__slide" style="text-align:center;">
        <a href="http://zlinaf.github.io/images/photo-graduation2.jpg" title="graduation2">
          <img src="http://zlinaf.github.io/images/photo-graduation2.jpg" style="width:100%; max-height:900px; height:auto; object-fit:contain; border-radius:4px; box-shadow:0 4px 8px rgba(0,0,0,0.1);">
        </a>
        <div style="margin-top:8px; font-size:14px; color:#333; font-weight:bold;">Sen Yan's undergraduate ceremony.</div>
      </li>

      <li class="glide__slide" style="text-align:center;">
        <a href="http://zlinaf.github.io/images/photo-graduation1.jpg" title="graduation1">
          <img src="http://zlinaf.github.io/images/photo-graduation1.jpg" style="width:100%; max-height:900px; height:auto; object-fit:contain; border-radius:4px; box-shadow:0 4px 8px rgba(0,0,0,0.1);">
        </a>
        <div style="margin-top:8px; font-size:14px; color:#333; font-weight:bold;">Binghao Cheng's undergraduate ceremony.</div>
      </li>

      <!-- 可继续添加更多图片 -->
    </ul>
  </div>

  <!-- 左右箭头 -->
  <div class="glide__arrows" data-glide-el="controls">
    <button class="glide__arrow glide__arrow--left" data-glide-dir="<">◀</button>
    <button class="glide__arrow glide__arrow--right" data-glide-dir=">">▶</button>
  </div>

  <!-- 圆点导航（可选） -->
  <div class="glide__bullets" data-glide-el="controls[nav]">
    <button class="glide__bullet" data-glide-dir="=0"></button>
    <button class="glide__bullet" data-glide-dir="=1"></button>
    <button class="glide__bullet" data-glide-dir="=2"></button>
  </div>
</div>

<!-- 初始化轮播和 Lightbox -->
<script>
  // Glide.js 初始化
  new Glide('.glide', {
    type: 'carousel',
    perView: 1,
    focusAt: 'center',
    gap: 16
  }).mount();

  // Lightbox 初始化
  var lightbox = new SimpleLightbox('.glide__slide a', {
  captions: true,
  captionDelay: 250,
  close: true,
  nav: true,
  overlay: true,
  scrollZoom: false // 防止 Lightbox 弹出时滚动跳动
  });

</script>

<!-- 响应式 -->
<style>
@media screen and (max-width: 768px){
  .glide { max-width: 90%; }
}
@media screen and (max-width: 480px){
  .glide { max-width: 100%; }
}
</style>
