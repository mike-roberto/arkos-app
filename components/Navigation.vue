<template>
   
    <v-layout>
  <v-navigation-drawer
    v-model="drawer"
    app
    temporary
    dark
    src="@/assets/img/bgDrawer.jpg"
  >
    <v-list>
      <v-list-item>
        <v-list-item-avatar>
          <img height="100%" src="/keeplace.png" alt="Logo" />
        </v-list-item-avatar>
        <v-list-item-content>
          <v-list-item-title class="title">Calango</v-list-item-title>
          <v-list-item-subtitle>WEB</v-list-item-subtitle>
        </v-list-item-content>
      </v-list-item>
    </v-list>
  
    <v-divider />
  
    <v-list dense>
      <v-list-item
        v-for="([icon, text, link], i) in items"
        :key="i"
        link
        @click="$vuetify.goTo(link)"
      >
        <v-list-item-icon class="justify-center">
          <v-icon>{{ icon }}</v-icon>
        </v-list-item-icon>
        <v-list-item-content>
          <v-list-item-title class="subtitile-1">{{
            text
          }}</v-list-item-title>
        </v-list-item-content>
      </v-list-item>
    </v-list>
  </v-navigation-drawer>
  
  <v-app-bar
   height="80"
    app
  
    scroll-behavior="elevate"
    dark
    class="px-15 bg-white"
   
  >
  
      <v-toolbar-title class="text-h5 font-weight-bold">Arkos <v-img src="" width="350px" /></v-toolbar-title>
  
  <!--    <v-toolbar-title>
      <v-img src="@/assets/img/origemlogo.jpeg" max-width="200px" />
    </v-toolbar-title>-->
   <!-- <v-toolbar-title>
      <v-img src="@/assets/img/cury.jpg" max-width="100px" />
    </v-toolbar-title>-->
    <v-spacer />
    <v-app-bar-nav-icon
      @click.stop="drawer = !drawer"
      class="mr-4"
      v-if="isXs"
    />
    <div v-else>
    
        <v-menu>
          
  <template v-slot:activator="{ props }">
  
    <v-btn
      color="black"
      v-bind="props"
    >
  
    <span>Quem Somos</span> &nbsp; <v-icon color="indigo" start  icon="mdi-chevron-down"></v-icon>
    </v-btn>
  </template>
  
  <v-card 
  width="400px">
  <v-container fluid>
    <v-row>
      <v-col cols="12" md="6">
  <v-list density="compact">
    <v-list-subheader class="weight-text-bold">Rio de Janeiro</v-list-subheader>
    <v-list-item
      v-for="(buy, index) in buys"
      :key="index"
      :value="index"
    >
      <v-list-item-title>{{ buy.title }}</v-list-item-title>
    </v-list-item>
  </v-list>
  </v-col>
  <v-col cols="12" md="6">
  <v-list density="compact">
    <v-list-subheader></v-list-subheader>
    <v-list-item
      v-for="(other, index) in others"
      :key="index"
      :value="index"
    >
      <v-list-item-title>{{ other.title }}</v-list-item-title>
    </v-list-item>
  </v-list>
  </v-col>
  </v-row>
  </v-container>
  </v-card>
  </v-menu>
  
  <v-menu>
  <template v-slot:activator="{ props }">
    <v-btn
      color="black"
      v-bind="props"
    >
     <span>Soluçoes</span> &nbsp; <v-icon color="indigo" start  icon="mdi-chevron-down"></v-icon>
    </v-btn>
  </template>
  <v-list>
    <v-list-item
      v-for="(sell, index) in sells"
      :key="index"
      :value="index"
    >
      <v-list-item-title>{{ sell.title }}</v-list-item-title>
    </v-list-item>
  </v-list>
  </v-menu>
  <v-menu>
  <template v-slot:activator="{ props }">
    <v-btn
      color="black"
      v-bind="props"
    >
      
     <span>Setores</span> &nbsp; <v-icon color="indigo" start  icon="mdi-chevron-down"></v-icon>
    </v-btn>
  </template>
  <v-list>
    <v-list-item
      v-for="(skill, index) in skills"
      :key="index"
      :value="index"
    >
      <v-list-item-title>{{ skill.title }}</v-list-item-title>
    </v-list-item>
  </v-list>
  </v-menu>
  <v-menu>
  <template v-slot:activator="{ props }">
    <v-btn
      color="black"
      v-bind="props"
    >
      
     <span>Ferramentas</span> &nbsp; <v-icon color="indigo" start  icon="mdi-chevron-down"></v-icon>
    </v-btn>
  </template>
  <v-list>
    <v-list-item
      v-for="(partner, index) in partners"
      :key="index"
      :value="index"
    >
      <v-list-item-title>{{ partner.title }}</v-list-item-title>
    </v-list-item>
  </v-list>
  </v-menu>
  <v-menu>
  <template v-slot:activator="{ props }">
    <v-btn
      color="black"
      v-bind="props"
    >
      
     <span>Insights</span> &nbsp; <v-icon color="indigo" start  icon="mdi-chevron-down"></v-icon>
    </v-btn>
  </template>
  <v-list>
    <v-list-item
      v-for="(more, index) in mores"
      :key="index"
      :value="index"
    >
      <v-list-item-title>{{ more.title }}</v-list-item-title>
    </v-list-item>
  </v-list>
  </v-menu>
  
  <v-btn
      color="indigo"
     
    >
  
    <span>Entrar</span> &nbsp; <v-icon color="indigo" start  icon="mdi-login"></v-icon>
    </v-btn>
  
    </div>
  
  </v-app-bar>
  </v-layout>
  </template>
  
  <style scoped>
  .v-toolbar {
  transition: 0.6s;
  }
  
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
    ["mdi-home-outline", "Sobre", "#hero"],
    ["mdi-information-outline", "Plantas", "#features"],
    ["mdi-download-box-outline", "Construtora", "#download"],
    ["mdi-currency-usd", "Preços", "#pricing"],
    ["mdi-email-outline", "Contato", "#contact"],
  ],
  buys: [
    { title: 'Leblon' },
    { title: 'Ipanema' },
    { title: 'Copacabana' },
    { title: 'Leme' },
    { title: 'Botafogo' },
    { title: 'Flamengo' },
    { title: 'Laranjeiras' },
    { title: 'Catete' },
    ],
  others: [
    { title: 'Largo do Machado' },
    { title: 'Tijuca' },
    { title: 'Grajaú' },
    { title: 'Centro' },
    { title: 'Barra da Tijuca' },
    { title: 'Recreio' },
    { title: 'Jacarepaguá' },
    { title: 'São Cristóvão' },
    ],
  
  sells: [
    { title: 'Quero Vender' },
    { title: 'Avaliação do Imóvel' },
    { title: 'Como vender' },
   
  ],
  skills: [
    { title: 'Avaliação de Imóvel' },
    { title: 'Comprar' },
    { title: 'Alugar' },
    { title: 'Onde Morar' },
  ],
  partners: [
    { title: 'Assessoria de Crédito' },
    { title: 'Corretores' },
    { title: 'Arquitetos' },
    { title: 'Reformas' },
  ],
  mores: [
    { title: 'Crédito' },
    { title: 'Sobre ' },
    { title: 'Carreiras' },
    { title: 'Blog' },
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