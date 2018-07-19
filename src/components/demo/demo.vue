<template>
  <div class="hello">
    <div class="holder">
      <ul>
        <li v-for="(data,index) in skills" :key ='index'>{{index}}: {{data.skill}}</li>
      </ul>
    </div>
    <button v-bind:disabled="btnState" v-on:click="click">change name</button>
    <div v-bind:class="{ 'alert': showAlert, 'second': lula}">example one</div>
    <div v-bind:class="demoObj">example two</div>
    <div v-bind:style="{ backgroundColor: bgColor, width: bgWidth, height:bgHeight}">example three</div>
  </div>
</template>

<script>
export default {
  name: "demo",
  data() {
    return {
      skills: [{ skill: "Vue.js" }, { skill: "Frontend Developer" }],
      btnState: true,
      showAlert: true,
      lula: true,
      demoObj: {
        demo: true,
        obj: true
      },

      bgColor: "green",
      bgWidth: "100%",
      bgHeight: "100px"
    };
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.alert {
  background-color: yellow;
  width: 100%;
  height: 50px;
}
.second {
  border: 3px black solid;
}
.demo {
  background-color: crimson;
  width: 100%;
  height: 50px;
}
.obj {
  border: 3px black solid;
}
</style>
