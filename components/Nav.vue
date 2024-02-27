<template>
    <v-layout>
       <div>
    
     <v-navigation-drawer
       v-model="drawer"
       app
       temporary
       dark
       src=""
     >
       <v-list>
         <v-list-item>
           <v-list-item-avatar>
             <img src="/arkoslogo.png" alt="Logo" />
           </v-list-item-avatar>
           <v-list-item-content>
             <v-list-item-title class="title">Arkos</v-list-item-title>
             <v-list-item-subtitle>App</v-list-item-subtitle>
           </v-list-item-content>
         </v-list-item>
       </v-list>
 
       <v-divider />
 
       <v-list dense>
         <v-list-item
          
         >
          <a href="#home"> <v-btn flat text >
           <span class="mr-2 text-black">home</span>
         </v-btn></a>
       </v-list-item>
       <v-list-item
          
          >
         <a href="#sobre"> <v-btn  flat text >
           <span class="mr-2 text-black">Sobre</span>
         </v-btn></a> </v-list-item>
         <v-list-item
          
          >
         <a href="#wedo"> <v-btn flat text>
           <span class="mr-2 text-black">o que fazemos</span>
         </v-btn></a></v-list-item>
         <v-list-item
          
          >
         <a href="#partners"><v-btn flat text>
           <span class="mr-2 text-black">parceiros</span>
         </v-btn></a></v-list-item>
 
         <v-list-item >
         <a href="#blog"><v-btn flat text>
           <span class="mr-2 text-black">News</span>
         </v-btn></a></v-list-item>
         <v-list-item >
         <a href="#contact"><v-btn flat outlined text >
           <span class="mr-2 text-black">Contate-nos</span>
         </v-btn></a></v-list-item>
         <v-list-item
          
          >
         <v-btn class="text-noe" color="#E61428" rounded="0" variant="outlined"  @click="$vuetify.goTo('#contact')">
           <span class="mr-2">login</span><v-icon color="#E61428">mdi-login</v-icon>
         </v-btn>
         
         </v-list-item>
       </v-list>
     </v-navigation-drawer>
 
     <v-app-bar
       app
       :color="color"
       :flat="flat"
       dark
       class="px-15"
       :class="{ expand: flat }"
     >
       <v-toolbar-title>
         <v-img  src="/arkoslogo.png" width="130px" />
       </v-toolbar-title>
       <v-spacer />
       <v-app-bar-nav-icon
         @click.stop="drawer = !drawer"
         class="mr-4"
         v-if="isXs"
       />
       <div v-else>
         <a href="#home"> <v-btn text >
           <span class="mr-2 text-black">home</span>
         </v-btn></a>
         <a href="#sobre"> <v-btn text >
           <span class="mr-2 text-black">Sobre</span>
         </v-btn></a>
         <a href="#wedo"> <v-btn text>
           <span class="mr-2 text-black">o que fazemos</span>
         </v-btn></a>
         <a href="#partners"><v-btn text>
           <span class="mr-2 text-black">parceiros</span>
         </v-btn></a>
         <a href="#blog"><v-btn text>
           <span class="mr-2 text-black">News</span>
         </v-btn></a>
         <a href="#contact"><v-btn rounded outlined text >
           <span class="mr-2 text-black">Contate-nos</span>
         </v-btn></a>
         <v-btn class="text-noe" color="#E61428" rounded="0" variant="outlined"  @click="$vuetify.goTo('#contact')">
           <span class="mr-2">login</span><v-icon color="#E61428">mdi-login</v-icon>
         </v-btn>
       </div>
     </v-app-bar>
   </div>
 </v-layout>
 </template>
 
 <style scoped>
 .v-toolbar {
   transition: 0.6s;
 }
 .v-list-item-content { text-decoration-line: none;}
 .expand {
   height: 80px !important;
   padding-top: 10px;
 }
 </style>
 
 <script>
 export default {
   data: () => ({
     drawer: null,
     isXs: false,
     items: [
       ["mdi-home-outline", "Home", "#sobre"],
       ["mdi-information-outline", "Sobre", "#features"],
       ["mdi-download-box-outline", "Download", "#download"],
       ["mdi-currency-usd", "Preços", "#pricing"],
       ["mdi-email-outline", "Contatos", "#contact"],
     ],
   }),
   props: {
     color: String,
     flat: Boolean,
   },
   methods: {
     onResize() {
       this.isXs = window.innerWidth < 850;
     },
   },
 
   watch: {
     isXs(value) {
       if (!value) {
         if (this.drawer) {
           this.drawer = false;
         }
       }
     },
   },
   mounted() {
     this.onResize();
     window.addEventListener("resize", this.onResize, { passive: true });
   },
 };
 </script>