<template>
  <v-app>
    <v-content >
      <v-container fluid  style="padding:0px;">
        <!--<v-parallax height="300" src="https://cdn.vuetifyjs.com/images/parallax/material.jpg"></v-parallax>-->

        <!--<v-parallax height="600" src="http://annwalls.xyz/wp-content/uploads/2018/03/Sunrise-Mountain-Landscape-Wallpaper.jpg"></v-parallax>-->



        <v-layout wrap row >

          <v-flex xs12 sm12 md10 lg6 offset-xs0 offset-sm0 offset-md1 offset-lg3 >
            <personal-info></personal-info>
          </v-flex>


            <v-flex xs12 sm12 md10 lg6 offset-xs0 offset-sm0 offset-md1 offset-lg3 >
              <v-card  >
                <v-divider></v-divider>
                <v-tabs
                  right
                >
                  <v-tabs-slider></v-tabs-slider>

                  <v-tab to="/portfolio" router class="body-1" style="text-transform : capitalize">Portfolio</v-tab>

                  <v-tab to="/crafts" router class="body-1" style="text-transform : capitalize">   Crafts</v-tab>
                  <v-divider vertical></v-divider>


                  <v-tooltip bottom>
                    <v-btn slot="activator" flat icon color="grey darken-2" @click="openLink('https://github.com/ryanguna')">
                      <v-icon>fab fa-github</v-icon>
                    </v-btn>
                    <span>ryanguna@github</span>
                  </v-tooltip>


                  <v-divider vertical></v-divider>




                  <v-tooltip bottom>
                    <v-btn slot="activator" flat icon color="grey darken-2" @click="openLink('https://linkedin.com/in/ryanguna')" >
                      <v-icon>fab fa-linkedin</v-icon>
                    </v-btn>
                    <span>ryanguna@linkedin</span>
                  </v-tooltip>

                  <v-divider vertical></v-divider>




                </v-tabs>
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
  },
  methods : {
    openLink(link){
      window.open(link, '_blank');
    }
  }
}
</script>

<style>
 .card--flex-toolbar {
    margin-top: 120px;
   padding:0px;
  }
 .application {
   font-family: "Whitney SSm A","Whitney SSm B",sans-serif !important;
   line-height: 1.8;
 }


</style>

