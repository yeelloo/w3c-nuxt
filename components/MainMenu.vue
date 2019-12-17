<template>
  <div class="main-nav">
    <section class="container">
        <header>
            <h1><nuxt-link to="/">w3CodeMaster - Digital Production Agency. API, Software, IoT, CMS Integration, Laravel, NodeJs, AngularJs, VueJs, ReactJs, WordPress, Digital Banner Ads</nuxt-link></h1>
            <nav>
                <MainMenuItems />
            </nav>
            <span class="mico"><a href="javascript:void(0)">Menu</a></span>
        </header>
    </section>


    <div class="overlay">
        <nav>
            <figure><nuxt-link to="/">w3CodeMaster</nuxt-link></figure>
            <MainMenuItems />
        </nav>
        <span class="mico"><a href="javascript:void(0)">Menu</a></span>
    </div>


    <div class="mMenu no-display">
      <div class="mMenu-wrapper">
        <mark><a class="closeMenu" href="javascript:void(0)">Close</a></mark>
        <figure><nuxt-link to="/">w3codeMaster</nuxt-link></figure>
        <MainMenuItems />
        <div class="mMenuContact clearfix">
            <p class="clearfix"><i><a href="https://www.facebook.com/Activeoo">Facebook</a></i><i><a href="https://www.twitter.com/activeooltd">Twitter</a></i><i><a href="skype:Activeoo?chat">Skype</a></i></p>
            <address>10 Anson Road, #10-11<br>International Plaza, Singapore 079903</address>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import MainMenuItems from "~/components/MainMenuItems"
export default {
  components:{
    MainMenuItems
  },
  data(){
    return{

    }
  },
  methods: {
    inits:function(){

    }
  },
  created(){
      this.inits();
  }
}
</script>

<style>
.container{
  padding-top: 0%;
}
.overlay {
    position: fixed;
    top: 0;
    left: 0;
    z-index: 1000;
    width: 100%;
    height: 70px;
    background: #0c0c09;
    background: rgba(0,0,0,.9);
}

header h1 a {
  display: block;
  float: left;
  width: 237px;
  height: 40px;
  margin: 15px 0 0 20px;
  text-indent: -9999px;
  background: url(~assets/images/interface/activeoo-logo.png) left top no-repeat
}

.mico {
  display: none
}

.mico a {
  display: block;
  float: right;
  position: relative;
  width: 27px;
  height: 21px;
  margin: 27px 20px 0 0;
  text-indent: -9999px;
  background: url(~assets/images/interface/nav-drop-down-close-icon.png) 0 -50px no-repeat
}

.mico a span {
  display: block;
  position: absolute;
  top: 0;
  width: 27px;
  height: 21px;
  background: url(~assets/images/interface/nav-drop-down-close-icon.png) 0 -74px no-repeat
}

nav {
  float: right;
  margin: 0 16px 0 0
}

nav ul li {
  float: left;
  position: relative;
  height: 70px
}

nav ul li:hover,
nav ul li:hover span {
  background-color: #e7e8e9
}

nav ul li a:link,
nav ul li a:visited,
nav ul li span {
  display: block;
  height: 38px;
  padding: 32px 20px 0;
  line-height: 13px;
  text-transform: uppercase;
  color: #2f3338;
  font-family: AvgMedium;
  font-size: 12px;
  box-sizing: content-box;
}

nav ul li a:active,
nav ul li a:hover,
nav ul li:hover span {
  text-decoration: none;
  color: #ef4123
}

nav>ul>li span,
nav>ul>li+li+li span {
  padding-right: 26px
}

nav>ul>li span:before,
nav>ul>li+li+li span:before {
  background: url(~assets/images/interface/nav-drop-down-icon.png) 0 0 no-repeat;
  cursor: default;
  width: 7px;
  height: 5px;
  content: "";
  position: absolute;
  right: 15px;
  top: 38px
}

nav>ul>li:nth-child(4)>a {
  color: #ef4123;
  font-family: AvgBold
}

nav>ul>li:nth-child(4)>a:hover {
  background-color: #ef4123;
  color: #fff !important
}

header .nav-select,
header .nav-select:hover {
  background-color: #fff;
  color: #464b50 !important
}

