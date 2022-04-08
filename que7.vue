<template>
    <div>
        <b-table  :fields="fields" :items="response"></b-table>
    </div>
</template>
<script>
var axios=require("axios").default
export default{
    name:"QuE7",
    data(){
        return{
            fields:["url"],
            items:[{url:""}]
        }
    },
    async mounted(){
        let response=await this.getData()
            console.log(response)},
        methods: {
getData(){
let response= new Promise((resolve, reject) => {
axios.get("https://agilecrm.com").then((response) => {
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
