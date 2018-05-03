<template>
<ul>

  <li v-for="n in 3" :key="n"><nuxt-link :to="'/sample0' + n">sample0{{n}}</nuxt-link></li>
 
  
</ul>
</template>
