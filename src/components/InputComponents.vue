<template>
<div>

        <div class="Type-div">
            <Error v-if="!types">Please privide the Type of Contract</Error>
               <label for="input-with-list">Contract Type</label>
                <b-form-input list="input-list" id="input-with-list"></b-form-input>
                <b-form-datalist id="input-list" :options="types"></b-form-datalist>
        </div>
        <div class="cat-div">
            <Error v-if="!options">Contract Must Be Put Under A category</Error>
            <label for="input-with-list">Contract Category</label>
                <b-form-input list="input-list" id="input-with-list"></b-form-input>
                <b-form-datalist id="input-list" :options="options"></b-form-datalist>
        </div>    
        <div class="country-div">
             <Error  v-if="!countries">Country</Error>
             <label for="input-with-list">Country</label>
                <b-form-input list="input-list" id="input-with-list"></b-form-input>
                <b-form-datalist id="input-list" :options="countries"></b-form-datalist>
        </div>
        </div>
</template>
<script>
import Error from './Error'
export default {
    components:{
        Error
    },
    data() {
    return {
      options: ['Contract Base', 'Internal Contract', 'Freelancing '],
      countries: ['PH', 'Uganda', 'PH'],
       types: [1, 2,2]
    }
  }
    
}
</script>