nav ul li div {
  display: none;
  position: absolute;
  top: 70px;
  left: -38px;
  width: 190px;
  background: url(~assets/images/interface/nav-drop-down-icon.png) 82px -80px no-repeat;
  padding-top: 7px
}

nav ul li:hover div {
  display: block
}

nav ul li div ul {
  background-color: #e7e8e9;
  padding: 15px 20px;
  -webkit-border-radius: 3px;
  -moz-border-radius: 3px;
  border-radius: 3px
}

nav ul li div ul li {
  display: block;
  float: none;
  height: auto;
  border-bottom: #fff 1px solid
}

nav ul li div ul li:last-child {
  border-bottom: none
}

nav ul li div ul li a:link,
nav ul li div ul li a:visited {
  display: block;
  height: auto;
  color: #000;
  padding: 13px 5px 11px 5px;
  font-family: AvgMedium;
  text-transform: none
}

nav ul li div ul li a:active,
nav ul li div ul li a:hover {
  color: #ef4123;
  text-decoration: none;
  background-color: #fff
}

.overlay {
  position: fixed;
  top: 0;
  left: 0;
  z-index: 1000;
  width: 100%;
  height: 70px;
  background: #0c0c09;
  background: rgba(0, 0, 0, .9)
}

.overlay nav {
  float: none;
  width: 980px;
  margin: 0 auto;
  max-width: 100%
}

.overlay nav figure a {
  display: block;
  float: left;
  width: 236px;
  height: 40px;
  margin: 15px 0 0 20px;
  text-indent: -9999px;
  background: url(~assets/images/interface/activeoo-logo.png) 0 -43px no-repeat;
}

.overlay nav ul {
  float: right
}

.overlay>nav>ul>li {
  height: 70px
}

.overlay>nav>ul>li>a,
.overlay>nav>ul>li>span {
  height: 40px;
  padding: 30px 15px 0 15px;
  color: #b5b6b7
}

.overlay>nav>ul>li span,
.overlay>nav>ul>li+li+li span {
  padding-right: 26px
}

.overlay>nav>ul>li.nav-select>a,
.overlay>nav>ul>li>span.nav-select {
  color: #fff;
  background-color: rgba(255, 255, 255, .15)
}

.overlay>nav>ul>li a:hover,
.overlay>nav>ul>li:hover>span {
  color: #ef4123
}

.overlay>nav>ul>li span:before,
.overlay>nav>ul>li+li+li span:before {
  top: 36px
}

.overlay>nav>ul>li span,
.overlay>nav>ul>li+li+li span {
  cursor: default
}

.overlay>nav>ul>li:nth-child(4) a {
  color: #ef4123
}

.overlay>nav>ul>li:nth-child(4) a:hover {
  background-color: #ef4123;
  color: #fff
}

.overlay nav ul li div ul {
  width: 154px;
  box-sizing: content-box;
}

.overlay>.mico a {
  margin: 24px 20px 0 0;
  background-position: 0 0
}

.overlay>.mico a span {
  background-position: 0 -24px
}

.mMenu-wrapper {
  height: 91%;
  overflow-y: auto;
  overflow-x: hidden
}

.mMenu {
  position: fixed;
  right: -320px;
  z-index: 9999;
  width: 240px;
  height: 100%;
  background: #0f0f0f;
  padding: 40px;
  -webkit-transition: all 250ms ease-in-out;
  -moz-transition: all 250ms ease-in-out;
  -o-transition: all 250ms ease-in-out;
  transition: all 250ms ease-in-out
}

.mMenu mark a {
  display: block;
  position: relative;
  float: right;
  width: 15px;
  height: 15px;
  text-indent: -9999px;
  background: url(~assets/images/interface/nav-drop-down-close-icon.png) -70px 0 no-repeat;
  margin-top: 9px
}

.mMenu mark a span {
  display: block;
  position: absolute;
  width: 100%;
  height: 100%;
  top: 0;
  left: 0;
  background: url(~assets/images/interface/nav-drop-down-close-icon.png) -70px -35px no-repeat
}

