<template>
    <div>
        <b-form @submit="onSubmit" @reset="onReset" v-if="show">
      <b-form-group
        id="input-group-1"
        label="country"
        label-for="input-1">
        <b-form-input
          id="input-1"
          v-model="form.country"
          type="text"
          placeholder="Enter country name"
          required></b-form-input>
      </b-form-group>
      <b-button @click="OnSubmit(event)" type="submit" variant="primary">Submit</b-button>
      <b-button  @click="OnReset(event)" type="reset" variant="danger">Reset</b-button>
    </b-form>
    <b-card class="mt-3" header="Form Data Result">
      <pre class="m-0">{{ form }}</pre>
    </b-card>
    </div>
</template>
<script>
var axios = require("axios").default;
export default {
name: 'QuE4',
components: {},
data(){
    return{
        form:{
           country:" "
       },
    }
},
async mounted(){
let response=await this.getData()
console.log(response)
},
methods: {
     onSubmit(event) {
        event.preventDefault()
        alert(JSON.stringify(this.form))
     },
     onReset(event) {
        event.preventDefault()
        // Reset our form values
        this.form.country = ''
     },
 getData(){
let response= new Promise((resolve, reject) => {
axios.get("http://universities.hipolabs.com/search?country=${India}").then((response) => {
resolve(response.data);
}).catch((error) => {
reject(error);
});
});
response.then((data) => {console.log("response", data) }).catch((err) => {console.log(err)})
}

}
}
</script>
