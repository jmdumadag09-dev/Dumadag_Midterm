<script setup>
//String interpolation
import { ref } from "vue";

const q1 = 80;
const q2 = 90;
const q3 = 85;

const score = 59;
const prefectScore = 80;
const precentage = (score/prefectScore) * 100;

//Attribute Binding

const productName = ref("Laptop");
const image = "https://cdn.shopify.com/s/files/1/0533/2089/files/vuejs-tutorial.png?v=1509471047";


   //Hyperlink Binding

const schoolName = "Cebu Doctors University";
const website = "https://cdu.edu.ph/";


//button dissable/ actvite

const isDisabled = false;
const isActive = true;

//inrement/decrement
const count = ref(0);
const increase = () =>{
    count.value++;
};
const decrease = () =>{
    count.value--;
};

const reset = ()=>{
    count.value = 0;
};

// conditional using ternary operator

const passed = false;

//conditional rendering

const online = ref(false)

const toggleStatus = () => {
    online.value = !online.value;
};
</script>

<template>
  <div>

    <h2>Quiz 1: {{ q1 }}</h2>
    <h2>Quiz 2: {{ q2 }}</h2>
    <h2>Quiz 3: {{ q3 }}</h2>
    <h2>Average: {{ (q1 + q2 + q3) / 3 }}</h2>

    <h2>{{ score }} / 100</h2>
    <h2>{{ precentage }}%</h2>
    <hr></hr>

    <h2>{{ productName }}</h2>
    <img :src="image" alt="Vuejs" width="200"/>

    <hr></hr>
    <h2>{{ schoolName }}</h2>
    <a :href ="website" target="_blank">Open Website</a>
    <hr></hr>

<br>


    <button :disabled="isDisabled">Press me</button>
    <h1 :class="{active: isActive}"> Online</h1>
<hr>

<h1>Count:{{ count }}</h1>
<button @click="increase">increase</button>
<button @click="decrease">decrease</button>
<button @click="reset">reset</button>
<hr>

<h2>
  
    Status: {{ passed ? "Passed": "Falied" }}</h2>
<hr>
<h2  :class="online ? 'Online' : 'Offline'">{{ online ? "Online": "Offline" }}</h2>
<button @click="toggleStatus">Status</button>

 


  </div>
</template>

<style>
.active{
    color: green;
    font-weight: bold;
}

.Online{
    color: green;
}

.Offline{
    color:red;
}
</style>



