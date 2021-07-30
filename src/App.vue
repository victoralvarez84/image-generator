<template>
  <div id="app" class="content-container">
    <Header title="Victor's Image Generator"/>
    <p v-if="selectedImage" class="image-box">
    <img style="width:100%; height:100%" :src="selectedImage" alt="">
    </p>
    <div class="button-box">
     <button @click="generate()">Generate random image</button> 
    </div>
    </div>
  
</template>

<script>
import Header from './components/Header.vue';

export default {
  name: 'App',
  components:{
    Header
  },
  data () {
    return {
      images: [
      'https://picsum.photos/600/200',
      'https://picsum.photos/600/200',
      'https://picsum.photos/600/200'
    ],
       selectedImage: null
    }
  },
  methods: {
   randomItem (items) {
    return items[Math.floor(Math.random()*items.length)];
    },
   generate () {
    this.selectedImage = this.randomItem(this.images)
    },
   created() {
    this.selectedImage = this.randomItem(this.images)
  }
}
}
</script>

<style>

body{
margin:0;
padding:0;
box-sizing: border-box;
}

.content-container{
display:flex;
flex-direction: column;
align-items:center;
}

.image-box{
 width:75%;
}

.button-box{
display:flex;
justify-content: center;
}

button{
  background-color:#101010;
  border:none;
  height:32px;
  color:white;
  padding:16px;
  border-radius:16px;
  display:flex;
  justify-content: center;
  align-items:center;
  margin-top:48px;
}

</style>
