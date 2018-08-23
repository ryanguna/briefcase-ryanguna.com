<template>
    <div>
         <v-container
            fluid
            grid-list-lg
        >
        <v-layout row wrap text-xs-left>
        
          <v-flex v-for="project in projects" :key="project.name" xs12 sm6>
              <v-card-text>
                   <div>
                     <v-icon>settings</v-icon>
                     {{project.name}}</div>
                
                     <p class=" font-weight-light">
                        {{project.description}}
                    </p>
                </v-card-text>


          </v-flex>

         
        </v-layout>
      </v-container>
    </div>
</template>

<script>
    export default {
        data : () => ({
            projects : [
                {name : 'doubleunderscore', description : 'doubleunderscore.js is a utility-belt library for javaScript that i created that provides support for my usually used functionalities.'},
                {name : 'luke-skywalker', description : ''},
                {name : 'node-oauth',description : ''},
                {name : 'NEXUS', description : ''},
                {name : 'TESI Inventory', description : ''},
            ]
        })
    }


</script>   
