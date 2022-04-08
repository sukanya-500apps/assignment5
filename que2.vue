<template>
<div>
<h1>Question2</h1>
<b-form-input type="Number" id="multi" placeholder="Enter a Firstnumber"></b-form-input>
<b-form-input type="Number" id="divi" placeholder="Enter a Secondnumber "></b-form-input>
<b-button @click="f1()">Multiply</b-button>
<b-button @click="f2()">Divide</b-button>
<p id="demo"></p>
</div>
</template>
<script>
export default {
name: "QuestioN2",
data() {
return {
multiply: [],
division: [],
};
},
methods: {
f1() {
document.getElementById("demo").innerHTML =
document.getElementById("multi").value *
document.getElementById("divi").value;
return this.multiply;
},
f2() {
document.getElementById("demo").innerHTML =
document.getElementById("multi").value /
document.getElementById("divi").value;
return this.division;
},
},
};
</script>


