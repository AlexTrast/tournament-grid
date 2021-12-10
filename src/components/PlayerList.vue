<template>

  <!-- table template -->

     <v-list two-line>
            <v-list-item-group v-model="selectedItem" color="primary" >
                  <v-list-item v-for="player in players" :key="player.id" >
              
                    <v-list-item-avatar>
                      <v-avatar color="green" size="62">
                      <span class="white--text text-h5">{{player.full_name[0]}}</span>
                      </v-avatar>
                    </v-list-item-avatar>

                    <v-list-item-content>
                      <v-list-item-title v-text="player.full_name"></v-list-item-title>
                      <v-list-item-subtitle v-text="player.description"></v-list-item-subtitle>
                    </v-list-item-content>

                  </v-list-item>
                </v-list-item-group>
           </v-list>
</template>
 
<script>
/** Export as default obj*/
  export default {
    props: ['players'] 
  }
</script>


<style scoped>
/** Private style*/

  .theme--light {
      background: rgb(244, 244, 244); ;
      color: rgba(0, 0, 0, 0.87);
  }
  /**TODO: Fix white spases*/
  .v-item-group {
    margin-top: -8px;
    margin-bottom: -8px;
  }
  .v-list {
    margin-top: 8px;
  }

  .white--text {
    margin-left: -22px;
  }
</style>
