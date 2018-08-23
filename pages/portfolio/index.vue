<template>
    <div>
         <v-container
            fluid

            style="padding:0px;"
        >

        
          <v-flex v-for="project in projects" :key="project.name" xs12 sm12>
            <v-card  style="border-bottom: 1px solid #dbdcdb !important; margin-bottom: 5px; margin-top:5px;" flat height="250">

              <v-layout fill-height row wrap align-end  v-if="project.align == 'left'">
                <v-flex xs12 sm5 >
                 <v-card hover flat height="218" style="overflow:hidden !important; ">


                   <v-system-bar height="22" style="background-color:rgba(0, 0, 0, .1) !important"  window dark lights-out >

                     <v-icon style="font-size:12px;" color="red lighten-1">fas fa-circle</v-icon>
                     <v-icon style="font-size:12px;" color="orange lighten-1">fas fa-circle</v-icon>
                     <v-icon style="font-size:12px;" color="green lighten-1">fas fa-circle</v-icon>
                   </v-system-bar>

                   <v-card-media

                     style="
                      height: 228px;
                      background-position: center;
                      background-repeat: no-repeat;
                      text-rendering: optimizelegibility;
                      -webkit-font-smoothing: antialiased;
                      background-size: cover; "
                     :src="project.img"
                   >
                   </v-card-media>



                   </v-card>
                </v-flex>


                <!--<v-icon color="green">fab fa-node</v-icon>-->
                <!--<v-icon color="orange">fab fa-laravel</v-icon>-->
                <!--<v-icon color="green">fab fa-vuejs</v-icon>-->
                <!--<v-icon color="yellow darken-0">fab fa-js</v-icon>-->

                <v-flex xs12 sm7>
                  <v-card-text class="px-4">


                    <blockquote class="blockquote mb-4">
                      <div class="title font-weight-regular" style="margin-bottom:14px;">{{project.name}}</div>
                      <div class="body-2 font-weight-thin">{{project.description}}</div>

                    </blockquote>

                  </v-card-text>
                </v-flex>
                <v-divider light></v-divider>
              </v-layout>


              <v-layout fill-height row wrap align-end v-else>


                <v-flex xs12 sm7>
                  <v-card-text class="px-4">

                    <blockquote class="blockquote mb-4">
                      <div class="title font-weight-regular" style="margin-bottom:14px;">{{project.name}}</div>
                      <div class="body-2 font-weight-thin">{{project.description}}</div>
                    </blockquote>

                  </v-card-text>
                </v-flex>

                <v-flex xs12 sm5>
                  <v-card flat hover height="218" style="overflow:hidden !important;">


                    <v-system-bar height="22"   window dark lights-out style="background-color:rgba(0, 0, 0, .1) !important">

                      <v-icon style="font-size:12px;" color="red lighten-1">fas fa-circle</v-icon>
                      <v-icon style="font-size:12px;" color="orange lighten-1">fas fa-circle</v-icon>
                      <v-icon style="font-size:12px;" color="green lighten-1">fas fa-circle</v-icon>
                    </v-system-bar>

                    <v-card-media
                      style="
                      height: 228px;
                      background-position: center;
                      background-repeat: no-repeat;
                      text-rendering: optimizelegibility;
                      -webkit-font-smoothing: antialiased;
                      background-size: cover; "
                      :src="project.img"
                    >
                    </v-card-media>






                  </v-card>
                </v-flex>

              </v-layout>


            </v-card>

          </v-flex>



      </v-container>
    </div>
</template>

