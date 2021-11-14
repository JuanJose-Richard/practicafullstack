<template>
  <q-layout view="lHh Lpr lFf">
    <q-header elevated>
      <q-toolbar>
        <q-btn
          flat
          dense
          round
          icon="menu"
          aria-label="Menu"
          @click="toggleLeftDrawer"
        />

        <q-toolbar-title>
          Quasar App
        </q-toolbar-title>

        <div>Quasar v{{ $q.version }}</div>
      </q-toolbar>
    </q-header>

    <q-drawer
      v-model="leftDrawerOpen"
      show-if-above
      bordered
    >
      <q-list>
        <q-item-label
          header
        >
          Essential Links
        </q-item-label>
        <q-list bordered separator>
      <q-item clickable v-ripple to="/" exact >
        <q-item-section>Principal</q-item-section>
      </q-item>
      <q-item clickable v-ripple to="materia" exact>
        <q-item-section>Materias</q-item-section>
      </q-item>
      <q-item clickable v-ripple to="estudiante" exact>
        <q-item-section>Estudiantes</q-item-section>
      </q-item>



    </q-list>

      </q-list>
    </q-drawer>

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>



export default {
  data(){
    return{
      leftDrawerOpen:false,
    }
  },
  methods:{
    toggleLeftDrawer () {
         this.leftDrawerOpen = !this.leftDrawerOpen
      }
  }
  // name: 'MainLayout',

  // components: {
  //   EssentialLink
  // },

  // setup () {
  //   const leftDrawerOpen = ref(false)

  //   return {
  //     essentialLinks: linksList,
  //     leftDrawerOpen,
  //     toggleLeftDrawer () {
  //       leftDrawerOpen.value = !leftDrawerOpen.value
  //     }
  //   }
  // }
}
</script>
