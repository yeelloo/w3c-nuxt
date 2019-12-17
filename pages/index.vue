<template>
  <div>
    <HomeHeader />
    <div class="container">
      <section class="home-haedline">
        <h2>Production Simplified</h2>
        <p>At Activeoo, we are committed to take off the workload from your marketing, creative team by providing high quality, cost effective digital production solutions that help to activate your brand.</p>
      </section>
      <!--  -->
      <div class="home-production row">
        <span>Our Digital Production Solutions</span>
        <section style="grid-area: fnd">
            <figure></figure>
            <h3>Frontend <br>Development</h3>
            <p>We offer a wide range of frontend solutions with premium quality and pixel-precision at the core.</p>
            <ul>
                <li>PSD To HTML + CSS</li>
                <li>Responsive &amp; Mobile</li>
                <li>Git, Version Control</li>
                <li>AngularJs / VueJs / ReactJs</li>
                <li>API Integration</li>
                <li>Landing Page</li>
            </ul>
            <nuxt-link class="cta-small" to="/solutions/frontend-development">LEARN MORE</nuxt-link>
        </section>
        <section style="grid-area: bnd">
            <figure></figure>
            <h3>CMS <br>Integration</h3>
            <p>Looking for a professional team to implement your design in popular CMS that functions seamlessly?</p>
            <ul>
                <li>WordPress</li>
                <li>Umbraco</li>
                <li>BlogEngine.NET</li>
                <li>Magento</li>
                <li>Theme Customization</li>
                <li>Build Custom CSM</li>
            </ul>

            <nuxt-link class="cta-small" to="/solutions/cms-integration">LEARN MORE</nuxt-link>
        </section>
        <section style="grid-area: cnd">
            <figure></figure>
            <h3>Software <br>Development</h3>
            <p>Turn your ideas into reality, Trun daily problems into affordable solution across plutforms (Win, Mac, IoT)</p>
            <ul>
                <li>ES6 +</li>
                <li>NPM</li>
                <li>ElectronJs</li>
                <li>MAC</li>
                <li>Windows 10</li>
                <li>IoT, Raspberry Pi </li>
            </ul>

            <nuxt-link class="cta-small" to="/solutions/software-development">LEARN MORE</nuxt-link>
        </section>
        <section style="grid-area: dnd">
            <figure></figure>
            <h3>Digital <br>Banner Ads</h3>
            <p>Whether you need HTML5 or Flash banner, we can help you at any stage of the development process.</p>
            <ul>
                <li>DoubleClick</li>
                <li>MediaMind</li>
                <li>Standard &amp; Rich Media</li>
                <li>Creative Development</li>
                <li>HTML5 Banners</li>
                <li>Resizing &amp; Adaptation</li>
            </ul>
            <nuxt-link class="cta-small" target="_blank" to="/solutions/banner">LEARN MORE</nuxt-link>
        </section>
      </div>
    </div>
    <OurSkill />
    <!-- <div class="container">
      <ContactSection />
    </div> -->
  </div>
</template>

<script>
import Logo from '~/components/Logo.vue'
import HomeHeader from '~/components/Header/HomeHeader.vue'
import ContactSection from '~/components/Contact/ContactSection.vue'
import OurSkill from '~/components/OurSkill.vue'

export default {
  components: {
    Logo, HomeHeader, ContactSection, OurSkill
  },
  methods: {
    initials:function() {

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
.home-haedline {
    margin: 0 auto;
    padding: 74px 0 0 0;
}
.home-haedline h2,
.home-haedline span {
    padding: 0 0 18px 0;
    font-size: 48px;
    line-height: 48px;
    text-align: center;
    letter-spacing: -.04em;
}
.home-haedline p {
    padding: 0;
    text-align: center;
}
.home-production {
    padding: 40px 0 40px 0;
}
.home-production span {
    display: block;
    padding: 0 0 30px 0;
    font-family: AvgBold;
    font-size: 20px;
    line-height: 20px;
    text-align: center;
    color: #96999c;
}
.home-production section {
    padding: 45px 20px 40px;
    background-color: #eaebec;
    border-radius: 3px;
    -webkit-border-radius: 3px;
    -moz-border-radius: 3px;
    box-shadow: 0 2px 0 0 #c8c8c8;
    -webkit-box-shadow: 0 2px 0 0 #c8c8c8;
    -moz-box-shadow: 0 2px 0 0 #c8c8c8;
}
.home-production section figure {
    display: block;
    width: 60px;
    height: 60px;
    margin: 0 auto;
    background: url(~assets/images/home/solutions-icon.png) 0 0 no-repeat;
}
.home-production section h3 {
    padding: 22px 0 17px 0;
    text-align: center;
    font-size: 20px;
    letter-spacing: -.04em;
}
.home-production section p {
    display: block;
    text-align: center;
    line-height: 18px;
}
.home-production section ul {
    display: block;
    margin: 18px 15px 28px 15px;
    border-bottom: #d1d2d3 1px solid;
}
.home-production section ul li {
    display: block;
    border-top: #d1d2d3 1px solid;
    padding: 8px 0;
    text-align: center;
    line-height: 18px;
}
.home-production section a {
    margin: 0 auto;
    border: #959697 1px solid;
    background-color: transparent;
    color: #222324;
}
.home-production{
  display: grid;
  grid-template-areas:
    'header header header header'
    'fnd bnd cnd dnd';
  grid-gap: 10px;
}
.home-production > span{
  grid-area: header;
}
.home-production > section{
  /* grid-area: prod; */
}
.home-production section:active,
.home-production section:hover {
    background-color: #ffcb05;
}
.home-production section:hover,
.home-production section:hover b,
.home-production section:hover h3,
.home-production section:hover p,
.home-production section:hover strong {
    color: #fff;
}
.home-production section:hover ul {
    color: #fff;
    border-bottom: #fff 1px solid;
}
.home-production section:hover ul li {
    color: #fff;
    border-top: #fff 1px solid;
}
.home-production section+section figure {
    background-position: -60px 0;
}
.home-production section+section+section figure {
    background-position: -137px 0;
}
.home-production section+section+section+section figure {
    background-position: -200px 0;
}
@media only screen and (max-width: 980px){
  .home-haedline {
      width: 95%;
  }
  .home-production {
    display: grid;
    grid-template-areas:
      'header header header header'
      'fnd fnd bnd bnd'
      'cnd cnd dnd dnd';
    grid-gap: 20px;
    margin-bottom: 40px;
  }
  .home-production section {

  }
  .home-production section p, .home-production section ul li {
      font-size: 13px;
  }
  .home-production section p, .home-production section ul li {
      font-size: 13px;
  }
}
@media only screen and (max-width: 959px){

}
@media only screen and (max-width: 559px){
  .home-production {
    display: block;
    grid-template-areas: none;
    grid-gap: 10px;
  }
  .home-production section{
    margin-bottom: 15px;
  }
}
</style>
