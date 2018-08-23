<template>
<div>
    <v-layout row pb-2 >
            <v-flex xs8 offset-xs2 align-center text-xs-center>
             <div style="text-align:center;">
                 <div >
                    <v-avatar size="120"  color="grey lighten-4" >
                    <img :src="profile.avatar" alt="avatar">
                     </v-avatar>
                  </div>


    
<v-card-text>
      <p class="text-md-center headline">{{profile.name}}</p>
      <p class="text-md-center font-weight-medium">{{profile.position}}</p>
     <p class="text-md-center font-weight-light">{{profile.aboutMe}}</p>
      <v-btn flat icon color="red lighten-2">
                        <v-icon>fab fa-github</v-icon>
                      </v-btn>
                      <v-btn flat icon color="red lighten-2">
                        <v-icon>fab fa-linkedin</v-icon>
                      </v-btn>
</v-card-text>


             </div>
            </v-flex>
          </v-layout>
</div>
    

</template>

<script>
    export default {
        data(){
            return {
                activeTab : '',
                profile : {
                    name : 'Ryan Gunawardana',
                    position : 'Full Stack Lead Developer',
                    aboutMe : `An open source contributor, I strive for sustainable and process-oriented development, love collaborating on challenging projects, mentor and be mentored 
                            and learn new languages or technologies — for a project or just for fun. I look for a long-term, thought-out solution when it benefits the business.`,
                    avatar : 'https://media.licdn.com/dms/image/C5603AQE3jR0rFggAqA/profile-displayphoto-shrink_200_200/0?e=1536192000&v=beta&t=nfw0mG8TQilFDHNKEzkjhBaW9oKTjZUeP_Uje3zz7Xs',
                }
            }
        }
    }
</script>