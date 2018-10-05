<template>
  <div id='app'>
    <main>
      <p :listings="listings"></p>
    </main>
  </div>
</template>

<script>
  export default {
      name:'app',

    data(){
      return{
        lisings: [],
        apiURL: ''
      }
    },
    mounted (){
      fetch(this.apiURL)
        .then(response => response.json())
        .then(response => {
        this.listings = response
      })
    },
  }

</script>