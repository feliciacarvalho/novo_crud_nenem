<template>

      <v-container>

        <v-card class="ma-10 pa-10">
          <v-card-text>
            <h2 class="mb-3">Olá</h2>
            <h1>Bem vindo </h1>
            <hr class="my-4 mb-10">
            <p :key="item.text" v-for="item in welcome"> {{ item.text }} </p>
            
          </v-card-text>
        </v-card>

        <v-card class="ma-10 pa-10">
            <v-card-text>
          <h1 class="mb-3">  Passo a Passo</h1>

                             
                   
          <v-img             class="ml-auto"
          src="https://picsum.photos/510/300?random"
  

              max-height="300"
    max-width="300"
        ></v-img>
       

                          
        <h2 class="mb-6"  > Para buscar o funcionãrio acesse: </h2>  
        <v-btn class="mb-3"
          color="#1d495f"
          dark
          v-on="on"
          to="/tarefa"
        >
        Buscar funcionário 
         </v-btn>

 

         <h2 class="mb-6" > Para cadastrar funcionário acesse </h2>
        <v-btn
        class="mb-3"
          color="#1d495f"
          dark
          v-on="on"
          to="/registrar"
        >
         Cadastrar Funcionário
          
        </v-btn>








        <h2 class="mb-6"  > Para gerenciar cadastro e permissões de acesso, acesse:</h2>
        <v-btn
        class="mb-3"
          color="#1d495f"
          dark
          v-on="on"
          to="/registrar"
        >
        Gerenciar cadastro e permissões
          
        </v-btn>
          </v-card-text>



          


        </v-card>
      

      </v-container>

</template>




<script>

export default {


  data: () => ({
    headers: [
      { text: 'Período', value: 'periodoNome' },
      { text: 'Prazo de Envio', value: 'prazoEnvio' },
    ],
    welcome:[
      { text: ' Tribunal de Contas do Estado do Maranhão (TCE/MA).'},
      
    ],
  }),

  watch: {

  },

  methods: {
    firstWord(str) {
      return str.split(' ')[0];
    },

    capitalize(str) {
      return str.toLowerCase().replace(/\b\w/g, l => l.toUpperCase());
    },

  },
}
</script>


<style lang="sass" scoped>

  .bar-title
    background: #442ba1
    border-radius: 20px
    position: relative


    height: 39.5px
    padding: 5px 15px 5px 40px
    z-index: 10
    color: #fff

  .title
    font-family: 'Asap Condensed', sans-serif !important
    font-size: 24px



</style>
