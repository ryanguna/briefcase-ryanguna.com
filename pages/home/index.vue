<template>
    <div>
         <v-container
            fluid
            grid-list-lg
        >
        <v-layout row wrap text-xs-left>


          <v-flex v-for="project in projects" :key="project.name" xs12 sm6>



            <blockquote  class="blockquote mb-4" >

              <div class="title font-weight-regular"  style="margin-bottom:12px;" >{{project.name}}</div>
              <div class="caption font-weight-medium"> {{project.description}}</div>

              <div class="caption font-weight-medium">
                <v-icon style="font-size:13px;" color="yellow lighten-1">fas fa-circle</v-icon>
                Javascript
                <v-icon style="font-size:13px;" color="red lighten-1">fas fa-circle</v-icon>
                HTML
              </div>


            </blockquote>


            <v-divider></v-divider>


          </v-flex>




        </v-layout>
      </v-container>
    </div>
</template>

<script>
    export default {
        data : () => ({
            projects : [
                {
                  name : 'doubleunderscore',
                  description : `Lorem ipsum dolor sit amet, et magna omnes quodsi eum, utinam gloriatur quo id. Ex
                    'reque dissentiunt ius. Vel sale epicuri ex, te sit harum reformidans, pri ea clita vocent virtute. Cu quo inani probatus.`
                }, {
                  name : 'zeus',
                  description : `Lorem ipsum dolor sit amet, et magna omnes quodsi eum, utinam gloriatur quo id. Ex
                    'reque dissentiunt ius. Vel sale epicuri ex, te sit harum reformidans, pri ea clita vocent virtute. Cu quo inani probatus.`
                }, {
                  name : 'node-api',
                  description : `Lorem ipsum dolor sit amet, et magna omnes quodsi eum, utinam gloriatur quo id. Ex
                    'reque dissentiunt ius. Vel sale epicuri ex, te sit harum reformidans, pri ea clita vocent virtute. Cu quo inani probatus.`
                }, {
                  name : 'node-oauth',
                  description : `Lorem ipsum dolor sit amet, et magna omnes quodsi eum, utinam gloriatur quo id. Ex
                    'reque dissentiunt ius. Vel sale epicuri ex, te sit harum reformidans, pri ea clita vocent virtute. Cu quo inani probatus.`
                },
              {
                name : 'baezic-chat-node',
                description : `Lorem ipsum dolor sit amet, et magna omnes quodsi eum, utinam gloriatur quo id. Ex
                    'reque dissentiunt ius. Vel sale epicuri ex, te sit harum reformidans, pri ea clita vocent virtute. Cu quo inani probatus.`
              }, {
                name : 'doubleunderscore',
                description : `Lorem ipsum dolor sit amet, et magna omnes quodsi eum, utinam gloriatur quo id. Ex
                    'reque dissentiunt ius. Vel sale epicuri ex, te sit harum reformidans, pri ea clita vocent virtute. Cu quo inani probatus.`
              },
            ]
        })
    }


</script>   
