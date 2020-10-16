<template>
  <div class="text_board_creater">
    <quillEditor
    v-model="content"
    ref="HrContractEditor"
    :options="editorOption"
    />
  </div>
</template>

<script>
import 'quill/dist/quill.snow.css'
import {quillEditor} from 'vue-quill-editor'
import {Button ,Input ,Select } from 'iview'
export default {
  components:{
    quillEditor,
    // Button,
    // Input,
    // Select

  },
  data(){
    return{
      conatent:'',
      editorOption:{
        debug:'info',
        placeholder:'Type Your Contract Agreement Here ....',
        readOnly:true,
        theme:'snow'
      },
      delta:undefined
    }

  },
  watch:{
    conatent(val){
      this.delt = this.$refs.HrContractEditor.quill.getcontents()
      console.log(this.delt)
    }

  }
 
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>
.ql-editor{
  height: 72vh;
}

</style>
