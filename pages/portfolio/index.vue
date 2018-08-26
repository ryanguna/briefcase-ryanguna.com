<template>
    <div>
         <v-container
            fluid
            style="padding:0px;"
        >


         <div v-if="!$vuetify.breakpoint.xsOnly">

           <div v-for="project in projects" :key="project.name"  >

             <div v-if="project.align == 'left'" style="height:280px; border-bottom:1px solid #e1e1e1;">
               <v-layout row wrap align-end fill-height >
                 <v-flex xs12 sm5 >
                   <v-card hover flat height="220" style="overflow:hidden !important; ">
                     <v-system-bar height="22" style="background-color:rgba(0, 0, 0, .1) !important"  window dark lights-out >
                       <v-icon style="font-size:12px;" color="red lighten-1">fas fa-circle</v-icon>
                       <v-icon style="font-size:12px;" color="orange lighten-1">fas fa-circle</v-icon>
                       <v-icon style="font-size:12px;" color="green lighten-1">fas fa-circle</v-icon>
                     </v-system-bar>
                     <v-card-media
                       style="
                          height: 200px;
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
                 <v-flex xs12 sm7 >
                   <v-card-text class="px-4" >
                     <blockquote class="blockquote mb-3">
                       <div class="title font-weight-regular"  style="margin-bottom:12px;">{{project.name}}</div>
                       <div class="caption font-weight-thin">{{project.description}}</div>
                     </blockquote>

                   </v-card-text>
                 </v-flex>
                 <v-divider light></v-divider>
               </v-layout>
             </div>


             <div v-else style="height:290px; border-bottom:1px solid #e1e1e1;">
               <v-layout row wrap align-end fill-height >

                 <v-flex xs12 sm7 >

                   <v-card-text class="px-4">
                     <blockquote class="blockquote mb-3">
                       <div class="title font-weight-regular"  style="margin-bottom:12px;">{{project.name}}</div>
                       <div class="caption font-weight-thin">{{project.description}}</div>
                     </blockquote>

                   </v-card-text>

                 </v-flex>

                 <v-flex xs12 sm5>
                   <v-card hover flat height="220" style="overflow:hidden !important; ">
                     <v-system-bar height="22" style="background-color:rgba(0, 0, 0, .1) !important"  window dark lights-out >
                       <v-icon style="font-size:12px;" color="red lighten-1">fas fa-circle</v-icon>
                       <v-icon style="font-size:12px;" color="orange lighten-1">fas fa-circle</v-icon>
                       <v-icon style="font-size:12px;" color="green lighten-1">fas fa-circle</v-icon>
                     </v-system-bar>
                     <v-card-media
                       style="
                          height: 200px;
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
                 <v-divider light></v-divider>
               </v-layout>
             </div>

           </div>

         </div>


         <div v-else>

             <div v-for="project in projects" :key="project.name" >

               <v-layout row wrap align-end fill-height>

                 <v-flex xs12 sm5 >
                   <v-card hover flat height="220" style="overflow:hidden !important; ">
                     <v-system-bar height="22" style="background-color:rgba(0, 0, 0, .1) !important"  window dark lights-out >
                       <v-icon style="font-size:12px;" color="red lighten-1">fas fa-circle</v-icon>
                       <v-icon style="font-size:12px;" color="orange lighten-1">fas fa-circle</v-icon>
                       <v-icon style="font-size:12px;" color="green lighten-1">fas fa-circle</v-icon>
                     </v-system-bar>
                     <v-card-media
                       style="
                      height: 220px;
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
                 <v-flex xs12 sm7>
                   <v-card  flat height="400">
                     <v-card-text class="px-3">
                       <blockquote class="blockquote mb-4">
                         <div class="title font-weight-regular"  style="margin-bottom:12px;">{{project.name}}</div>
                         <div class="body-2 font-weight-thin">{{project.description}}</div>
                       </blockquote>

                     </v-card-text>
                   </v-card>
                 </v-flex>
                 <v-divider light></v-divider>
               </v-layout>
             </div>
           </div>








      </v-container>
    </div>
</template>

