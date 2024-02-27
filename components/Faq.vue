<template>
    <div>
        <div class="text-h4 font-weight-bold text-center mt-4 mb-2">Pergundas Frequentes</div>
        <v-container fluid>
        <v-row align="center" justify="center">
<v-col cols="12" md="11">
  <div>
    <v-expansion-panels>
      <v-expansion-panel>
        <v-expansion-panel-title  >
        O que é Arkos
        <template v-slot:actions="{ expanded }">
            <v-icon :color="!expanded ? 'red' : ''" :icon="expanded ? 'mdi-minus' : 'mdi-plus'"></v-icon>
          </template>
        
        </v-expansion-panel-title>
        <v-expansion-panel-text>
          Arkos é uma plataforma de serviços de engenharia e projetos. Um ecossitema construído por engenheiros, técnicos, arquitetos, empreiteiros, construtores, desenvolvedores e muito mais.
        </v-expansion-panel-text>
      </v-expansion-panel>

      <v-expansion-panel>
        <v-expansion-panel-title  >
     Quais serviços a plataforma oferece?<template v-slot:actions="{ expanded }">
            <v-icon :color="!expanded ? 'red' : ''" :icon="expanded ? 'mdi-minus' : 'mdi-plus'"></v-icon>
          </template>
          
        </v-expansion-panel-title>
        <v-expansion-panel-text>
     Dentro do ecossistema você encontra serviços de consultoria, projetos implantação e operação. Ou seja todo o ciclo de vida do projeto. 
        </v-expansion-panel-text>
      </v-expansion-panel>
      <v-expansion-panel>
        <v-expansion-panel-title  >
        Em que setor a Arkos atua?
        <template v-slot:actions="{ expanded }">
            <v-icon :color="!expanded ? 'red' : ''" :icon="expanded ? 'mdi-minus' : 'mdi-plus'"></v-icon>
          </template>
        </v-expansion-panel-title>
        <v-expansion-panel-text>
          Arkos atua como um hub de engenharia. Nossas soluções abrangem Energia, Infraestrutura, Construção, MEP, HVAC, Engenharia e Telecomunicações. Desde indústria até o varejo.        </v-expansion-panel-text>
      </v-expansion-panel>
      <v-expansion-panel>
        <v-expansion-panel-title  >
       Como receber um orçamento
        <template v-slot:actions="{ expanded }">
            <v-icon :color="!expanded ? 'red' : ''" :icon="expanded ? 'mdi-minus' : 'mdi-plus'"></v-icon>
          </template>
        </v-expansion-panel-title>
        <v-expansion-panel-text>
         Em poucos cliques você cadastra a sua solicitação em nossa plataforma e um especialista entrará em contato com você
        </v-expansion-panel-text>
      </v-expansion-panel>
      <v-expansion-panel>
        <v-expansion-panel-title  >
      Sou fornecedor como me cadastrar?
        <template v-slot:actions="{ expanded }">
            <v-icon :color="!expanded ? 'red' : ''" :icon="expanded ? 'mdi-minus' : 'mdi-plus'"></v-icon>
          </template>
        </v-expansion-panel-title>
        <v-expansion-panel-text>
         Para fazer parte do ecossistema Arkos entre em contato com nosso time. Preencha o cadastro como fornecedor e seja um parceiro credenciado
        </v-expansion-panel-text>
      </v-expansion-panel>
    
        
    </v-expansion-panels>
  </div>
</v-col>
</v-row>
</v-container>
</div>
</template>

<script>
export default {

}
</script>

<style>

</style>