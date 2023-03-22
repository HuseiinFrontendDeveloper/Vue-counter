<template>
<div class="devor">
<h1 class="heading">{{ title }}</h1>
<div class="general">
  <h2>
    Count:
  <span
    v-bind:class="num > 5 ? 'color:red':'color:black'">
    {{ num }}
  </span>
  </h2>
  <div class="btn_general">
    <button v-on:click="addOne" class="add">Add</button>
    <button v-on:click="removeOne" class="remove">Remove</button>
  </div>
</div>
</div>
</template>

<script>

export default {
  name: 'App',
  data(){
    return{
      title:"Vue Counter",
      num:0
    }
  },
  methods:{
    addOne(){
      this.num++
    },
    removeOne(){
      this.num--
    }
  } 
}
</script>

<style>
.devor{
  border: 1px solid black;
  padding: 10px;
}
.heading{
  text-align: center;
}
.general{
  display: flex;
  justify-content: space-between;
  align-items: center;
}
.add{
  padding: 10px 20px;
  border-radius: 5px;
  background-color: green;
  color: white;
  font-weight: 600;
  margin-right: 20px;
  border: none;
  outline: none;
}
.remove{
  padding: 10px 20px;
  border-radius: 5px;
  background-color: red;
  color: white;
  font-weight: 600;
  border: none;
  outline: none;
}
</style>
