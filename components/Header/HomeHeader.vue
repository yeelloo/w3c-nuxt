<template>
  <section class="in-header about-header home-header">
      <div class="container">
          <h2>Mastering.<br>Innovation</h2>
          <p>A bunch of production and marketing specialists helping brands to activate and amplify the digital communications with maximum cost efficiencies.</p>
          <a href="javascript:void(0)">Learn more</a>
      </div>
      <video id="vid" autoplay loop muted="muted" preload="auto">
          <source src="~/assets/images/home/video/blue.mp4" type="video/mp4">
      </video>
      <span class="s-scroll"><a href="javascript:void(0)">Scroll</a></span>
  </section>
</template>
<script>
export default {
  mounted: ()=>{
    $(".s-scroll a, .about-header div a").click(function(a) {
        $("html,body").animate({
            scrollTop: $(".home-haedline").offset().top - 70
        }, "slow", "easeInOutExpo")
    })
  }
}
</script>
<style>
.in-header {
    display: block;
    position: relative;
    width: 100%;
    height: 600px;
    overflow: hidden;
    max-width: 1920px;
    margin: 0 auto;
}
.about-header {
    position: relative;
    background: #0f1011;
    height: 100vh;
    max-height: 1075px;
    max-width: 1920px;
    margin: 0 auto;
}
.about-header:after {
    content: "";
    position: absolute;
    left: 0;
    top: 0;
    z-index: 9;
    width: 100%;
    height: 100%;
    background: url(~assets/images/about-us/overlay-pattern.png) repeat;
}
.in-header div {
    display: block;
    position: relative;
    padding-top: 263px;
    text-align: center;
}
.about-header div {
    position: relative;
    z-index: 10;
    padding-top: 338px;
}
.s-scroll {
    display: block;
    position: absolute;
    bottom: 0;
    z-index: 10;
    width: 100%;
    text-align: center;
}
.in-header div h2 {
    font-size: 60px;
    line-height: 60px;
    font-weight: bolder;
    letter-spacing: -.05em;
    padding: 0 0 17px 0;
    color: #fff;
    width: 90%;
    margin: auto;
}
.about-header div h2 {
    color: #fcc113;
    font-size: 90px;
    line-height: 90px;
    font-weight: bolder;
    letter-spacing: -.05em;
}
.in-header video {
    position: absolute;
    left: 50%;
    top: 50%;
    z-index: 1;
    min-height: 100%;
    min-width: 100%;
    -webkit-transform: translate(-50%,-50%);
    -ms-transform: translate(-50%,-50%);
    transform: translate(-50%,-50%);
}
.in-header div p {
    font-family: AvgLight;
    font-size: 16px;
    line-height: 24px;
    width: 80%;
    margin: auto;
}
.about-header div p {
    color: #fff;
    font-size: 18px;
    line-height: 24px;
    padding: 29px 0 37px;
}
.about-header div>a {
    font-family: AvgMedium;
    font-size: 14px;
    line-height: 24px;
    letter-spacing: .05em;
    text-decoration: underline;
    text-transform: uppercase;
    display: inline-block;
    color: #fff;
}
.s-scroll a {
    display: inline-block;
    margin-right: -5px;
    width: 120px;
    height: 50px;
    background: url(~assets/images/interface/slider-icon.png) 0 -100px no-repeat;
    text-indent: -9999px;
}
.s-scroll a span {
    display: block;
    position: absolute;
    top: 0;
    width: 70px;
    height: 70px;
    background: url(~assets/images/interface/slider-icon.png) 0 -160px no-repeat;
}
@media only screen and (max-width: 991px){
  header {
      max-width: 720px;
  }
  header h1 a {
      width: 90px;
      background: url(~assets/images/interface/activeoo-logo.png) -237px top no-repeat;
  }
}
@media only screen and (max-width: 980px){
  header {
      max-width: 530px;
      width: 74%;
  }

}
@media only screen and (max-width: 959px){
  .about-header div h2 {
      font-size: 75px;
      line-height: 75px;
  }
}
@media only screen and (max-width: 599px){
  header {
    width: 82%;
  }
}
</style>
