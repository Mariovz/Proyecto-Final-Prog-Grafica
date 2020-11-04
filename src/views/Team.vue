<template>
  <div class="team">
    <h1 class="subheading grey--text">VENTAS</h1>
    <v-container >
      <v-layout row wrap>
         <v-flex
        sm6
        xs12
        md6
        lg3
      >
       <v-card class="ma-3">
    <v-list-item  >
       <v-list-item-avatar
        tile
        
        class="mt-n7"
      >
      <v-sheet color="green" width="40" height="80" elevation="10">
            <v-icon dark large>store</v-icon>
      </v-sheet>
      </v-list-item-avatar>
      <v-list-item-content>
        <div class="headline mb-1 text-right">Computadoras</div>
        <v-list-item-title class="overline text-right" >5,000.01</v-list-item-title>
        <div><v-divider></v-divider></div>
      </v-list-item-content> 
    </v-list-item>
    <v-card-actions>
      <v-icon text class="ma-2"></v-icon>
      <div class="overline">Octubre</div>
    </v-card-actions>
  </v-card>
      </v-flex>
       <v-flex
        sm6
        xs12
        md6
        lg3
      >
       <v-card class="ma-3">
    <v-list-item>
       <v-list-item-avatar
        tile
        class="mt-n7"
      >
      <v-sheet color="#F44336" width="40" height="80" elevation="10">
            <v-icon dark large>home</v-icon>
      </v-sheet>
      </v-list-item-avatar>
      <v-list-item-content>
       <div class="headline mb-1 text-right">V.Vigilanicia</div>
        <v-list-item-title class="overline text-right" >2,000.91</v-list-item-title>
        <div><v-divider></v-divider></div>
      </v-list-item-content> 
    </v-list-item>
    <v-card-actions>
     
      <div class="overline">Octubre</div>
    </v-card-actions>
  </v-card>
      </v-flex>
       <v-flex
        sm6
        xs12
        md6
        lg3
      >
       <v-card class="ma-3">
    <v-list-item>
       <v-list-item-avatar
        tile
        class="mt-n7"
      >
      <v-sheet color="#03A9F4" width="40" height="80" elevation="10">
            <v-icon dark large>home</v-icon>
      </v-sheet>
      </v-list-item-avatar>
      <v-list-item-content>
      <div class="headline mb-1 text-right">Redes</div>
        <v-list-item-title class="overline text-right" >6,500.00</v-list-item-title>
        <div><v-divider></v-divider></div>
      </v-list-item-content> 
    </v-list-item>
    <v-card-actions>
      
      <div class="overline">Octubre</div>
    </v-card-actions>
  </v-card>
      </v-flex>
       <v-flex
        sm6
        xs12
        md6
        lg3
      >
       <v-card class="ma-3">
    <v-list-item >
       <v-list-item-avatar
        tile
        class="mt-n7"
      >
      
      <v-sheet color="#FFC107" width="40" height="80" elevation="10">
            <v-icon dark large>home</v-icon>
      </v-sheet>
      </v-list-item-avatar>
      <v-list-item-content>
        <div class="headline mb-1 text-right">Software</div>
        <v-list-item-title class="overline text-right" >1,100.60</v-list-item-title>
        <div><v-divider></v-divider></div>
      </v-list-item-content> 
    </v-list-item>
    <v-card-actions>

      <div class="overline">Octubre</div>
    </v-card-actions>
  </v-card>
      </v-flex>
      <div></div>

       <h2 class="subheading grey--text">PROVEEDORES</h2>

        <v-flex xs12 sm6 md4 lg3 v-for="person in team" :key="person.name">
              <v-card class="text-center ma-3">
                <v-responsive class="pt-4">
                    <v-img 
          :src="require('../assets/img/st.png')"
          class="my-5"
          contain
          height="100"
          
        ></v-img>
                </v-responsive>
                <v-card-text>
                  <div class="subheading">{{person.name}}</div>
                  <div class="grey--text">{{person.role}}</div>
                </v-card-text>
                <v-card-actions>
                    <v-btn outlined color="orange">
                        <v-icon small left >message</v-icon>
                        <span>Message</span>
                    </v-btn>
                </v-card-actions>
              </v-card>
        </v-flex>
       
      </v-layout>
    </v-container>
  </div>
</template>

<script>
// @ is an alias to /src
export default {
  name: 'team',
  components: {
   
  },
  data : () => ({
    team: [
      {name: 'ServiTech', role: 'Computadoras', avatar:'/img1.png'},
      {name: 'ServiTech', role: 'V.Vigilnicia', avatar:'/img2.png'},
      {name: 'ServiTech', role: 'Redesy Software', avatar:'/img3.png'},
     
    ]
  }),
}
</script>