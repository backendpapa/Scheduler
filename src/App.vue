<template>
  <v-app class="animate__animated animate__fadeIn animate__slow">
    <v-app-bar
      app
      color="white"
      flat
    >
      <div class="mt-6">
       <v-text-field prepend-inner-icon="mdi-magnify" flat  placeholder="Search Categories" class="text-caption" clearable solo dense></v-text-field>
      </div>

      <v-spacer></v-spacer>

      <v-btn color="#70D25F" style="text-transform:none" class="text-caption" dark>Create <v-icon>mdi-chevron-down</v-icon></v-btn>
      <v-btn plain class="ml-2" small icon><v-icon>mdi-bell-badge-outline</v-icon></v-btn>

    </v-app-bar>

    <v-navigation-drawer
        
        width="250"
        color="#0286C2"
        app
        class="d-none d-sm-flex"
      >
       <div style="height:10.3vh;background-color:#0078AE;color:white" class="">
         <v-row no-gutters style="height:100%" align="center" class="ml-4">
           <v-avatar size="40">
             <v-img src="https://images.unsplash.com/flagged/photo-1570612861542-284f4c12e75f?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=870&q=80"></v-img>
           </v-avatar>
           <div class="ml-1 mt-4">
             <p class="text-caption mb-n2 font-weight-bold">Backend Papa</p>
             <p class="text-caption ">Abuja</p>
           </div>
           <div>
             <v-btn icon small plain><v-icon color="white">mdi-chevron-down</v-icon></v-btn>
           </div>
         </v-row>
       </div>

        <v-list
          nav
          dense
          v-for="i in items" :key="i"
         
        
        >
          <v-list-item :to="i.to" link>
            <v-list-item-icon>
              <v-icon color="white">{{i.icon}}</v-icon>
            </v-list-item-icon>
            <v-list-item-title  style="color:white">{{i.title}}</v-list-item-title>
          </v-list-item>
         
          
        </v-list>
      </v-navigation-drawer>

    <v-main>
      <router-view/>
    </v-main>
  </v-app>
</template>

<script>
import "./App.css"
export default {
  name: 'App',

  data: () => ({
    //
    items:[
      {title:"Dashboard",icon:"mdi-view-dashboard",to:"/"},
      {title:"Campaigns",icon:"mdi-thermostat",to:"/campaigns"},
      {title:"List",icon:"mdi-list-status",to:"/list"},
      {title:"Subscribers",icon:"mdi-account-arrow-right-outline",to:"/subscribers"},
      {title:"Settings",icon:"mdi-cog-outline",to:"/settings"},
      
    ]
  }),
};
</script>
