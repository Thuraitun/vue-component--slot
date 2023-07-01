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
    <br><br>
    <Input v-model="name" />
    <br><br>
    <Card></Card>
    <Card>Card Content 1 </Card>
    <Card><h2>Card Content 2</h2></Card>
    <Card><img src="https://cdn.pixabay.com/photo/2015/04/23/22/00/tree-736885_1280.jpg"></Card>
    <Card>
      <template v-slot:header>
        <h2>Header</h2>
      </template>
      <template v-slot:default>
        <img src="https://cdn.pixabay.com/photo/2015/04/23/22/00/tree-736885_1280.jpg">
      </template>
      <template v-slot:footer>
        <button>View Details</button>
      </template>
    </Card>
  </div>
</template>

<script>
  import Greet from "./components/Greet.vue"
  import Article from "./components/Article.vue"
  import ComponentC from "./components/ComponentC.vue"
  import Popup from "./components/Popup.vue"
  import Input from "./components/Input.vue"
  import Card from "./components/Card.vue"

  export default {
    name: "App",
    components: {
      Greet,
      Article,
      ComponentC,
      Popup,
      Input,
      Card,
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
  img{
    width: 200px;
  }
  h2 {
    text-align: center;
    color:blue;
  }
  button {
    padding: 7px 10px;
    background-color: coral;
    color: #fff;
    border-radius: 8px;
  }
</style>