
<template>
    <v-layout id="home">
  <v-main app class="bg-white mt-">
    <v-container class="mt-15">
    <v-row class="mt-15">
      <v-col cols="12">
        <v-row>
          <v-col cols="12" sm="12" md="6">
            <v-card-text>
              <div class="text-black"></div>
              </v-card-text>
            <h1 class="title1 text-h3 font-weight-black mt-5 mx-15">
              Soluções Práticas para problemas  complexos
            </h1>
            <p class="par1 ms-15">
              Provemos as melhores soluções de serviços de engenharia através de uma plataforma inteligente que vai desde o planejamento e projeto, até a implementação e operação.
            </p>
            <v-btn class="text-noe mt-8 bt1 mx-15" color="#E61428" size="x-large" variant="flat" rounded="0">
           conecte-se
            </v-btn>
           
          </v-col>
          <v-col cols="12" sm="12" md="6">
            <v-carousel
    cycle
    height="400"
    hide-delimiter-background
    show-arrows="hover">
  <v-carousel-item
    src="/engineer.jpg"
    cover
  ></v-carousel-item>

  <v-carousel-item
    src="/energy.jpg"
    cover
  ></v-carousel-item>

  <v-carousel-item
    src="/architect.jpg"
    cover
  ></v-carousel-item>
  <v-carousel-item
    src="/engineer2.jpg"
    cover
  ></v-carousel-item>
</v-carousel>
          </v-col>
        </v-row>
      </v-col>
      </v-row>
      </v-container>
      <v-container fluid class="mt-15">
    <v-row>
      <v-col cols="12">
        <v-row>
         
          <v-col cols="12" sm="12" md="6">
            <v-img height="500px" src="/arkos.png" class="img1"></v-img>
          </v-col>
          <v-col cols="12" sm="12" md="6">
            <v-card-text>
              <div class="text-black"></div>
              </v-card-text>
            <h1 class="title1 mt-15 text-h3 font-weight-black  ">
           Um ecossistema 
            de serviços feito sob medida para você
            </h1>
            <p class="par1 ">
             Em um mundo cada vez
                 mais complexo e em constante transformação
                  arkos nasce para ser um facilitador de negócios e construtor de ideias.
            </p>
            <v-btn class="text-noe mt-8 bt1 " color="#E61428" size="x-large" variant="flat" rounded="0">
              Conecte-se
            </v-btn>
         
          </v-col>
        </v-row>
      </v-col>
      <v-container>
      <v-row class="mt-15 justyfy-center align-center">
      <v-col cols="12" sm="12" md="3">
        <v-card
          class="mx-auto"
          max-width="344"
          color="#F4F6FA"
          flat
          height="300"
          rounded="lg"
      
          
         
        >
        <template v-slot:prepend>
         
         <v-icon color="black" size="60px" icon="mdi-account-tie"></v-icon>
    
     </template>
          <v-card-item>
            <div>
              <div class="text-overline mb-1">
                {{ variant }}
              </div>
              <div class="text-h6 mb-1">
             Consultoria
              </div>
              <div class="text-caption">Planejamento estratégico de todas as fases do empreendimento </div>
            </div>
          </v-card-item>

          
        </v-card>
      </v-col>
      <v-col cols="12" sm="12" md="3">
        <v-card
          class="mx-auto"
          max-width="344"
          color="#F4F6FA"
          flat
          height="300"
          rounded="lg"
          :variant="variant"
         
        >
        <template v-slot:prepend>
         
         <v-icon color="black" size="60px" icon="mdi-chart-timeline"></v-icon>
    
     </template>
          <v-card-item>
            <div>
              <div class="text-overline mb-1">
                {{ variant }}
              </div>
              <div class="text-h6 mb-1">
              Projetos
              </div>
              <div class="text-caption">
Possibilitamos a construção, montagem, funcionamento, manutenção e reparo de instalações e equipamentos</div>
            </div>
          </v-card-item>

         
        </v-card>
      </v-col>
     
      <v-col cols="12" sm="12" md="3">
        <v-card
          class="mx-auto"
          max-width="344"
          color="#F4F6FA"
          flat
          height="300"
          rounded="lg"
          :variant="variant"
         
        >
        <template v-slot:prepend>
         
         <v-icon color="black" size="60px" icon="mdi-cog-outline"></v-icon>
    
     </template>
          <v-card-item>
            <div>
              <div class="text-overline mb-1">
                {{ variant }}
              </div>
              <div class="text-h6 mb-1">
             Implantação
              </div>
              <div class="text-caption">Responsável por todo processo construtivo.</div>
            </div>
          </v-card-item>

         
        </v-card>
      </v-col>
      <v-col cols="12" sm="12" md="3">
        <v-card
          class="mx-auto"
          max-width="344"
          color="#F4F6FA"
          elevate="8"
          height="300"
          rounded="lg"
          :variant="variant"
         
        >
        <template v-slot:prepend>
         
         <v-icon color="black" size="60px" icon="mdi mdi-account-hard-hat-outline"></v-icon>
    
     </template>
          <v-card-item>
            <div>
              <div class="text-overline mb-1">
                {{ variant }}
              </div>
              <div class="text-h6 mb-1">
              Operação
              </div>
              <div class="text-caption">Garantimos que as operações diárias ocorram de maneira suave, segura e eficiente.</div>
            </div>
          </v-card-item>

          
        </v-card>
      </v-col>
    </v-row>
  </v-container>
      </v-row>
      
      </v-container>
  </v-main>
</v-layout>
</template>

<script>
export default {

}
</script>

<style>

</style>