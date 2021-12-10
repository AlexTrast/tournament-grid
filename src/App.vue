
<template>
  <!-- Application template -->
  <v-app>
      <div class="players-area">
          <h2>Tournament players</h2>
         <v-text-field class="players-cnt-input" label="Players count"/>
          <v-btn color="primary" elevation="2">Generate players</v-btn>
         <PlayerList v-bind:players="players"/>
      </div>
  </v-app>
</template>

<script>

/**Import component */
import PlayerList from '@/components/PlayerList'

export default {
  name: 'App',

  /**Registration components */
  components: {
    PlayerList
  },

  /**Data declare */
  data() { 
   return { 
          players:[ 
            {id: 1, full_name: 'Jimi Hendrix',    description: 'Мusician',      color:"#2c3e50"},
            {id: 2, full_name: 'Bill Gates',      description: 'Ex. Dirrector', color:"#2c3e50" },
            {id: 3, full_name: 'Linus Torvalds',  description: 'Real coder',    color:"#2c3e50" },
            {id: 4, full_name: 'Dave Mastane',    description: 'Мusician',      color:"#2c3e50" },
            {id: 5, full_name: 'Madame Curie',    description: 'Scientist',     color:"#2c3e50" }
          ]
        }
    },
  };

</script>



<style>

/** application style*/
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}


.players-area { 
    padding: 22px;
    height: 100%; 
    width: auto; 
    position: fixed;
    min-width: 300px;
    z-index: 1; 
    background-color: rgb(244, 244, 244); 
    overflow-x: hidden; 
    box-shadow: 2px 0 25px -2px #888;
    text-align: left;
  }


</style>
