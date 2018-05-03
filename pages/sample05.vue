<template>
  <div>
    <h1 v-if="ok">Hello {{ name }}</h1>
    <div v-show="ok">{{ upperName }}</div>
    <input type="text" :value="name"><br>
    <input type="text" v-model="name"><br>
    <button @click="doToggle">Toggle</button>
  </div>
</template>
<script>
export default {
  data() {
    return { name: "World", ok: true }
  },
  computed: {
    upperName() {return this.name.toUpperCase()}
  },
  methods: {
    doToggle() {
      this.ok = !this.ok;
    },
  },
}
</script>