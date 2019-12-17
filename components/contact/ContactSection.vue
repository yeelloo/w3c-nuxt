<template>
  <div class="row">
    <div class="connect-us">
      <article>
        <h5>Have multiple projects or need a custom solution? </h5>
        <p>Let's discuss. Totally free review and quote.</p>
        <nuxt-link class="cta-small" to="/get-a-quote">Get a quote</nuxt-link>
      </article>
      <ul class="connect-social">
        <li><a href="https://www.facebook.com/Activeoo"><span class="icoov1" style="opacity: 0;">Facebook</span><span style="opacity: 0;"></span></a></li>
        <li><a href="https://www.twitter.com/activeooltd"><span class="icoov2" style="opacity: 0;">Twitter</span><span style="opacity: 0;"></span></a></li>
        <li><a href="skype:Activeoo?chat"><span class="icoov3" style="opacity: 0;">Skype</span><span style="opacity: 0;"></span></a></li>
      </ul>
      <article>
        <h5>Any question or want us to call you back?</h5>
        <p>Drop us a line at <a href="cdn-cgi/l/email-protection.html#b3dbd6dfdfdcf3d2d0c7dac5d6dcdc9dd0dcde">hello@activeoo.com</a> or</p>
        <a class="cta-small has-popup" href="#quick-connect-us">Send Message</a>
      </article>
    </div>
  </div>
</template>
<style>
.connect-us {
    display: grid;
    grid-template-columns: 1.5fr 1fr 1.5fr;
    gap: 20px;
    align-items: center;
    margin: 0 auto 80px auto;
    padding: 0 20px 0 20px;
    border-top: #dddedf 1px solid;
    border-bottom: #dddedf 1px solid;
}
.connect-us ul li {
    display: inline-block;
    width: 50px;
    height: 48px;
}
.connect-us ul li a {
    display: block;
    position: relative;
    width: 50px;
    height: 48px;
    background: url(~assets/images/interface/social-icon.png) 0 0 no-repeat;
}
.connect-us ul > li a:hover{
  background-position: 0 -49px;
}
.connect-us ul > li+li a{
  background-position: -49px 0;
}
.connect-us ul > li+li a:hover{
  background-position: -49px -49px;
}
.connect-us ul > li+li+li a{
  background-position: -98px 0;
}
.connect-us ul > li+li+li a:hover{
  background-position: -98px -49px;
}
.connect-us article {
    padding: 60px 0 60px 0;
    text-align: center;
}
.connect-us article h5 {
    font-size: 20px;
    line-height: 24px;
    padding-bottom: 15px;
    color: #1f2021;
    letter-spacing: -.04em;
}
.connect-us article p {
    display: block;
    padding-bottom: 22px;
}
.connect-us article p a {
    font-family: OpenSansBold;
}
@media only screen and (max-width: 959px){
  .connect-us{
    grid-template-columns: 1fr 1fr;
  }
  .connect-social{
    display: none;
  }
}
@media only screen and (max-width: 768px){
  .connect-us {
      grid-template-columns: auto;
      width: 100%;
      gap: 0;
  }
  .connect-social{
    display: block;
    border-top: #dddedf 1px solid;
    border-bottom: #dddedf 1px solid;
    padding: 30px 0 30px;
  }
}
</style>
