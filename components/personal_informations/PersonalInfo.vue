<template>
<div>
  <v-layout row >

    <v-flex xs2>
      <blockquote class="blockquote ">
        <v-avatar  size="120"   style="margin-top:5px; " >
          <img :src="profile.avatar" alt="avatar">
        </v-avatar>
      </blockquote>

    </v-flex>

    <v-flex xs10 align-left text-xs-left>


      <v-card-text>

        <blockquote class="blockquote">

          <div class="headline font-weight-regular" >{{profile.name}}</div>

          <div class="caption font-weight-medium">{{profile.position}}</div>

          <div class="caption font-weight-thin">{{profile.aboutMe}}</div>


        </blockquote>

      </v-card-text>



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
                            and learn new languages or technologies.`,
                    avatar : 'https://media.licdn.com/dms/image/C5603AQE3jR0rFggAqA/profile-displayphoto-shrink_200_200/0?e=1536192000&v=beta&t=nfw0mG8TQilFDHNKEzkjhBaW9oKTjZUeP_Uje3zz7Xs',
                }
            }
        }
    }
</script>
