<template>
    <div>


          <h2>
                  {{bookName}}
          </h2>
          <h5>
                  {{authorName}}

          </h5>
          <h6>
                  {{messageabout}}
          </h6>

          
        

    </div>
</template>

<script>

export default{
  name: 'HeaderTop',
  props:{
      bookName: String,
      authorName: String,
      messageabout: String
  }
}


</script>

<style scoped>
  div{
      text-align: center;
  }
</style>
