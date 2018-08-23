<template>
  <v-app>
    <v-content>
      <v-container fluid  style="padding:0px;">
        <!--<v-parallax height="300" src="https://cdn.vuetifyjs.com/images/parallax/material.jpg"></v-parallax>-->

        <!--<v-parallax height="600" src="https://i.imgur.com/OuSizUw.jpg"></v-parallax>-->
          <v-layout row style="padding:0px;">
            <v-flex xs12 sm12 md10 lg6 offset-xs0 offset-sm0 offset-md1 offset-lg3 >
              <v-card  class="card--flex-toolbar" >
                <v-toolbar card prominent height="200"  style="background-color:#f7f7f7e3"  tabs extended >
                 <personal-info></personal-info>


                  <v-tabs
                    slot="extension"
                    right
                  >
                    <v-tabs-slider></v-tabs-slider>

                    <v-tab to="/portfolio" router class="body-1" style="text-transform : capitalize">Portfolio</v-tab>

                    <v-tab to="/home" router class="body-1" style="text-transform : capitalize"> Showcase</v-tab>
                    <v-divider vertical></v-divider>
                    <v-btn flat icon color="grey darken-2">
                      <v-icon>fab fa-github</v-icon>
                    </v-btn>
                    <v-divider vertical></v-divider>
                    <v-btn flat icon color="grey darken-2">
                      <v-icon>fab fa-linkedin</v-icon>
                    </v-btn>

                  </v-tabs>

                </v-toolbar>
                <v-divider></v-divider>
                <nuxt/>
              </v-card>
            </v-flex>
          </v-layout>
      </v-container>
    </v-content>
  </v-app>
</template>

<script>
import PersonalInfo from '@/components/personal_informations/PersonalInfo.vue'
export default {
  data(){
    return {
    }
  },
  components : {
    PersonalInfo
  }
}
</script>

<style>
 .card--flex-toolbar {
    margin-top: 150px;
   padding:0px;
  }
 .application {
   font-family: "Whitney SSm A","Whitney SSm B",sans-serif !important;
   line-height: 1.8;
 }


</style>

