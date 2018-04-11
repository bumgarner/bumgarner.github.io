<template>
    <div class="inp-box">
        <input type="password" id="InpPass" class="inp" />
        <label for="InpPass" class="lbl" >비밀번호</label>
        <div class="wrapper-msg">
            <!-- <span class="msg error">ERROR!</span> -->
            <span class="msg success">SUCCESS!</span>
        </div>
    </div>	
</template>

<script>
export default {
  name: "InputPass",
  data () {
      return {
      }
  }
}
</script>

