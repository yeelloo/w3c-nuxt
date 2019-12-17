<template>
  <footer>
        <div class="container">
          <div class="row">
            <div class="widget">
            <section class="">
                <h6>Stay tuned!</h6>
                <p>Subscribe for news &amp; special offers. <br>We don't spam.</p>
                <form action="#" method="get" name="newsletter">
                    <input type="text" name="email" onfocus="if(this.value=='Your Email') this.value='';" onblur="if(this.value=='') this.value='Your Email';" value="Your Email">
                    <button name="submit" type="submit">Subscribe</button>
                </form>
            </section>
            <section class="ft-connect">
                <h6>Contact</h6>
                <address>
                    10 Anson Road, #10-11<br>
                    International Plaza, Singapore 079903 </address>
                <ul>
                    <li><a href="https://www.facebook.com/w3codeMaster">Facebook</a></li>
                    <li><a href="https://www.twitter.com/w3codeMaster">Twitter</a></li>
                    <li><a href="skype:hangout14?chat">Skype</a></li>
                </ul>
            </section>
            <section class="">
                <h6>Company</h6>
                <ul>
                    <li><nuxt-link to="/our-work">Work</nuxt-link></li>
                    <li><nuxt-link to="/about">About w3codeMaster</nuxt-link></li>
                    <li><a href="about-us.html#how-we-do">How We Do</a></li>
                    <li><a href="faq.html">FAQ</a></li>
                    <li><a href="nda.html">NDA</a></li>
                </ul>
            </section>
            <section class="">
                <h6>Solutions</h6>
                <ul>
                    <li><a href="psd-to-html/index.html">PSD to HTML</a></li>
                    <li><a href="responsive-website/index.html">Responsive Website</a></li>
                    <li><a href="cms-integration/index.html">CMS Integration</a></li>
                    <li><a href="email-development/index.html">Email Development</a></li>
                    <li><a href="digital-banner-ads/index.html">Digital Banner Ads</a></li>
                </ul>
            </section>
            </div>
            </div>
        </div>
        <div class="container ft-bottom">
          <div class="row">
            <nuxt-link to="/terms-and-conditions">Terms &amp; Conditions</nuxt-link><span>&#8226;</span>
            <nuxt-link to="/privacy-policy">Privacy Policy</nuxt-link><span>&#8226;</span>&copy; {{CopyYear}} w3codeMaster
          </div>
        </div>
    </footer>
</template>

<script>
// import $ from 'jquery';
export default {
  data(){
    return{
      CopyYear : new Date().getFullYear()
    }
  },
  methods: {

  },
  mounted: () => {
    // var f = $("header > nav > ul").html();
    //   $(".overlay > nav > ul").html(f), $(".mMenu ul:first").append(f).promise().done(function() {
    //       $(".mMenu").html('<div class="mMenu-wrapper">' + $(".mMenu").html() + "</div>")
    //   });
      var g, h = $(".overlay"),
          i = h.height();
      h.removeClass("no-display").css({
          top: -i + "px"
      }), $("body").append('<div class="back-to-top no-display"><a href="javascript:void(0)">Back to top</a></div>');
      var j = $(".back-to-top");
      j.removeClass("no-display").css({
          opacity: 0
      }), $(window).scroll(function() {
          g && clearTimeout(g), g = setTimeout(function() {
              $(window).scrollTop() > 250 ? (h.css({
                  top: 0
              }), j.css({
                  opacity: 1
              })) : (h.css({
                  top: "-" + i + "px"
              }), j.css({
                  opacity: 0
              }))
          }, 250)
      }), $("html").on("click", ".back-to-top", function(a) {
          a.preventDefault(), $("html,body").animate({
              scrollTop: 0
          }, "slow", "easeInOutExpo")
      });
      var k = ".mMenu",
          l = "header .mico a, .mMenu mark a, .overlay .mico a";
      setTimeout(function() {
          $("body").addClass("push")
      }, 1e3), $(k).removeClass("no-display"), $(l).click(function(a) {
          $("body, .overlay").toggleClass("pushed"), $(k).toggleClass("push-reset")
      }),
      $(k).find("a").click(function() {
          return $(this).parent().children("ul").length > 0 ? ($(this).parent().toggleClass("selected"), !1) : void 0
      }),
      $(k).find(".close").click(function(a) {
          $("body, .overlay").removeClass("pushed"), $(k).removeClass("push-reset")
      }),
      $(".mMenu").on("click", "a, span", function(a) {
          var b = $(this).parent().find("ul");
          b.length > 0 && (a.stopPropagation(), b.stop().slideToggle("normal"))
      }),

      $(".s-scroll a, .s-paging a, .mMenuContact a, .back-to-top a, .ft-contact ul li a, .contact ul li a, .mico a, .mMenu mark a, .p2h-special section a, .rwd-interest figure a, .about-header-more, .mfp-close a, .about-header div > a").append("<span></span>").each(function() {
          var a = $("> span", this).css("opacity", 0);
          $(this).hover(function() {
              a.stop().fadeTo(10, 1)
          }, function() {
              a.stop().fadeTo(10, 0)
          })
      });
  }
}
</script>

