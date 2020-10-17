<template>
  <b-container >
    <Header/>
    <b-row class="main">
      <b-col cols="2" >
         <LeftInput/>
      </b-col>
      <b-col cols="10" >
         <TextBoardCreater/>
      </b-col>
       
    </b-row>
    
  </b-container>
</template>
<script>
import 'bootstrap/dist/css/bootstrap.css'
import 'bootstrap-vue/dist/bootstrap-vue.css'
import LeftInput from './components/InputComponents'
// import './custom.scss'
import TextBoardCreater from './components/TextBoard'
import Header from './components/Header'
export default {
  components:{
    TextBoardCreater,
    Header,
    LeftInput

  }
  
}
</script>

<style scoped>
.main{
  margin-top: 20px;
}

</style>