.mMenu figure a {
  display: block;
  margin: 3px 0 0 6px;
  width: 150px;
  height: 41px;
  text-indent: -9999px;
  background: url(~assets/images/interface/activeoo-logo.png) -10px -78px no-repeat
}

.mMenu b a {
  display: block;
  padding: 22px 0 10px 6px;
  color: #b5b6b7;
  text-transform: uppercase;
  font-family: AvgMedium;
  font-size: 12px;
  border-bottom: #282828 1px solid
}

.mMenu b a:hover {
  color: #fff
}

.mMenu ul {
  width: 100%
}

.mMenu ul li {
  border-bottom: #282828 1px solid;
  color: #fff
}

.mMenu ul li a,
.mMenu ul li span {
  display: block;
  height: 31px;
  padding: 19px 0 0 6px;
  color: #b5b6b7;
  text-transform: uppercase;
  line-height: 14px;
  font-family: AvgMedium;
  box-sizing: content-box;
}

.mMenu ul li a:hover,
.mMenu ul li:hover span {
  background-color: #1f2124;
  text-decoration: none;
  color: #fff
}

.mMenu ul li span {
  background: url(~assets/images/interface/ico-nav.png) right -131px no-repeat;
  cursor: default
}

.mMenu-wrapper>ul>li:nth-child(4)>a {
  color: #ef4123;
  font-family: AvgBold
}

.mMenu ul ul {
  display: none;
  border-top: #232323 1px solid;
  background-color: #191919
}

.mMenu ul ul li:last-child {
  border-bottom: none
}

.mMenu ul ul li a {
  text-transform: none;
  color: #7d7d7d
}

.mMenu ul ul li a:hover {
  background-color: #ffcb0b;
  color: #000
}

.mMenu .nav-select,
.mMenu .nav-select a {
  color: #fff
}

.mMenuContact {
  padding: 50px 0 5px 0
}

.mMenuContact address {
  display: block;
  padding: 10px 0 0 0;
  font-size: 12px;
  line-height: 17px;
  color: #7d7d7d;
  font-family: AvgMedium;
  clear: both
}

.mMenuContact p i {
  display: block;
  float: left;
  border: none;
  background: 0 0
}

.mMenuContact p i a {
  display: block;
  position: relative;
  margin: 0;
  padding: 0;
  width: 34px;
  height: 32px;
  text-indent: -9999px;
  background: url(~assets/images/interface/social-icon.png) 0 -120px no-repeat
}

.mMenuContact p i a span {
  display: block;
  position: absolute;
  width: 34px;
  height: 32px;
  top: 0;
  left: 0;
  padding: 0;
  background: url(~assets/images/interface/social-icon.png) 0 -153px no-repeat
}

.mMenuContact p i+i a {
  background-position: -33px -120px
}

.mMenuContact p i+i a span {
  background-position: -33px -153px
}

.mMenuContact p i+i+i a {
  background-position: -66px -120px
}

.mMenuContact p i+i+i a span {
  background-position: -66px -153px
}

.push {
  overflow-x: hidden;
  position: relative !important;
  left: 0;
  -webkit-transition: all 250ms ease-in-out;
  -moz-transition: all 250ms ease-in-out;
  -o-transition: all 250ms ease-in-out;
  transition: all 250ms ease-in-out
}

.pushed {
  left: -320px
}

.mMenu.push-reset {
  right: 0
}
.mMenu {
    position: fixed;
    right: -320px;
    z-index: 9999;
    width: 240px;
    height: 100%;
    background: #0f0f0f;
    padding: 40px;
    -webkit-transition: all 250ms ease-in-out;
    -moz-transition: all 250ms ease-in-out;
    -o-transition: all 250ms ease-in-out;
    transition: all 250ms ease-in-out;
    box-sizing: content-box;
}
.mMenu figure a {
    display: block;
    margin: 3px 0 0 6px;
    width: 100px;
    height: 41px;
    text-indent: -9999px;
    background: url(~assets/images/interface/activeoo-logo.png) -237px -47px no-repeat;
}
@media only screen and (max-width: 799px){
  .overlay nav ul, header>nav {
      display: none;
  }
  .mico {
      display: block;
  }
}
</style>
