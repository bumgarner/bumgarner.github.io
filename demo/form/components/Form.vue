<template lang="html">
    <div id="wrap">
        <!-- content -->
        <div id="content">
            <div class="wrapper-box">
                <h1 class="logo">Logo</h1>
                <div class="box-inner">
                    <form action="#">
                        <input-id></input-id>
                        <input-pass></input-pass>
                        <input-name></input-name>                        
                        <input-mail></input-mail>                       
                        <input type="submit" id="btnJoin" class="btn" title="가입하기" alt="가입하기" value="가입하기" >
                    </form>
                </div>
            </div>
        </div>
        <!-- //content -->
    </div>
</template>

<script>
import InputId from '@/components/input/InputId'
import InputPass from '@/components/input/InputPass'
import InputName from '@/components/input/InputName'
import InputMail from '@/components/input/InputMail'

export default {
  components: {
      InputId,
      InputPass,
      InputName,
      InputMail,

  },
  name: 'Form'
}
</script>

<style scoped>
@import '../css/form.css';



</style>


