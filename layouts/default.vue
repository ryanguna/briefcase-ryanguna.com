<template>
  <v-app>
    <v-content>
      <v-container fluid grid-list-xs style="padding:0px;">
        <!--<v-parallax height="300" src="https://cdn.vuetifyjs.com/images/parallax/material.jpg"></v-parallax>-->

        <!--<v-parallax height="600" src="https://i.imgur.com/OuSizUw.jpg"></v-parallax>-->
          <v-layout row >
            <v-flex xs12 sm6 offset-xs0 offset-sm3 align-center>
              <v-card  class="card--flex-toolbar" >
                <v-toolbar card prominent height="280" tabs extended >
                 <personal-info></personal-info>
                  <v-tabs
                    fixed-tabs
                    slot="extension"
                    centered
                    color="transparent"
                  >
                    <v-tabs-slider></v-tabs-slider>
                    <v-tab to="/portfolio" router class="primary--text">My Portfolio</v-tab>
                    <v-tab to="/home" router class="primary--text"> Showcase</v-tab>
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
    margin-top: 200px;
  }
</style>