<script>
    export default {
        data : () => ({
            projects : [
                {
                  name : 'TARMAC',
                  img : require('@/static/TARMAC.png'),
                  align : 'left',
                  description : `TARMAC is web service that can display the status, light activity and sensor activity of field Traffic Controllers. The user can also issue control commands and override the operation of a particular Traffic Controller. It provides real-time traffic monitoring and analytics. It can also connect to field Power Plant devices, to control and monitor power related settings in traffic controllers.`
                },

                {
                  name : 'EWS',
                  img : require('@/static/EWS.png'),
                  align : 'right',
                  description : `The system serves as a hub where all the data pertaining to EWS passes through, stored, processed, and converted to actionable information to aiding disaster mitigation and evacuation. The purpose is to bring the separate EWS detection systems (Monitoring Stations, Evacuation Stations, Monitoring Panels, Evacuation Panels, Weather Displays etc.) to operate coherently and in unison for the sole purpose and objective of detecting imminent threat of flash flood and other water-related disaster ahead of time, and to aid in evacuation of people in low-lying areas.
`
                },
              {
                name : 'RFID Vehicle Management',
                img : require('@/static/RFID.png'),
                align : 'left',
                description : `The RFID Vehicle Management help parking areas or gated communities to monitor/manage the entry of vehicles without human intervention as well as easy in-and-out access for drivers. Vehicle informations are automated gathered to enable vehicle management to be more efficient and safe. `
              },
              {
                name : 'Teknovarik Building Management System (BMS)',
                img : require('@/static/BMS.png'),
                align : 'right',
                description : `A System that serves as a digital hub and center of connectivity of a building.
Enables efficient management, regulation, and intelligent control of the building from a central computer, tablet of a modern room panel with touch screen.
Real-time process management, parameter monitoring and parameter control. All programmable controllers of the building’s various subsystems (heating, cooling, lighting, blinds, etc.) are combined in one integral whole.`
              },
              {
                name : 'TARMAC Mapboard Kiosk',
                img : 'https://cdn.vuetifyjs.com/images/home/vuetify_layout2.svg',
                align : 'left',
                description : `An interactive kiosk machine deployed on a raspberry pi device  featuring specialized hardware and software that provides access to information from the TARMAC server.`
              },

                {
                  name : 'Nexus',
                  img : require('@/static/Nexus.png'),
                  align : 'right',
                  description : `A web service designed to be the operational hub of the company. Streamlines and consolidates operational tasks into one cohesive system that will govern the employees in carrying out their duties and responsibilities, and provide a way to curtail deviations and improvisations from the set procedures. Provides a way to track all production items and all processes.`
                },

              {
                name : 'TESI Inventory and Tool Management System',
                img : 'https://cdn.vuetifyjs.com/images/home/vuetify_layout2.svg',
                align : 'left',
                description : `TESI  effectively keeps track and manages tools, assets, inventory and equipments for the company.
`
              },



                // {img : 'https://lh3.googleusercontent.com/5L38nyXeoycmkug4P0UjpUr3y8qaw9kLTXh7W8Q4N2fSe8_DWF_vJB1eRAOclGJdKm1v89k9vd7MYCD2hlKk=w1853-h987-rw', align : 'right', name : 'EWS', description : 'Lorem ipsum dolor sit amet, et magna omnes quodsi eum, utinam gloriatur quo id. Ex reque dissentiunt ius. Vel sale epicuri ex, te sit harum reformidans, pri ea clita vocent virtute. Cu quo inani probatus.'},
                // {img : 'https://lh6.googleusercontent.com/1tGlv-b36Ew7Yi7kEJ4OhcFLg6WGM5QmCHr7VUwX7R5qawCnHeqOGdwDK-jrBD9MOnIzQ5mMBQzP275ntikm=w1853-h987-rw', align : 'left', name : 'BMS', description : 'Lorem ipsum dolor sit amet, et magna omnes quodsi eum, utinam gloriatur quo id. Ex reque dissentiunt ius. Vel sale epicuri ex, te sit harum reformidans, pri ea clita vocent virtute. Cu quo inani probatus.'},
                // {img : 'https://lh3.googleusercontent.com/xjOk8jc89YW97QevvD4_Gtfv4PvfhaxwPFblVnmO8qwSXbP1nkXc266JKCOsrcukdCACulwhL7b3G8FUwb38=w1853-h987-rw', align : 'right', name : 'RFID',description : 'Lorem ipsum dolor sit amet, et magna omnes quodsi eum, utinam gloriatur quo id. Ex reque dissentiunt ius. Vel sale epicuri ex, te sit harum reformidans, pri ea clita vocent virtute. Cu quo inani probatus.'},
                // {img : 'https://lh5.googleusercontent.com/K7pMfRZaAqqv6_FTmV-uEuDF5h92yEfrcQWOMUr5g_n0taBm9zyMB8x_Uq-Q3pEDMkild3Fz4TvWppMgL-ei=w1853-h987-rw', align : 'left', name : 'Nexus', description : 'Lorem ipsum dolor sit amet, et magna omnes quodsi eum, utinam gloriatur quo id. Ex reque dissentiunt ius. Vel sale epicuri ex, te sit harum reformidans, pri ea clita vocent virtute. Cu quo inani probatus.'},
                // {img : 'https://cdn.vuetifyjs.com/images/home/vuetify_layout2.svg', align : 'right', name : 'TESI Inventory', description : 'Lorem ipsum dolor sit amet, et magna omnes quodsi eum, utinam gloriatur quo id. Ex reque dissentiunt ius. Vel sale epicuri ex, te sit harum reformidans, pri ea clita vocent virtute. Cu quo inani probatus.'},
            ]
        }),
      head () {
        return {
          title: 'Ryan Guna | Portfolio',
          meta: [
            { hid: 'description', name: 'Portfolio section', content: 'My Portfolio' }
          ]
        }
      }
    }
</script>   


<style scoped>


</style>
