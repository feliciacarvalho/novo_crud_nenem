<template>
  <v-list-item class="logo-sinc">
      <v-list-item-avatar>
      <v-img class="sinc-icon" src="@/assets/logo-etomada.png"></v-img>
      </v-list-item-avatar>

      <div class="bar-title">
          <span class="title">ETomada - </span>
          <span class="subtitle">Sistema de Tomada de Contas Especiais</span>
      </div>
  </v-list-item>
</template>

<style lang="sass" scoped>

  .bar-title
    background: #442ba1
    border-radius: 25px
    position: relative
    left: -50px
    height: 39.5px
    padding: 5px 15px 5px 40px
    z-index: 10
    color: #fff

  .title
    font-family: 'Asap Condensed', sans-serif !important
    font-size: 24px


  .subtitle
    font-family: 'Roboto', sans-serif !important
    font-size: 14px
    font-weight: normal
    position: relative
    bottom: 2px

  .v-list-item__avatar
    border: 2px solid #ffffff
    position: relative
    z-index: 11
</style>
