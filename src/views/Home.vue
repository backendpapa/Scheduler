<template>
<div class="pa-3">
 <v-container>
   <div class="d-none d-sm-flex">
    <v-row no-gutters >
    <p class="text-body-1 font-weight-bold">35 Campaigns</p>
    <v-spacer></v-spacer>
    
    <v-select
    solo
    dense
    flat
    style="min-width:10px;max-width:120px;font-size:10px"
    class="mr-2 text-caption"

    label="Date Created"
    
    ></v-select>
    <v-select
    solo
    dense
    flat
    style="min-width:10px;max-width:100px"
    class=" text-caption wn"
    label="By Status"
    
    
    ></v-select>
    <v-btn class="mr-1" icon ><v-icon>mdi-view-dashboard</v-icon></v-btn>
     <v-btn class="mr-1" icon ><v-icon>mdi-view-headline</v-icon></v-btn>
    
  </v-row>
   </div>
  <div class="d-flex d-sm-none">
    <div>
      <p class="text-body-1 font-weight-bold">35 Campaigns</p>
    <v-row no-gutters>
       <v-select
    solo
    dense
    flat
    style="min-width:10px;max-width:120px;font-size:10px"
    class="mr-2 text-caption"

    label="Date Created"
    
    ></v-select>
    <v-select
    solo
    dense
    flat
    style="min-width:10px;max-width:100px"
    class=" text-caption wn"
    label="By Status"
    
    
    ></v-select>
    <v-btn class="mr-1" icon ><v-icon>mdi-view-dashboard</v-icon></v-btn>
     <v-btn class="mr-1" icon ><v-icon>mdi-view-headline</v-icon></v-btn>
    </v-row>
    </div>
  </div>
  <v-row >
      <v-col cols="12" xl="3" lg="3" v-for="i in 24" :key="i">
        <v-card class="pa-2 " flat>
          <v-chip color="blue" class="mb-2" dark small>RUNNING</v-chip>
          <p class="font-weight-bold">Sed ut perpspecitis</p>
          <p class="text-caption font-weight-bold grey--text mt-n4">March 21,2022 10:34 PM</p>
          <p class="text-body-2 grey--text">Lorem ipsum dolor sit amet consectetur adipisicing elit. Dolorem ut iusto veritatis nobis inventore laborum.</p>
          <br>
          <p class="text-caption font-weight-bold mt-n3 grey--text" >LST</p>
          <p class="text-caption font-weight-bold mt-n4">Product Growth</p>
          <p class="text-caption grey--text font-weight-bold">KEYWORD</p>
          <v-row no-gutters>
            <v-chip outlined color="blue" class="mr-1 text-caption font-weight-bold" small>WONDER</v-chip>
            <v-chip outlined color="blue" class="text-caption font-weight-bold" small>SMS</v-chip>
          </v-row>
        </v-card>
      </v-col>
  </v-row>
 </v-container>
</div>
</template>

<script>


  export default {
    name: 'Home',

    components: {
     
    },
  }
</script>
<style>


</style>
