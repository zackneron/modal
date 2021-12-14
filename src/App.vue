<template>
<div>
  <h1 @click="toogleModal">{{ title }}</h1>
  <div v-show="showModal">
    <Modal header="Hello Neron" text="I am your new FED" @close="toogleModal" />
  </div>
</div>
</template> 

<script>
import Modal from './components/Modal.vue'
export default {
  name: 'App',
  components: {
    Modal,
  },
  data(){
    return {
      title: 'Hello Zack',
      showModal: false
    }
  },
  methods: {
    toogleModal(){
      this.showModal = !this.showModal
    }
  }
}
</script>

<style>
body {
  margin: 0;
  padding: 0;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
