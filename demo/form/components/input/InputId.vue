<template>
    <div class="inp-box" v-bind:class="{active:isActive}">
        <input type="text" id="InpId" class="inp" v-bind="inpid" v-on:input="classVali" />
        <label for="InpId" class="lbl" >아이디</label>
        <div class="wrapper-msg">
            <span class="msg" v-bind:class="{success:isSuccess, error:isError}">{{isValiTxt}}</span>
        </div>
        <!-- <div class="wrapper-msg">
            <span class="msg error">ERROR!</span>
            <span class="msg success">SUCCESS!</span>
        </div> -->

    </div>
</template>

<script>
export default {
  name: "InputId",
  data () {
      return {
        inpid: "",
        isSuccess: false,
        isError: false,
        isValiTxt: null,
        isActive: false
      }
  },
  methods: {
    classVali (event) {
        // console.dir(event.target.value);
        if (event.target.value.length > 0) {                  
                this.isSuccess = true;
                this.isError = false;
                this.isValiTxt = 'SUCCESS!';
                this.isActive = true;
        } else {
                this.isError = true;
                this.isSuccess = false;
                this.isValiTxt = 'ERROR!';
                this.isActive = false;               
        }
    }
  } 

}
</script>

