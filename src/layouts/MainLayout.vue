<template>
  <q-layout view="hHh Lpr lFf">
    <q-header >
      <q-toolbar>
        <q-btn
          flat
          dense
          round
          icon="mdi-menu"
          aria-label="Menu"
          @click="toggleLeftDrawer"
        />

        <q-toolbar-title>
          Quasar App
        </q-toolbar-title>

        <!-- <div>Quasar v{{ $q.version }}</div> -->
        <q-btn
        flat
        round
        icon="mdi-logout"  />

        <!-- </q-btn> -->
      </q-toolbar>
    </q-header>

    <q-drawer
      v-model="leftDrawerOpen"
      show-if-above
      bordered
    >
      <q-list>
        <q-toolbar class="col-sm-12 bg-green"
         />

        <q-item class="bg-grey-3">
          <q-item-section >
            list
          </q-item-section>
          <q-item-section side>
            <q-btn
            flat
            round
            size="sm"
            icon="mdi-plus"  />

          </q-item-section>
        </q-item>
        <q-item clickable>
          <q-item-section side>
            <q-icon name="mdi-shopping"/>



          </q-item-section>
          <q-item-section class="q-ml-md">
            Shopping list

          </q-item-section>
          <q-item-section side>
            7

          </q-item-section>
        </q-item>


        <!--  -->
      </q-list>
    </q-drawer>

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>
import { defineComponent, ref } from 'vue'



export default defineComponent({
  name: 'MainLayout',

  components: {

  },

  setup () {
    const leftDrawerOpen = ref(false)

    return {

      leftDrawerOpen,
      toggleLeftDrawer () {
        leftDrawerOpen.value = !leftDrawerOpen.value
      }
    }
  }
})
</script>
