<template>
   <div class="inp-box" v-bind:class="{active:isActive}">
        <input type="text" id="InpName" class="inp" v-bind="inpname" v-on:input="classVali" />
        <label for="InpName" class="lbl" >이름</label>
        <div class="wrapper-msg">
            <span class="msg" v-bind:class="{success:isSuccess, error:isError}">{{isValiTxt}}</span>
        </div>
    </div>		
</template>

<script>
export default {
  name: "InputName",
  data () {
      return {
        inpname: "",
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

