<template>
  <div>
    <Greet name="Thurai" heroName="Superman" />
    <Greet name="David" heroName="Spiderman" />
    <Greet name="Alex" heroName="Iconman" />
    <Greet :name="name" :heroName="channel" />

    <Article id="article-title" title="Article title" :likes="50" :isPublished="true" />
    <h2>App Component Username is <u>{{ name }}</u></h2>
    <ComponentC />

    <button @click="showPopup = true">Show Popup</button>
    <Popup v-show="showPopup" @close="closePopup" />
  </div>
</template>

<script>
  import Greet from "./components/Greet.vue"
  import Article from "./components/Article.vue"
  import ComponentC from "./components/ComponentC.vue"
  import Popup from "./components/Popup.vue"

  export default {
    name: "App",
    components: {
      Greet,
      Article,
      ComponentC,
      Popup,
    },
    data() {
      return {
        name: 'Nano',
        channel: 'Team Coding',
        showPopup: false,
      }
    },
    methods: {
      closePopup(name) {
        this.showPopup = false
        console.log('name', name)
      }
    },
    provide(){
      return {
        username: this.name,
      }
    }
  }
</script>

<style scoped>
  #app {
    text-align: center;
  }
</style>