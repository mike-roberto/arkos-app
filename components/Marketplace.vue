<template>
 
    <div class="bg-white mt-15">
      <v-container fluid class="mt-15">
      <v-row>
        <v-col cols="12">
          <v-row>
            <v-col cols="12" sm="12" md="6">
              <v-card-text>
                <div class="text-black"></div>
                </v-card-text>
              <h1 class="title1 mt-15 mx-15 text-h3 font-weight-black">
                Construa soluções<br />
                com a ajuda de <br /> nossos especialistas
              </h1>
              <p class="par1 ms-15">
                Tenha acesso a serviços personalizados, realizados<br> por profissionais experientes e habilitados, de forma ágil,<br> fácil e segura. Conte com a nossa tecnologia para facilitar<br> seus projetos através de um ambiente digital e padronizado.
              </p>
              <v-btn class="text-noe mt-8 bt1 mx-15" color="#E61428" size="x-large" variant="flat" rounded="0">
              Conect-se
              </v-btn>
             
            </v-col>
            <v-col cols="12" sm="12" md="6">
              <v-img src="https://ieor.columbia.edu/sites/default/files/styles/cu_crop/public/content/images/masters-msie-01.jpg?itok=QfzYUy2h" class="img1"></v-img>
            </v-col>
          </v-row>
        </v-col>
        </v-row>
        </v-container>
        <v-container fluid class="">
      <v-row>
        <v-col cols="12" md="12" sm="12">
          <v-row>
           
            <v-col cols="12" sm="12" md="12">
              <v-sheet
      class="mx-auto"
      flat
      id="partners"
    >
      <v-slide-group
        v-model="model"
        class="pa-4"
        prev-icon="mdi-minus"
        next-icon="mdi-plus"
      
        show-arrows
      
      
      >
      
        <v-slide-group-item
          
          v-slot="{ isSelected, toggle, selectedClass }"
        >
          <v-card
            color=""
            :class="['ma-4', selectedClass]"
            height="150"
            width="350"
          
            flat
            image="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRhqyGqtgcXmP8VBO8dXuJI_cczV0htSGhM7-TWWlvFExIJaGH8o_Y86bXAEsyzIyWmiqU&usqp=CAU"
          >
            <div class="d-flex fill-height align-center justify-center">
              <v-scale-transition>
              
              </v-scale-transition>
            </div>
          </v-card>
          <v-card
            color="grey-lighten-1"
            :class="['ma-4', selectedClass]"
            height="200"
            width="300"
            @click="toggle"
            flat
            image="https://logowik.com/content/uploads/images/316_siemens.jpg"
          >
            <div class="d-flex fill-height align-center justify-center">
              <v-scale-transition>
                <v-icon
                  v-if="isSelected"
                  color="white"
                  size="48"
                  icon="mdi-close-circle-outline"
                ></v-icon>
              </v-scale-transition>
            </div>
          </v-card>
          <v-card
           
            :class="['ma-4', selectedClass]"
            height="200"
            width="350"
            @click="toggle"
            flat
            image="https://findvectorlogo.com/wp-content/uploads/2022/04/archicad-vector-logo-2022.png"
          >
            <div class="d-flex fill-height align-center justify-center">
              <v-scale-transition>
                <v-icon
                  v-if="isSelected"
                  color="white"
                  size="48"
                  icon="mdi-close-circle-outline"
                ></v-icon>
              </v-scale-transition>
            </div>
          </v-card>
          <v-card
           
           :class="['ma-4', selectedClass]"
           height="150"
           width="300"
           @click="toggle"
           flat
           image="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAOEAAADhCAMAAAAJbSJIAAABDlBMVEX////aIRn/XwDYAAD/uQDXAAD0tq/bAADmcWz29fbYEADaHRT98O/cDADvlpTeAADwtbPeKSTlk5Hvubf55OX/VgDfLCHz09L/9/fdX1ncOC3oiofbFwziPDb/UwD/tQDywcD72tn/TAD30dD+/O/64eD2zs3+/Pb+5aLkSkX/vQD+7L/jZmPkWVXhIBbwrKrpfXrwp6XjU1D+3M3+gU3+yrL+0r/8tJ7/i1P+kWX+aCX/fj3wnp3+8c/86+TgsK7hvbv+3ob/xy3/bxz+yEn9lnD8q5H/0l3925/+8s38n3r+6a//dDH+dT//tpX+z0v+45f+wKP+xKf+2Gv98tz/mmPmgX/blZPq4uHYZ2RYiiufAAAMHklEQVR4nO2cC5ebNhbHjTUsHgQGYuzBtpiBODglNX7lsUnqzm6TtN2k6bTJdqe73/+L7BWSAD87OXFmlu795ZzkWMbi/pHuQwLSaCAIgiAIgiAIgiAIgiAIgiAIgiAIgiAIgiAIgiAIgiAIgiAIgiAIgiAIgiAIgjQaj588vGsTvixPu93Hd23DF+VZt9n9610b8SV52Gw2u893fGHFt27Ll+FFFyS+tDabk6G3vAtzjk9wv8nZdMS2YejzOzHo6Dw95wK7P6w1WiHRNLuWCh8+2GyRCr+ptgWhqWmavro9u47Ht482JV6KWdqsOuLfHBCoOX+/RcOOxncXrzaT++tc4FpGbPEh1Az3Ni07Fm9OtiR+391yxIzlY9i5VdOOw4NXFycXP663fdx2RKHQGN2qbcfht0cXJycX3621XeZj2Dw/LVqskHKFdnLb5h2Btyeci3+sNQpHvP+saJAKmX/b5h2Bt4+ExK+qje82HdH3uEIabtU5NeA38MNc4k+VxqdC4ZOiYZSHUpoGt2/g5/NGKDw5qUh8KB2xGLKRnU/SrJYKf1IKH70tG99vOOLYyBVO7sLAz+bhj4XE34pG6Yjv1Gc3V2jWsiyFjKgkXpT126YjrvJZag7vxsLP5sErJbEobi5f5tP0G/X5Oldot+/KxM8lz/pComr6OY80V+rjtShLozsx7xg8KCT+Iluu+DQ9Lw7IC29Sm1AabBv6rQw2Jxe/ioZnoPB+ubjIGDXJvC4CGx/eb+8Ufq0UvhGudwkCy5ImCA2vVaNdqA/3uy+2zP1KpYxvxecn96/KL625W6t67eq82W2+u9xo/Uq64tfi47sftn5XHz7w5R9o3BiWX3OJj76+G6OOykdZdTav1tv/efFnUfhY7jSBxo9rX3CJldIN/M+3LKuGa8LLZsH566fVb365uHilKrcgmnvMIIbhTNP2WW0SheBFt6Lx52eVb96o/Qz/2jNsmi/sNcp0e9Cu1VAW0zQvr7vPy/T44BcxSVc9ItQpqKHN65QwPpx3qxqbL4rUked7KzPW9eUaiVan3dLHT7prGrvVsOp7ZkVYVWN96jbg2ZPzisRmpYKxpkxpsonDGLMdNWVJvRb5z95X3bFZTNSlGkHdaXWSoBH40TA1uEjm1W2/9OnrUmOxYzEjck7q15U5aa1Sgxk1Kr4VH98Xc/VnsagIUjFH7XBzvOJlHe9aNB5evVQaRc4YO0JgVqfccBjr6nWu8Vw8fDEUe05/IoHA5TtIic3uv/IPSz5J6bRuIeWPuPy+2xVbh0HKE4NRy7vZh7l8fv8l/zfJb8EYf6o5qnj8nAfThBcxNd29vxnJlKf6uu5tRxViIMnx/WqxmfRgDEmdSuwqK8MumAp6017PC6/LtV9+s9cY36GVn4O8VV2uFRS6Vkri2cKJ7s7Iz6NDtlZ9UmqpaQ51t17XMWw0MnO3RI0yVVRHTo39ENa2O9buAubJFMhTvlPbu2iNxpnB9ki0VQ5c6Brr36mRn0ccOuZuyEwcEYSO4dS5prFm89Zu1E16Pxp36rQfgyAIgvy/YcXj+Ni52BJ7TsH4S+09+Wc3PTLoTEKb2GHrqKaMQ7GeX5JP3n2C2qGfTdp/8Oh3R5vdsL8k0838OV3zmK91zHU9r7JnBJYXn3bpZhoxGTMJyQ5oPM108peb9TdmsPAxSV44H1GiQ8XTeAtYObJPuivR0uEXpg0X3Tww+qdEu6HCZMo0SlquOzGgZ33xKbYcYkpJrjDoEXL9KT+EFQh1+sNhyq852bvaurnClKlbW8G1oenOsXxRKYSV7yeNoG9rLMxDCPee5d5C/cYKuZsMVBR1SeWOehBYN1kHBHueMygVrh/+R53OdK24yovB/ocYNhSe+vveLoYhtKPiUzGAvttKB164XKhTxK7baQQjt+NWBtmCo0I46l6lLRh1OvwJkmKWdoqfWJ05HD5Ih2pQE+iO/x11ymGem5SVJ6hYejbMlq1ZcX0qCq1oDsYO0rYy48ztdPjfLnSbGJq5Yxs60gyTb5Ux4kn5Q8OY+qltEMKKW+7JgMijWLH9Mg7hGDudQaQRCi1G5OaMlRomE4fL0XUdwkYTRnTCJupS9plmbBvUsOY24fE1jLYU+iEPvbxfc6aMJb1GyzYM1udzYtfmkAWpw4T+qMZskVbv2drAM/PHYIh6NyIIGTMYGAyhSp54Bh/4XiJxQ6XQK84wMRmxbX6EbOk4mjcQnRa3TVvmrg05KyO8XwiyxmJTYWMJkdfk/VL5qPE9m2YtnV/MLH8GeddcH5J5FMdualKzrxRqVKcehYBL1Nb8gkzcOO4sicbSvCFhVKM2CKZssK0wIpk7GkV9nj8CqRAuJfMo4fcVxUFtCAw0amwwMaBTz+OJTW4qVxTOdDDjrAMXgfaUsdQk2oBnv5TL3EEiHaMPJltKIVn5lr8yypeULJmRr21Nz5vmumaGnVPfHZgq0lcUBtLwFdH0M6mQ2sPEshaQ/YiwPOGq9X60FpBcXWO9jmXFc1BhbyoM5JjDcBG/YmzgL+KGt9MNK0pN6gXyR/JpAjibsVEuWSG1ffEvFYPJI5hSSLf8IKR6LBVK14ns4pULl09jRoysXYSfYABzQkgGt9JnUqGxkS2sARU+BcYW54TZ0TqokBYKqSfbvK08kPSEQn9K9UiejWyPYUFaKuzJscpYMZnGoc49EwJQJn0zMsqyCGLtco9C3ysU0uLld2+fQqtzb9h2/XhaKuwV9hWOGEQrOCpJBkLhCM6qvJruUJgfPouDJVMKKZUJocXKrdRgtrQNvodu2uKXQ7200gen58JPjVKhMCNOyjGkg/Jq7t6jnQ0MvtGppdq2wrBQ2AkJMU2dphALuTK41rbyn+l2pBmHhm5DgIbDDyoEk5PFhEcVGRwzVpkGcPrxusIo5WYQxs3YUjhnO9+LaxMKwYjYJjukEDyGmgb8YVJhx6Ca6mJbYWQwyFk2GFMq1HYr5MQtHnNz68DNy1XGhOm8v3KWLrgZBP6wXQoXcszXcYlmDuar9u/ZgO5XOIbf9lq/t3/vh1QodI3ioG2FMeibThbt1QQOv4FC8dJXPoigsCx6WiZZNCqxNCbU7IGx93i/2wpH+q6nI1JqtsSZ4wMKIYHLZ2O4i4tZSrW9s3RIaCicNKhEmkMKeRbK1SyZqij4h2KWCoVgRuoXZmwpbMCFTTc79h3NlieGC79XoaMReWV9GUthVPf7YcjUy003VujDoNxr8PhZRm/L0Bz+42KW2lQ9FLdb4ZCIyySvT25L4tBQGprsH0MLsrBVds0VxuD9as7b1FxTGAwYVVPtoEK/LLeheMyNg9mvqdYVEcYphaC4KEB2KoRONCKfm7MmJH+S1Xeo+tGC7FUYOMVd+ciW+VAr+oLMbK9l/CCkhvzujB3ww8RLC4kQD/Jxhz7U/30SQ/mU91sdQ2UG26WQXxPKhkkQ+DPPlLczPSryjzU3DsRSnqT5d9aQykgDiY6K+6FQ+BQK5SydE/HCdrAwD0SaJIR1grwSPhTlvfxS85nGVx9Bx6OauEFX+CGYscz7XbFdkYb3DUEZUlrqQSUhL8cKysvlajaHxcQBhaDCTNuz69BW2SIPzYPVeNa3+dnWFfLQG7Znw5Q/Mbs3H475KclyNo7HC1BDRBi0oAg0vawFKwEVGQuFPPDzfkPe706FQQu+gnHkSxMZsiw+mpBFKQkP5cMUSnhIb4yEPSpqmSA1wT5YQ5pZSjfrUriU4rvBgO7P+K5m5mWpzZ8d1tV7iWMGmZnxLUFd1tFlxl/Kfu1wpx/mQzblK1noNS0W36FBYMVltyNI+rkNbce05Zc9W24tWZnBawn7euSZMsLAajRfiw6sqSn8xZra0pKgJQ6f/Ps/plDoOrYK2n3HkaVkvCT8avPVnT4pqpERDBHffSv+L6JTyPGiX6uflzT2PA5NJ1c4dOyi8hBYs3maTtrVhWdnOBku/EYwGolqwh+PVFlxNhqr4jMatq4XSd6kbHGzQZgtgsZkkollw2g8VqFj1G5dr+LycGs8Vp3G43JrPALXggW4vYyqNi48xtikrG2yfqYMHg9FvyPZb1L2iyAIgiAIgiAIgiAIgiAIgiAIgiAIgiAIgiAIgiAIgiAIgiAIgiAIgiAIgiDI/x7/BfYFG6OKfo8GAAAAAElFTkSuQmCC"
         >
           <div class="d-flex fill-height align-center justify-center">
             <v-scale-transition>
               
            
             </v-scale-transition>
           </div>
         </v-card>
         <v-card
           
           :class="['ma-4', selectedClass]"
           height="200"
           width="200"
           @click="toggle"
           flat
           image="/hitachi.png"
         >
           <div class="d-flex fill-height align-center justify-center">
             <v-scale-transition>
               
            
             </v-scale-transition>
           </div>
         </v-card>
         <v-card
           
           :class="['ma-4', selectedClass]"
           height="210"
           width="200"
           @click="toggle"
           flat
           image="data:image/jpeg;base64,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"
         >
           <div class="d-flex fill-height align-center justify-center">
             <v-scale-transition>
               
            
             </v-scale-transition>
           </div>
         </v-card>
          <v-card
          
            :class="['ma-4', selectedClass]"
            height="200"
            width="240"
            @click="toggle"
            flat
            image="https://brand.autodesk.com/app/uploads/2021/04/primary-logo-1.svg"
          >
            <div class="d-flex fill-height align-center justify-center">
              <v-scale-transition>
                <v-icon
                  v-if="isSelected"
                  color="white"
                  size="48"
                  icon="mdi-close-circle-outline"
                ></v-icon>
              </v-scale-transition>
            </div>
          </v-card>
        </v-slide-group-item>
      </v-slide-group>
    </v-sheet>
            </v-col>
          </v-row>
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