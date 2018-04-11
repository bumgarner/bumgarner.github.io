<template>
    <div class="inp-box">
        <input type="text" id="InpId" class="inp" v-model="inpid" />
        <label for="InpId" class="lbl" >아이디</label>
        <div class="wrapper-msg">
            <span class="msg error">ERROR!</span>
            <!-- <span class="msg success">SUCCESS!</span> -->
        </div>
    </div>
</template>

<script>
export default {
  name: "InputId",
  data () {
      return {
      }
  }
}
</script>

