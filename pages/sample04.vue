<template>
  <div>
    <h1>Hello {{ name }}</h1>
    <div>{{ upperName }}</div>
    <input type="text" :value="name"><br>
    <input type="text" v-model="name"><br>
    <v-btn @click="doSave"><v-icon>favorite</v-icon>SAVE</v-btn>
   
  </div>
</template>
<script>
export default {
  data() {
    return { name: "World" }
  },
  computed: {
    upperName() {return this.name.toUpperCase()}
  },
  methods: {
    doSave() {
      console.log('SAVE',this.name, this.upperName);
    },
  },
}
</script>