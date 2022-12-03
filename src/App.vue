<template>
  <div class="container">
      <!-- Step 3 must use the component-->
      <HeaderTop bookName="Restaurant Review Application" 
      authorName="Your trusted App for trusted restaurants"
      messageabout="Green represents clearing Health Inspection"/>
      <BookBox :books="books"/>

  </div>

</template>

<script>

// Step 1: Import components
import HeaderTop from './components/HeaderTop.vue'
import BookBox from './components/BookBox.vue'

export default{
  name: 'App',

  // step 2: must register the component
  components: {
    HeaderTop,
    BookBox
  },
  data()
  {
return{
  books:[]
}

  },

  methods:{
//promises
async fetchBooks(){
  const res =await fetch("https://chocolate-chicken-tie.cyclic.app/api")
  const data = await res.json()
  console.log(data) //.books
  return data; //.books
}

  },
  async created(){
this.books= await this.fetchBooks()

  }
}

</script>


<style>
@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@300&display=swap');
*{
box-sizing: border-box;
margin: 0;
padding: 0;
}
body{
font-family:  'Monsterrat', sans-serif;
}
.container{
max-width: 1000px;
min-height: 150px;
overflow:  auto;
margin: 30px auto;
border: 0.3 em solid black;
border-radius: 5px
}

div{
margin-bottom: 0.5em;
}
</style>
