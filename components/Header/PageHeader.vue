<template>
  <section class="in-header about-header page-header">
      <div class="container">
          <h2>Build. with<br>Care</h2>
      </div>
      <video id="vid" autoplay loop muted="muted" preload="auto">
          <source src="~/assets/images/page/video/codes.mp4" type="video/mp4">
      </video>
      <span class="s-scroll"><a href="javascript:void(0)">Scroll</a></span>
  </section>
</template>
<script>
export default {
  mounted: ()=>{
    $(".s-scroll a, .page-header div a").click(function(a) {
        $("html,body").animate({
            scrollTop: $(".home-haedline").offset().top - 70
        }, "slow", "easeInOutExpo")
    })
  }
}
</script>
<style>
.in-header.page-header{
  height: 80vh;
}
.page-header.about-header div {
    padding-top: 65%;
}

@media only screen and (min-width: 960px){
  .page-header.about-header div {
      padding-top: 220px;
  }
}
@media only screen and (max-width: 959px){
  .in-header.page-header {
      height: 60vh;
  }
  .page-header.about-header div {
      padding-top: 220px;
  }
}
@media only screen and (max-width: 559px){
  .page-header.about-header div h2{
    font-size: 52px;
    line-height: 55px;
  }
}
</style>
