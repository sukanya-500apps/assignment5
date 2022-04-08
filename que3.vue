<template>
    <div>
        <form>
    Firstname: <input type="text" id="fn" name="firstname" placeholder="Enterfirstname"/><br>
    Lastname: <input type="text" id="sn"  name="lastname" placeholder="Enterlastname" /><br>
        <input type="button" @click="add()" Value="add" />
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
            var fn,sn
this.firstname=document.getElementById(fn).value
this.lastname=document.getElementById(sn).value

console.log(this.firstname)
console.log(this.lastname)



       }
    }
}
</script>
