<template>
  <div class="wrap">
    <nuxt-link to="/header"></nuxt-link>
    <CoachMenuMobile v-model="headerMobileState"/>
    <div class="header">
      <img src="../components/images/Logo1.png" id="logo" />
    </div>
    <div class="burgerWrap">
      <div class="language">
        <div class="en"><a href="#">EN</a></div>
        <div class="ua"><a href="#">UA</a></div>
      </div>
      <div class="burger" @click="openMenuMobile">
        <a href="#"> <img id="menu" src="../components/images/gamburger.png" /> </a>
      </div>
    </div>
  </div>
</template>
<script>
import CoachMenuMobile from "../components/CoachMenuMobile"
export default {
  name: 'Header',
  components:{
    CoachMenuMobile
  },
  data(){
    return {
      headerMobileState:false,
    }
    },
  methods:{
    openMenuMobile(){
      this.headerMobileState=!this.headerMobileState
    }
  }
}
</script>
<style scoped>
@media only screen and (max-width: 475px) {
  .header {
    width: 53.5%;
    height: 40px;
    background-color: #d2d1d1;
  }
  #logo {
    width: 79px;
    height: 42px;
    margin: 1px 0px 3px 8px;
  }
  .wrap {
    width: 100vw;
    height: 40px;
    background-color: #d2d1d1;
    display: flex;
    align-items: center;
    justify-content: space-between;
  }
  .burger {
    width: 33px;
    height: 24px;
    display: flex;
    justify-content: right;
    margin: 8px 8px 8px 0px;
  }
  .language {
    width: 67px;
    /* border: 1px solid navy;  */
    font-family: "Inter";
    font-style: normal;
    font-weight: 400;
    font-size: 16px;
    line-height: 19px;
    color: #000000;
    display: flex;
  }
  .en {
    display: flex;
    align-items: center;
    width: 21px;
    height: 40px;
    justify-content: space-between;
    margin: 0px 25px 0px 11px;
  }
  img > #menu {
    margin: 0 auto;
    height: 21px;
    width: 19px;
  }

  .ua {
    display: flex;
    margin: 0 auto;
    width: 23px;
    height: 40px;
    justify-content: space-between;
    align-items: center;

    /* border: 1px solid orange; */
  }

  .burgerWrap {
    display: flex;
    justify-content: space-between;
    width: 46.5%;
  }
  a {
    text-decoration: none;
    color: rgba(0, 0, 0, 0.4);
  }
  a:hover {
    text-decoration: underline;
    color: #000000;
  }
}
</style>