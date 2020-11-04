<template>
  <div class="team">
    <h1 class="subheading grey--text">CATEGORIAS</h1>
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
    <v-img 
          :src="require('../assets/img/c2s.png')"
          class="my-5"
          contain
          height="100"
          
        ></v-img>
        <div><v-divider></v-divider></div>
    
    </v-list-item>
    <v-card-actions>
      
      <div class="headline mb-1 text-right">Computadoras</div>
      <v-list-item-title class="overline text-right" >Stock 40</v-list-item-title>
     

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
         <v-list-item  >
    <v-img 
          :src="require('../assets/img/c3.png')"
          class="my-5"
          contain
          height="100"
          
        ></v-img>
        <div><v-divider></v-divider></div>
        </v-list-item>
    <v-card-actions> 

    <div class="headline mb-1 text-right">V.Vigilancia</div>
      <v-list-item-title class="overline text-right" >Stock 80</v-list-item-title> 
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
         <v-list-item  >
    <v-img 
          :src="require('../assets/img/c1.png')"
          class="my-5"
          contain
          height="100"
          
        ></v-img>
        <div><v-divider></v-divider></div>
        </v-list-item>
    <v-card-actions> 

    <div class="headline mb-1 text-right">Redes</div>
      <v-list-item-title class="overline text-right" >Stock 112</v-list-item-title> 
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
         <v-list-item  >
    <v-img 
          :src="require('../assets/img/c4.png')"
          class="my-5"
          contain
          height="100"
          
        ></v-img>
        <div><v-divider></v-divider></div>
        </v-list-item>
    <v-card-actions> 

    <div class="headline mb-1 text-right">Software</div>
      <v-list-item-title class="overline text-right" >Stock 30</v-list-item-title> 

    </v-card-actions>
  </v-card>
      </v-flex>
<br />


<br />


    <h1 class="subheading grey--text"> SERVICIOS </h1>
        <v-flex xs12 sm6 md4 lg3 v-for="person in team" :key="person.name">
              <v-card class="text-center ma-3">
                <v-responsive class="pt-4">
                   
                    <v-avatar size="100">

                      <v-img
                       :src="require('../assets/img/b1.png')"
                         class="my-3"
                           contain
                             height="200"
                                 ></v-img>

                    </v-avatar>

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
      {name: 'Simon Bolivar', role: 'Ventas Computadoras', avatar:'/img1.png'},
      {name: 'Jose Matinez', role: 'Especialista en V.V', avatar:'.scr/assets/igm/img2.png'},
      {name: 'Davis Martinez', role: 'Especialista en Redes y Software', avatar:'/img3.png'},
      
    ]
  }),
}
</script>