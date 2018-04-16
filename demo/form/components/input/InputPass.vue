<template>
    <div class="inp-box" v-bind:class="{active:isActive}">
        <input type="password" id="InpPass" class="inp" v-bind="inppass" v-on:input="classVali" />
        <label for="InpPass" class="lbl" >비밀번호</label>
        <div class="wrapper-msg">
            <span class="msg" v-bind:class="{success:isSuccess, error:isError}">{{isValiTxt}}</span>
        </div>
    </div>	
</template>

<script>
export default {
  name: "InputPass",
  data () {
      return {
        inppass: "",
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

