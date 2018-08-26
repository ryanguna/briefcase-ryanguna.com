<template>
    <div>
         <v-container
            fluid
            grid-list-lg
            text-xs-center
        >
        <v-layout row wrap text-xs-left>


          <v-flex v-for="project in projects" :key="project.name" xs12 sm6>



            <blockquote  class="blockquote mb-4" >

              <div class="title font-weight-regular"  style="margin-bottom:12px;" >
                <a :href = "project.link" target="_blank">{{project.name}}</a></div>
              <div class="caption font-weight-medium"> {{project.description}}</div>



            </blockquote>







          </v-flex>





        </v-layout>

           <blockquote  class="blockquote mb-4 "  >
             <v-icon>fas fa-drafting-compass</v-icon>
             Still crafting more contents...
           </blockquote>

         </v-container>
    </div>
</template>

<script>
    export default {
        data : () => ({
            projects : [
                {
                  name : 'doubleunderscore',
                  link : 'https://github.com/ryanguna/doubleunderscore',
                  description : `doubleunderscore.js is a utility-belt library for JavaScript available in npm that i created that provides support for my usually used functionalities.`
                },
                {
                  name : 'briefcase-ryanguna.com',
                  link : 'https://github.com/ryanguna/briefcase-ryanguna.com',
                  description : `Briefcase is my personal website that showcases my projects and contributions`
                }, {
                  name : 'node-api',
                  link : 'https://github.com/ryanguna/node-api',
                  description : `A node Restful API with mongoDB`
                },
                {
                  name : 'baezic-chat-node',
                  link : 'https://github.com/ryanguna/baezic-chat-node',
                  description : `Server side part of my real time baezic-chat application built with Nodejs`
                },
                {
                  name : 'baezic-chat-vue',
                  link : 'https://github.com/ryanguna/baezic-chat-vue',
                  description : `Client side part of my real time baezic-chat application built with Vuejs`
                },
            ]
        }),
        head () {
          return {
            title: 'Ryan Guna | Crafts',
            meta: [
              { hid: 'description', name: 'description', content: 'My custom description' }
            ]
          }
        }
    }


</script>   
