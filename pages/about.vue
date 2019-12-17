<template>
  <div>
    <HomeHeader />
    <div class="container">
      <div class="row">
        <section class="home-haedline" style="margin-bottom:60px;">
          <h2>About <span>W</span>3<span>C</span>ode<span>M</span>aster</h2>
          <div>
              <p>
                  <br>
                  We are a digital production studio providing tailored services to the international clients. At Activeoo, we keep the passion for excellence at the core and blend powerful creative ideas with superior digital technologies to activate the brands.
                  <br><br>
                  We work with advertising agencies, companies, startup businesses and freelancers to assist in delivering digital creation, adaptation and localization solutions. We believe in simplicity and work in partnership with clients to ensure cost efficient, inspiring digital solutions that people want to share and engage with.
              </p>
          </div>
        </section>
      </div>
      <div class="row">
        <section class="home-haedline" style="margin-bottom: 30px;padding-top: 0px;">
          <h2>People who Matters</h2>
        </section>
        <ul class="people-list">
          <b-row>
            <b-col>
              <span class="img_item">
                <img src="~assets/images/about-us/team/masud-rana.jpg" alt="masud rana">
              </span>
              <span class="name">Masud Rana</span>
              <span class="job">Head of JavaScript</span>
            </b-col>
            <b-col>
              <span class="img_item">
                <img src="~assets/images/about-us/team/ikbal.jpg" alt="Marshall Ikbal">
              </span>
              <span class="name">Marshall Ikbal</span>
              <span class="job">Head of PHP</span>
            </b-col>
            <b-col>
              <span class="img_item">
                <img src="~assets/images/about-us/team/hasan.jpg" alt="Hasan Manik">
              </span>
              <span class="name">Hasan Manik</span>
              <span class="job">Head of Design</span>
            </b-col>
            <b-col>
              <span class="img_item">
                <img src="~assets/images/about-us/team/bakul.jpg" alt="Bakul Sinha">
              </span>
              <span class="name">Bakul Sinha</span>
              <span class="job">Head of UX</span>
            </b-col>
          </b-row>
        </ul>
      </div>
      <ContactSection />
    </div>

  </div>
</template>

<script>
import Logo from '~/components/Logo.vue'
import HomeHeader from '~/components/Header/HomeHeader.vue'
import ContactSection from '~/components/Contact/ContactSection.vue'

export default {
  components: {
    Logo, HomeHeader, ContactSection
  },
  methods: {
    initials() {

    }
  },
  mounted: () => {
    $('body.pushed .closeMenu').trigger('click');
  },
  created(){
    this.initials();
  }
}
</script>

<style>
.home-haedline span {
    color: #ffcb05;
    font-family: AvgBold;
}
ul.people-list {
    margin-bottom: 60px;
}
.people-list .img_item {
    text-align: center;
    display: block;
}
.people-list .img_item > img {
    border-radius: 50%;
    max-width: 75%;
    box-shadow: 0px 0px 2px #c3c3c3;
}
.people-list span {
    display: block;
}
.people-list span.name {
    font-weight: 600;
    color: #1f2021;
}
@media only screen and (max-width: 768px){
  ul.people-list > .row {
      display: block;
  }
  .people-list .col {
      width: 50%;
      float: left;
      margin-bottom: 25px;
  }
}
</style>
