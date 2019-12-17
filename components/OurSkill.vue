<template>
  <div id="OurSkills">
    <!-- yellow_line start -->
    <section class="yellow_skill_line">
      <div class="container">
        <div class="col-xs-12">
          <p>Ready to discuss your project? <a href="#brif" onclick="ga('send', 'event', 'request', 'click_request')" data-toggle="modal" class="btn btn_black trans">Request a quote</a></p>
          <!-- [~~<p>Записей не найдено.</p>~~] -->
        </div>
      </div>
    </section>
    <!-- yellow_line end -->
    <section class="skills lilac">
      <div class="new-container clearfix">
          <h3 class="heading">Set of Skills</h3>
          <div class="col-md-6">
            <img src="~assets/images/home/web-tech.png" alt="web technologies">
          </div>
          <div class="col-md-6 text-center">
            <img src="~assets/images/home/mobile-tech.png" alt="mobile technologies">
          </div>
      </div>
    </section>
  </div>
</template>
<style>
.skills {
  color: #fff;
  padding: 32px 0;
  background: #5c2483;
}
.new-container {
  width: 90%;
  margin: 0 auto;
}
.skills .col-md-6{
  float: left;
}
.skills .heading {
  font-size: 54px;
  margin-bottom: 40px;
  text-align: center;
  text-transform: uppercase;
  color: #fff;
  line-height: initial;
}
.skills > img {
  transition: scale 350ms;
  -webkit-transition: all 350ms;
}
.skills > img:hover {
  transform: scale(1.1);
}
.yellow_skill_line {
    padding: 40px 0 36px;
    background: #fd0;
    text-align: center;
    margin-top: 20px;
}
.yellow_skill_line p {
    font-size: 24px;
    text-transform: uppercase;
    color: #000;
    font-family: AvgMedium;
    line-height: 2em;
    display: block;
}
.yellow_skill_line .btn {
    font-size: 19px;
    line-height: 2.2;
    margin-left: 10px;
    background: #660080;
    color: #fff;
    border-radius: 0;
    margin-top: -2px;
}
.yellow_skill_line .btn:hover,
.yellow_skill_line .btn:focus {
    color: #fd0;
    background: #000;
}
@media only screen and (max-width: 768px){
  .yellow_skill_line .btn{
    font-size: 15px;
  }
}
</style>
