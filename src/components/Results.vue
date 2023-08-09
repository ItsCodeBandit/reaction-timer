<template>
    <div>
      <p>Reaction time: {{ score }} ms</p>
      <p class="rank">{{ rank }}</p>
    </div>
  </template>
  
  <script>
  export default {
    props: ['score'], 
    data() {
        return{
            rank: null
        }
    }, 
    mounted(){
        if (this.score < 120){
            this.rank = 'Are you Goku!?? '    
        }else if (this.score < 250 ){
            this.rank = 'Like lightning ' 
        } else if (this.score < 400){
            this.rank = 'good Reflexes'
        } else {
            this.rank = 'Maaaaan Your slow.......'
        }
    }
  }
  </script>
  
  <style>
  .rank{
    font-size: 1.4em; 
    color: #6e4eaa; 
    font-weight: bold;
  }
  </style>
  