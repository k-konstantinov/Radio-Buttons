<template>
  <div class="main">
    <div>
      <h1 v-bind:class="color">This is website Content</h1>
      <b><label for="color">Select Color:&nbsp;</label></b>
      <input type="radio" v-model="color" value="green" />
      <label for="green">&nbsp;Green&nbsp;</label>
      <input type="radio" v-model="color" value="orange" />
      <label for="orange">&nbsp;Orange&nbsp;</label>
      <button v-on:click="color = 'black'">Reset</button>
      <br/><br/>
      <input type="checkbox" v-model="isActive" value="true" />
      <label for="active">&nbsp;Deactivate&nbsp;</label>
      <button :disabled="isActive">Click</button>
    </div>
    <br />
    <div v-if="result">
      <ul>
        <li v-for="item in data" :key="item">
          {{ item }}
        </li>
      </ul>
    </div>
    <button v-on:click="result = !result" :disabled="isActive">
      Show / Hide
    </button>
    <br/>
    <br/>
  </div>
</template> 
<script>
export default {
  name: "Hello",
  data() {
    return {
      color: "",
      isActive: false,
      result: false,
      data: ["Sofia", "Plovdiv", "Varna"],
    };
  },
};
</script>
<style>
.green {
  color: green;
}
.orange {
  color: orange;
}
li {
  list-style: none;
  font-size: 30px;
  font-weight: 800;
  display: inline-block;
  margin: 10px;
  color: #35495e;
}
button {
  background-color: #41b883;
  border: none;
  color: white;
  padding: 20px;
  text-align: center;
  display: inline-block;
  font-size: 16px;
  cursor: pointer;
  border-radius: 12px;
}
</style>