<style>
footer {
    width: 100%;
    background-color: #0f0f0f;
    padding: 80px 0 60px 0;
}
.ft-bottom {
    display: block;
    clear: both;
    margin-top: 60px;
    padding-top: 50px;
    border-top: #292a2b 1px solid;
    text-align: center;
    font-size: 12px;
    color: #838485;
}
footer section {
    float: left;
    color: #838485;
}
.ft-subs {
    display: block;
    width: 400px;
}
footer h6 {
    color: #b5b6b7;
    height: 35px;
    text-transform: uppercase;
}
.ft-subs p {
    font-size: 13px;
    line-height: 17px;
    color: #838485;
    padding-bottom: 8px;
}
.ft-contact {
    display: block;
    width: 300px;
}
.ft-contact address {
    font-size: 13px;
    color: #838485;
    line-height: 22px;
}
.ft-contact a {
    font-size: 13px;
    color: #838485;
}
.ft-contact ul {
    padding-top: 20px;
}
.ft-contact ul li {
    display: block;
    float: left;
    position: relative;
    width: 34px;
    height: 32px;
}
.ft-contact ul li a {
    display: block;
    width: 34px;
    height: 32px;
    text-indent: -9999px;
    background: url(~assets/images/interface/social-icon.png) 0 -120px no-repeat;
}
.ft-contact ul li a span {
    display: block;
    position: absolute;
    width: 34px;
    height: 32px;
    top: 0;
    left: 0;
    padding: 0;
    background: url(~assets/images/interface/social-icon.png) 0 -153px no-repeat;
}
footer .widget {
  display: grid;
  grid-template-columns: 1.5fr 1fr 1fr 1fr;
  grid-gap: 15px;
  gap: 30px;
  -webkit-box-align: baseline;
  align-items: baseline;
  text-align: left;
  line-height: normal;
}
.back-to-top {
  position: fixed;
  bottom: 10%;
  right: 8%;
  width: 40px;
  height: 40px;
  z-index: 10;
}
.back-to-top a {
  display: block;
  position: relative;
  width: 50px;
  height: 50px;
  background: url(~assets/images/interface/go-top-bottom-icon.png) no-repeat 0 0;
  text-indent: -9999px;
}
.back-to-top a span {
    display: block;
    position: absolute;
    top: 0;
    left: 0;
    width: 50px;
    height: 50px;
    background: url(~assets/images/interface/go-top-bottom-icon.png) no-repeat 0 -52px;
    text-indent: -9999px;
    z-index: 10;
}
footer p {
    font-size: 13px;
    line-height: 17px;
    color: #838485;
    padding-bottom: 8px;
}
footer address {
    font-size: 13px;
    color: #838485;
    line-height: 22px;
}
.widget ul li a,
.widget ul li a strong {
    font-size: 12px;
    color: #838485;
}

.widget ul li a:hover,
.widget ul li a:hover strong {
    color: #fff;
}
.ft-bottom {
    display: block;
    clear: both;
    margin-top: 60px;
    padding-top: 50px;
    border-top: #292a2b 1px solid;
    text-align: center;
    font-size: 12px;
    color: #838485;
}
.ft-bottom a {
    font-size: 12px;
    color: #838485;
}
.ft-bottom span {
    display: inline-block;
    color: #838485;
    padding: 0 40px;
    font-size: 14px;
    font-family: OpenSansBold;
}
.container.ft-bottom > div {
    text-align: center;
    justify-content: center;
}
@media only screen and (max-width: 1024px){
  footer .widget{
    grid-template-columns: 1fr 1fr;
    width: 100%;
    grid-gap: 50px;
  }
  footer .widget section {
    position: relative;
    height: 100%;
  }
  footer .widget section:after{
    content: "";
    border-right: 1px dashed #3a3a3acc;
    position: absolute;
    right: -24px;
    height: 100%;
    top: 0;
    width: 0;
  }
  footer .widget section:nth-child(even):after {
    border-right: none;
  }
  footer .widget section:before {
    content: "";
    border-bottom: 1px dashed #3a3a3acc;
    position: absolute;
    left: 0;
    height: 0;
    bottom: -24px;
    width: 100%;
  }
  footer .widget section:nth-child(3)::before,
  footer .widget section:nth-child(4)::before{
    content: none;
  }
}
@media only screen and (max-width: 590px){
  .container.ft-bottom > div {
    display: block;
  }
  .ft-bottom span {
    display: block;
  }
}
@media only screen and (max-width: 424px){
  footer .widget {
    display: grid;
    grid-template-columns: 1fr;
  }
}
</style>

