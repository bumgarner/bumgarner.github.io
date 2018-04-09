<template lang="html">
    <div id="mobile-bar">
        <a class="menu-button"></a>
        <a class="logo" href="/">Logo</a>
    </div>
</template>

<script>
export default {
  name: "MobileHeader"
}
</script>

<style scoped>
#mobile-bar {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 40px;
  background-color: #fff;
  z-index: 9;
  display: none;
  box-shadow: 0 0 2px rgba(0,0,0,0.25);
}
#mobile-bar .menu-button {
  position: absolute;
  width: 24px;
  height: 24px;
  top: 8px;
  left: 12px;
  background: url("../../img/menu.png") center center no-repeat;
  background-size: 24px;
}
#mobile-bar .logo {
  position: absolute;
  width: 30px;
  height: 30px;
  /* background: url("../../images/logo.png") center center no-repeat; */
  top: 5px;
  left: 50%;
  margin-left: -15px;
  background-size: 30px;
}
@media screen and (max-width: 900px) {
  #mobile-bar {
    display: block;
    line-height: 30px;
  }
  #mobile-bar {
    display: block;
    line-height: 30px;
  }
}
</style>


