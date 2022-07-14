


<template>
<div>
  <v-navigation-drawer v-model="drawer" app>
    <v-list-item>
      <v-avatar size="40" color="indigo">
        <v-icon dark> mdi-account-circle </v-icon>
      </v-avatar>
      <v-list-item-content>
        <v-list-item-title class="text-h6"> Pessoa </v-list-item-title>
      </v-list-item-content>
    </v-list-item>

    <v-divider></v-divider>

    <v-list dense nav>
                    <v-list-item v-for="(item, index) in items" :key="index" :to="item.route">
                        <v-list-item-icon>
                            <v-icon v-text="item.icon"></v-icon>
                        </v-list-item-icon>
                        <v-list-item-content>
                            <v-list-item-title v-text="item.title"></v-list-item-title>
                        </v-list-item-content>
                    </v-list-item>
    </v-list>
  </v-navigation-drawer>



   <v-app-bar app>
      <v-app-bar-nav-icon @click="drawer = !drawer"></v-app-bar-nav-icon>
      <v-toolbar-title>
        <etomada-logo></etomada-logo>
      </v-toolbar-title>
      <tce-logo></tce-logo>
    </v-app-bar>
  </div>
</template>


<script>
import etomadalogo from "@/components/EtomadaLogo.vue";
import TceLogo from "@/components/TceLogo.vue";
export default {
    data(){
        return{
            drawer: false,
            group: null,
            items: [
                {icon: 'mdi-view-dashboard', title: 'Inicio', route: 'Inicio'},
                {icon: 'mdi-account-search', title: 'List Employee', route: '/'},
                {icon: 'mdi-account-edit', title: 'Employee Registration', route: '/register-new-employee'}
            ]
        }
    },
    watch: {
        group(){
            this.drawer = false
        }
    },

      components: { "etomada-logo": etomadalogo, TceLogo },
}

</script>