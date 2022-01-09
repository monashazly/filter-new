<template>
<Nav></Nav>
  <HelloWorld />
  
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import Nav from './components/nav.vue'

export default {
  name: 'App',
  components: {
    HelloWorld,
    Nav
  }
}
</script>

<style>

</style>