<script>
    export default {
        data : () => ({
            projects : [
                {
                  name : 'TARMAC',
                  img : 'https://cdn.vuetifyjs.com/images/home/vuetify_layout2.svg',
                  align : 'left',
                  description : `Lorem ipsum dolor sit amet, et magna omnes quodsi eum, utinam gloriatur quo id. Ex
                    'reque dissentiunt ius. Vel sale epicuri ex, te sit harum reformidans, pri ea clita vocent virtute. Cu quo inani probatus.`
                },
                {
                  name : 'EWS',
                  img : 'https://cdn.vuetifyjs.com/images/home/vuetify_layout2.svg',
                  align : 'right',
                  description : `Lorem ipsum dolor sit amet, et magna omnes quodsi eum, utinam gloriatur quo id. Ex
                      'reque dissentiunt ius. Vel sale epicuri ex, te sit harum reformidans, pri ea clita vocent virtute. Cu quo inani probatus.`
                },
                {
                  name : 'RFID',
                  img : 'https://cdn.vuetifyjs.com/images/home/vuetify_layout2.svg',
                  align : 'left',
                  description : `Lorem ipsum dolor sit amet, et magna omnes quodsi eum, utinam gloriatur quo id. Ex
                      'reque dissentiunt ius. Vel sale epicuri ex, te sit harum reformidans, pri ea clita vocent virtute. Cu quo inani probatus.`
                },
                {
                  name : 'Tailored for your team.',
                  img : 'https://cdn.vuetifyjs.com/images/home/vuetify_layout2.svg',
                  align : 'right',
                  description : `Lorem ipsum dolor sit amet, et magna omnes quodsi eum, utinam gloriatur quo id. Ex
                      'reque dissentiunt ius. Vel sale epicuri ex, te sit harum reformidans, pri ea clita vocent virtute. Cu quo inani probatus.`
                },
                {
                  name : 'BMS',
                  img : 'https://cdn.vuetifyjs.com/images/home/vuetify_layout2.svg',
                  align : 'left',
                  description : `Lorem ipsum dolor sit amet, et magna omnes quodsi eum, utinam gloriatur quo id. Ex
                      'reque dissentiunt ius. Vel sale epicuri ex, te sit harum reformidans, pri ea clita vocent virtute. Cu quo inani probatus.`
                },
                {
                  name : 'TESI Inventory',
                  img : 'https://cdn.vuetifyjs.com/images/home/vuetify_layout2.svg',
                  align : 'right',
                  description : `Lorem ipsum dolor sit amet, et magna omnes quodsi eum, utinam gloriatur quo id. Ex
                        'reque dissentiunt ius. Vel sale epicuri ex, te sit harum reformidans, pri ea clita vocent virtute. Cu quo inani probatus.`
                },

                // {img : 'https://lh3.googleusercontent.com/5L38nyXeoycmkug4P0UjpUr3y8qaw9kLTXh7W8Q4N2fSe8_DWF_vJB1eRAOclGJdKm1v89k9vd7MYCD2hlKk=w1853-h987-rw', align : 'right', name : 'EWS', description : 'Lorem ipsum dolor sit amet, et magna omnes quodsi eum, utinam gloriatur quo id. Ex reque dissentiunt ius. Vel sale epicuri ex, te sit harum reformidans, pri ea clita vocent virtute. Cu quo inani probatus.'},
                // {img : 'https://lh6.googleusercontent.com/1tGlv-b36Ew7Yi7kEJ4OhcFLg6WGM5QmCHr7VUwX7R5qawCnHeqOGdwDK-jrBD9MOnIzQ5mMBQzP275ntikm=w1853-h987-rw', align : 'left', name : 'BMS', description : 'Lorem ipsum dolor sit amet, et magna omnes quodsi eum, utinam gloriatur quo id. Ex reque dissentiunt ius. Vel sale epicuri ex, te sit harum reformidans, pri ea clita vocent virtute. Cu quo inani probatus.'},
                // {img : 'https://lh3.googleusercontent.com/xjOk8jc89YW97QevvD4_Gtfv4PvfhaxwPFblVnmO8qwSXbP1nkXc266JKCOsrcukdCACulwhL7b3G8FUwb38=w1853-h987-rw', align : 'right', name : 'RFID',description : 'Lorem ipsum dolor sit amet, et magna omnes quodsi eum, utinam gloriatur quo id. Ex reque dissentiunt ius. Vel sale epicuri ex, te sit harum reformidans, pri ea clita vocent virtute. Cu quo inani probatus.'},
                // {img : 'https://lh5.googleusercontent.com/K7pMfRZaAqqv6_FTmV-uEuDF5h92yEfrcQWOMUr5g_n0taBm9zyMB8x_Uq-Q3pEDMkild3Fz4TvWppMgL-ei=w1853-h987-rw', align : 'left', name : 'Nexus', description : 'Lorem ipsum dolor sit amet, et magna omnes quodsi eum, utinam gloriatur quo id. Ex reque dissentiunt ius. Vel sale epicuri ex, te sit harum reformidans, pri ea clita vocent virtute. Cu quo inani probatus.'},
                // {img : 'https://cdn.vuetifyjs.com/images/home/vuetify_layout2.svg', align : 'right', name : 'TESI Inventory', description : 'Lorem ipsum dolor sit amet, et magna omnes quodsi eum, utinam gloriatur quo id. Ex reque dissentiunt ius. Vel sale epicuri ex, te sit harum reformidans, pri ea clita vocent virtute. Cu quo inani probatus.'},
            ]
        })
    }
</script>   


<style scoped>


</style>
