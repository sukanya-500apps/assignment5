
<template>
    <div>
        <form>
    Firstname: <input type="text" id="fn" name="firstname" placeholder="Enterfirstname"/><br>
    Lastname: <input type="text" id="ln"  name="lastname" placeholder="Enterlastname" /><br>
        <input type="button" @click="add()" Value="add" />
        <input type="button" @click="remove()" Value="remove" />
    </form>
<b-table users :items="items" :fields="fields"></b-table>
    </div>
</template>
<script>
export default{
    name:"QuE3",
    data(){
        return{
fields:['firstname','lastname'],
items:[{firstname:"sukanya",lastname:"afa"}]
        }
    },
    methods:{
        add(){
            this.items.push({
firstname:document.getElementById("fn").value,
lastname:document.getElementById("ln").value,
            });
    },
    remove(){
        this.items.pop("fn","ln");
    },
       },
    };
</script>
