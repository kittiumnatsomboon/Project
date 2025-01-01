<script setup>
import { RouterLink, RouterView } from 'vue-router'
import HelloWorld from './components/HelloWorld.vue'
</script>
<script>
export default {
    
  name:'App',
  data(){
      return {
        fname:"kitti",
        lastname:"umnatsomboon",
        age:15,
        address:"<b>กรุงเทพ</b>",
        picture:"https://lh6.googleusercontent.com/proxy/LVIvOTNmgyyLbTFTRm2hy5hMfKbzGWIDSJ_txhczMof2eU_ByW-QxN86_6I5xp-9CnAQaxlZYEaRwzlonqp3YAUyrXBry0C2lrmAk8g1y-Zm7yjAaXYdl3hZyJmOpOcOgIN_iZGolVEhNms",
        width:"200px",
        height:"100px"
      }
  },
  methods:{
      getfullname(){
        return this.fname + this.lastname
      }
  }
}
</script>
<template>
  <header>
    <div>ชื่อ-นามสกุล {{ fname }} {{ lastname }}</div>
    <div>ที่อยู่<span v-html="address"></span></div>
    <div>{{ getfullname() }}</div>
    <img v-bind:width="width" v-bind:height="height" v-bind:src="picture">
    <input name="" v-text="Text" id="">    
  </header>

  <RouterView />
</template>

<!-- <style scoped>
header {
  line-height: 1.5;
  max-height: 100vh;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

nav {
  width: 100%;
  font-size: 12px;
  text-align: center;
  margin-top: 2rem;
}

nav a.router-link-exact-active {
  color: var(--color-text);
}

nav a.router-link-exact-active:hover {
  background-color: transparent;
}

nav a {
  display: inline-block;
  padding: 0 1rem;
  border-left: 1px solid var(--color-border);
}

nav a:first-of-type {
  border: 0;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }

  nav {
    text-align: left;
    margin-left: -1rem;
    font-size: 1rem;

    padding: 1rem 0;
    margin-top: 1rem;
  }
}
</style> -->
