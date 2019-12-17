<template>
  <div>
    <PageHeader />
    <div class="container">
      <div class="row">
        <section class="home-haedline" style="margin-bottom:60px;">
          <h2>Our <span>Cases</span></h2>
          <h3>We convert your ideas into great results</h3>
        </section>
      </div>
      <div class="row">

      </div>
    </div>

  </div>
</template>

<script>
import Logo from '~/components/Logo.vue'
import PageHeader from '~/components/Header/PageHeader.vue'
import ContactSection from '~/components/Contact/ContactSection.vue'

export default {
  components: {
    Logo, PageHeader, ContactSection
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
</style>
