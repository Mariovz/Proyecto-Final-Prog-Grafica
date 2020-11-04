<template>
  <div class="projects">
    <h1 class="subheading grey--text">INGRESOS Y PROVEEDORES </h1>

    <v-container>
      <v-layout row wrap class="mb-4">
      <v-tooltip bottom>
      <template v-slot:activator="{ on }">
        <v-btn small outlined color="green" @click="sortBy('title')" class="mr-2" dark v-on="on">
           <v-icon left small>folder</v-icon>
            <span class="caption text-lowercase">Ingresos</span>
        </v-btn>
      </template>
        <span>Sort project</span>
      </v-tooltip>
       <v-tooltip bottom>
      <template v-slot:activator="{ on }">
        <v-btn small outlined color="blue" @click="sortBy('title')" class="mr-2" dark v-on="on">
           <v-icon left small>person</v-icon>
            <span class="caption text-lowercase">Proveedores</span>
        </v-btn>
      </template>
        <span>Sort person</span>
      </v-tooltip>
      </v-layout>
      <v-card flat  v-for="project in projects" :key="project.title" class="mb-1">
          <v-layout row wrap :class="`pa-3 project ${project.status}`">
            <v-flex xs12 md6>
                <div class="caption grey--text"></div>
                <div >{{project.title}}</div>
            </v-flex>
            <v-flex xs6 sm4 md2>
                <div class="caption grey--text">ServiTech S.A</div>
                <div >{{project.person}}</div>
            </v-flex>
            <v-flex xs6 sm4 md2>
                <div class="caption grey--text">Fecha de Compra</div>
                <div >{{project.due}}</div>
            </v-flex>
          </v-layout>
      </v-card>
    </v-container>
  </div>
</template>

<script>
// @ is an alias to /src
export default {
  name: 'projects',
  components: {
   
  },
  data: () => ({
    projects : [
      {title: 'Computadoras ', person :'1005.00', due: '10/10/2020', status:'no'},
      {title: 'Camaras IP', person :'800.00', due: '02/11/2020', status:'complete'},
      {title: 'Cable CAT 6', person :'2500.00', due: '01/09/2020', status:'yes'},
      {title: 'Antivirus', person :'300.00', due: '02/09/2020', status:'up'},
    ]
  }),
  methods: {
    sortBy(prop){
      this.projects.sort((a,b) => a[prop] < b[prop] ? -1:1)
    }
  }
}
</script>
<style >
  .project.complete {
      border-left: 4px solid #3cd1c2;
  }
  .project.no {
      border-left: 4px solid orange;
  }
  .project.up {
      border-left: 4px solid black;
  }
  .project.yes {
      border-left: 4px solid yellow;
  }
   .v-chip.complete {
      color: #3cd1c2;
  }
  .p.ovnored {
      color: orange;
  }
  .p.up {
      color:  black;
  }
  .p.yes {
      color:  yellow;
  }
</style>
