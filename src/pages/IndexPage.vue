<template>
  <q-page  class="row">
    <q-card class="col-xs-9">
      <q-toolbar>
        <q-input
        class="full-width"
        borderless
        dense
        placeholder="Search"

        :model-value="search">

        <template #append>
          <q-icon name="mdi-magnify" />


        </template>

        </q-input>
      </q-toolbar>

      <q-list bordered>
        <q-item>
          <q-item-section side>
            <q-checkbox :model-value="true" />
          </q-item-section>
          <q-item-section>
            Learn Go
          </q-item-section>
          <q-item-section side>
            <q-btn flat
            round
            size="sm"
            icon="mdi-delete" />


          </q-item-section>
        </q-item>
      </q-list>

    </q-card>

    <div class="col-xs-3">
      <q-toolbar
      class="bg-green">

        <q-btn
        fab
        style= "margin-bottom: -2.5rem;"
        class="q-ml-md"
        color="secondary"
        icon="mdi-plus"
        size="2rem"/>


      </q-toolbar>

    </div>






  </q-page>
</template>

<script>
import { defineComponent } from 'vue'

export default defineComponent({
  name: 'IndexPage',
  data(){
    return {
      search:''
    }
  }
})
</script>
