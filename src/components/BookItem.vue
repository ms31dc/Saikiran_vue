<template>

    <div class="container">
          
    <div :class="book.isHealthInspected? 'green' : 'red'">
       Health Inspection Color Code
    </div>
    
     
    
    
    <h2 class="alignbb" > Name:{{book["restaurant Name"]}}</h2>
    <h4 class="alignbb" >Restaurant Cuisine:{{book.cuisine}}</h4>
    <h4 class="alignbb" >Restaurant Rating:{{book.rating}}</h4>
    <h4 class="alignbb" >Best Dishes:{{book.bestDishes}}</h4>
    <h4 class="alignbb" >Recent review date:{{book["review date"]}}</h4>
    
    
    
    
    </div>
    
    
    </template>
    
    
    <script>
    
     export default{
        name: 'BookItem',
        props:{
            book: Array
        }
        
     
     }
     
    </script>
    
    <style scoped>
     .alignbb{
        text-align: center;
     }
    
    
    
    h4{margin:2px;}
    div{background-color: #ffb89e; color:black; padding:1em;}
    
    .red{
    background-color: orangered;
    
    }
    
    .green{
        background-color:green;
    }
    
    
    
    
    .container{
    
    background-color: palegreen;
    padding: 1em;
    color: black;
    display: grid;
    grid-template-columns: 1fr 1fr 1fr 1fr 1fr 1fr;
    grid-template-rows: 1fr;
    grid-template-areas:  
    "Research Research Research Research Research";
    }
    
    #Research{
    
        grid-area:Research;
    background-color: #4C68B2;
    
    color: rgb(0, 0, 0);
    
    }
    
     
     </style>
     