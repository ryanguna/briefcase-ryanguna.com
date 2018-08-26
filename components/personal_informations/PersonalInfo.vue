<template>
<div>
  <v-card>
  <v-layout row wrap>


    <v-flex xs12 sm2 text-xs-center >
      <v-avatar  size="110"   style="margin-top:36px; " >
        <img :src="profile.avatar" alt="avatar">
      </v-avatar>

    </v-flex>

    <v-flex xs12 sm10 align-left text-xs-center text-sm-left>


      <v-card-text>

        <blockquote class="blockquote">

          <div class="headline font-weight-regular" >{{profile.name}}</div>

          <div class="subheading font-weight-regular">{{profile.position}}</div>
          <div class="caption font-weight-medium">
            <v-icon size="12">fas fa-envelope</v-icon>
            ryanmgunawardana@gmail.com</div>


          <div class="caption font-weight-thin">{{profile.aboutMe}}</div>


        </blockquote>

      </v-card-text>



    </v-flex>

  </v-layout>
  </v-card>
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
