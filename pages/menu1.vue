<template>
<div>
  <h1>Menu</h1>
<ul>
  <li><button @click="gotoRandom">Random</button></li>
  <li v-for="n in 7" :key="n"><nuxt-link :to="'/sample0' + n">sample0{{n}}</nuxt-link></li>

</ul>
</div>
</template>
<script>
export default {
  methods:  {
    gotoRandom(){
      //this.$router.push('/sample01')
      //this.$router.replace('/sample01')
      this.$router.go(-1)
    }
  }
}
</script>

