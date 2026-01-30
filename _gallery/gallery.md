---
title: "Gallery"
collection: gallery
redirect_from: 
  - /gallery/
---

<!-- 引入 SimpleLightbox CSS & JS -->
<link href="https://cdn.jsdelivr.net/npm/simplelightbox@2.12.1/dist/simple-lightbox.min.css" rel="stylesheet">
<script src="https://cdn.jsdelivr.net/npm/simplelightbox@2.12.1/dist/simple-lightbox.min.js"></script>

<!-- 图片墙容器 -->
<div class="gallery" style="
  display: grid;
  grid-template-columns: repeat(2, 1fr); /* 每行3张图片，可改为4或2 */
  gap: 16px;
  justify-items: center;
  margin: 20px 0;
">

  <!-- 图片卡片示例 -->
  <div style="text-align:center; padding:8px; border:1px solid #ccc; border-radius:8px; background-color:#f9f9f9;">
    <a href="http://zlinaf.github.io/images/photo-groupdinner3.jpg" title="Group dinner1">
      <img src="http://zlinaf.github.io/images/photo-groupdinner3.jpg" style="width:200px; height:auto; object-fit:contain; border-radius:4px; box-shadow:0 4px 8px rgba(0,0,0,0.1);">
    </a>
    <div style="margin-top:8px; font-size:14px; color:#333; font-weight:bold;">Group dinner.</div>
  </div>

  <div style="text-align:center; padding:8px; border:1px solid #ccc; border-radius:8px; background-color:#f9f9f9;">
    <a href="http://zlinaf.github.io/images/photo-groupdinner1.jpg" title="Group dinner2">
      <img src="http://zlinaf.github.io/images/photo-groupdinner1.jpg" style="width:200px; height:auto; object-fit:contain; border-radius:4px; box-shadow:0 4px 8px rgba(0,0,0,0.1);">
    </a>
    <div style="margin-top:8px; font-size:14px; color:#333; font-weight:bold;">Group dinner.</div>
  </div>

  <div style="text-align:center; padding:8px; border:1px solid #ccc; border-radius:8px; background-color:#f9f9f9;">
    <a href="http://zlinaf.github.io/images/photo-visit1.jpg" title="groupvisit1">
      <img src="http://zlinaf.github.io/images/photo-visit1.jpg" style="width:200px; height:auto; object-fit:contain; border-radius:4px; box-shadow:0 4px 8px rgba(0,0,0,0.1);">
    </a>
    <div style="margin-top:8px; font-size:14px; color:#333; font-weight:bold;">Group visit at Huawei.</div>
  </div>

  <div style="text-align:center; padding:8px; border:1px solid #ccc; border-radius:8px; background-color:#f9f9f9;">
    <a href="http://zlinaf.github.io/images/photo-talk1.jpg" title="talk1">
      <img src="http://zlinaf.github.io/images/photo-talk1.jpg" style="width:200px; height:auto; object-fit:contain; border-radius:4px; box-shadow:0 4px 8px rgba(0,0,0,0.1);">
    </a>
    <div style="margin-top:8px; font-size:14px; color:#333; font-weight:bold;">Research talk at ISEDA 2025.</div>
  </div>

  <div style="text-align:center; padding:8px; border:1px solid #ccc; border-radius:8px; background-color:#f9f9f9;">
    <a href="http://zlinaf.github.io/images/photo-talk2.jpg" title="talk2">
      <img src="http://zlinaf.github.io/images/photo-talk2.jpg" style="width:200px; height:auto; object-fit:contain; border-radius:4px; box-shadow:0 4px 8px rgba(0,0,0,0.1);">
    </a>
    <div style="margin-top:8px; font-size:14px; color:#333; font-weight:bold;">Research talk at Huawei.</div>
  </div>

  <div style="text-align:center; padding:8px; border:1px solid #ccc; border-radius:8px; background-color:#f9f9f9;">
    <a href="http://zlinaf.github.io/images/photo-graduation2.jpg" title="graduation2">
      <img src="http://zlinaf.github.io/images/photo-graduation2.jpg" style="width:200px; height:auto; object-fit:contain; border-radius:4px; box-shadow:0 4px 8px rgba(0,0,0,0.1);">
    </a>
    <div style="margin-top:8px; font-size:14px; color:#333; font-weight:bold;">Sen Yan's undergraduate graduation.</div>
  </div>

  <div style="text-align:center; padding:8px; border:1px solid #ccc; border-radius:8px; background-color:#f9f9f9;">
    <a href="http://zlinaf.github.io/images/photo-graduation1.jpg" title="graduation1">
      <img src="http://zlinaf.github.io/images/photo-graduation1.jpg" style="width:200px; height:auto; object-fit:contain; border-radius:4px; box-shadow:0 4px 8px rgba(0,0,0,0.1);">
    </a>
    <div style="margin-top:8px; font-size:14px; color:#333; font-weight:bold;">Binghao Cheng's undergraduate graduation.</div>
  </div>

  <!-- 可以继续增加更多图片 -->
</div>

<!-- 初始化 Lightbox -->
<script>
  var lightbox = new SimpleLightbox('.gallery a', {
    captions: true,       // 显示标题
    captionDelay: 250,    // 延迟显示标题
  });
</script>

<!-- 响应式 -->
<style>
@media screen and (max-width: 1024px){
  .gallery { grid-template-columns: repeat(2, 1fr); }
}
@media screen and (max-width: 600px){
  .gallery { grid-template-columns: 1fr; }
}
</style>

