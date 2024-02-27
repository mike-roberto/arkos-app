<template>
    <v-container>
        <v-row align="center" justify="center" >
            <v-col cols="12" sm="10">
              <v-card flat class=" "  >
               <v-window v-model="step">
                  <v-window-item :value="1">
                    <v-row>
                      <v-col cols="12" md="6">
                        <v-card-text class="mt-12">
                          <h2
                            class="text-center display-2"
                          >Deseja receber um orçamento?</h2>
                          <h6
                            class="text-center  grey--text "
                          >Faça o cadastro e um consultor  <br> entrará em contato com você</h6>
                          <v-row align="center" justify="center">
                            <v-col cols="12" sm="8">
                             
                            <v-text-field
                              label="Email"
                              outlined
                              dense
                              color="blue"
                              autocomplete="false"
                             class="mt-16"
                            />
                            <v-text-field
                              label="Nome"
                              outlined
                              dense
                              color="blue"
                            autocomplete="false"
                             type="password"
                            
                            />
                            <v-text-field
                              label="Telefone"
                              outlined
                              dense
                              color="blue"
                            autocomplete="false"
                             type="password"
                            
                            />
                              <v-row>
                                <v-col cols="12" sm="7" md="12">
                                  <v-checkbox
                         
                          label="Lembrar"
                          class="mt-n1"
                          color="blue"
                        > </v-checkbox>
                                </v-col>
                                
                              </v-row>
                            <v-btn color="red" dark block tile>Enviar</v-btn>
                       
                           <h5
                            class="text-center  grey--text mt-4 mb-3"
                          >Ou cadastre-se com</h5>
                           <div class="d-flex  justify-space-between align-center mx-10 mb-16">
                            
                          <v-btn flat  outlined color="white">
                            <v-icon color="blue">mdi-google</v-icon>
                          </v-btn>
                          <v-col cols="auto">
                            <v-btn flat  outlined color="white">
                            <v-icon color="blue">mdi-facebook</v-icon>
                          </v-btn>
      </v-col>
      <v-btn flat  outlined color="white">
                            <v-icon color="blue">mdi-linkedin</v-icon>
                          </v-btn>
                           </div>
                            </v-col>
                          </v-row>  
                        </v-card-text>
                      </v-col>
                      <v-col cols="12" md="6" class="bg-blue rounded-bl-xl" >
                      <div style="  text-align: center; padding: 180px 0;">
                        <v-card-text class="white--text" >
                          <h2 class="text-center display-2">Quer ser um fornecedor parceiro?</h2>
                          <h6
                            class="text-center"
                          >Preencha o cadastro e faça parte<br> do nosso ecossistema</h6>
                        </v-card-text>
                        <div class="text-center">
                          <v-btn color="red" tile flat outlined dark @click="step++">Fornecedor</v-btn>
                        </div>
                        </div>
                      </v-col>
                    </v-row>
                  </v-window-item>
                  <v-window-item :value="2">
                    <v-row >
                      <v-col cols="12" md="6" class="bg-blue rounded-be-xl" >
                   
                       <div style="  text-align: center; padding: 180px 0;">
                        <v-card-text class="white--text" >
                          <div class="text-center text-h5 font-weight-bold">Quero receber um orçamento</div>
                          <h6
                            class="text-center"
                          >Preencha os campos abaixo e um especialista<br> entrará em contato com você</h6>
                        </v-card-text>
                        <div class="text-center">
                          <v-btn flat color="red" tile outlined dark @click="step--">receber orçamento</v-btn>
                        </div>
                        </div>
               
                      </v-col>
  
                      <v-col cols="12" md="6">
                        <v-card-text class="mt-12">
                          <div
                            class="text-center text-h5 font-weight-bold"
                          >Seja um fornecedor parceiro</div>
                          <h5
                            class="text-center  black--text "
                          >Preencha os campos abaixo e seja um <br>
                          fornecedor parceiro da Arkos</h5>
                          <v-row align="center" justify="center">
                       
                            <v-col cols="12" sm="8">
                             <v-row>
                             <v-col cols="12" sm="6">
                              <v-text-field
                              label="Nome"
                              outlined
                              dense
                              color="blue"
                              autocomplete="false"
                             class="mt-4"
                            />
                             </v-col>
                             <v-col cols="12" sm="6">
                              <v-text-field
                              label="Sobrenome"
                              outlined
                              dense
                              color="blue"
                              autocomplete="false"
                             class="mt-4"
                            />
                             </v-col>
                             </v-row>
                            <v-text-field
                              label="Email"
                              outlined
                              dense
                              color="blue"
                              autocomplete="false"
                            />
                            <v-text-field
                              label="Telefone"
                              outlined
                              dense
                              color="blue"
                            autocomplete="false"
                             type="password"
                            
                            />
                              <v-row>
                                <v-col cols="12" sm="7">
                                  <v-checkbox
                         
                          label="Lembrar-me"
                          class="mt-n1"
                          color="blue"
                        > </v-checkbox>
                                </v-col>
                                <v-col cols="12" sm="5">
                                  <span class="caption blue--text ml-">Terms &Conditions</span>
                                </v-col>
                              </v-row>
                            <v-btn color="red" dark block tile>cadastrar</v-btn>
                       
                           <h5
                            class="text-center  grey--text mt-4 mb-3"
                          >Or Sign up using</h5>
                           <div class="d-flex  justify-space-between align-center mx-10 mb-11">
                            <v-btn flat  outlined color="white">
                            <v-icon color="blue">mdi-google</v-icon>
                          </v-btn>
                          <v-col cols="auto">
                            <v-btn flat  outlined color="white">
                            <v-icon color="blue">mdi-facebook</v-icon>
                          </v-btn>
      </v-col>
      <v-btn flat  outlined color="white">
                            <v-icon color="blue">mdi-linkedin</v-icon>
                          </v-btn>
                           </div>
                            </v-col>
                          </v-row>  
                        </v-card-text>
                      </v-col>
                    </v-row>
                  </v-window-item>
                </v-window>
              </v-card>
            </v-col>
        </v-row>
    </v-container>
  </template>
  
  <script>
    
  
    export default {
     data: () => ({
      step: 1
    }),
    props: {
      source: String
    } 
  
      
    }
  </script>
  <style scoped>
  .v-application .rounded-bl-xl {
      border-bottom-left-radius: 300px !important;
  }
  .v-application .rounded-br-xl {
      border-bottom-right-radius: 300px !important;
  }
  </style>