<template>
  <v-app>
    <v-navigation-drawer v-model="showMenu" location="left" permanent>
      <v-list nav>
        <v-list-item prepend-icon="mdi-menu" title="Menu" @click="toggleMenu"></v-list-item>
        <v-list-item prepend-icon="mdi-contacts" title="Contacts"></v-list-item>
        <v-list-item prepend-icon="mdi-cog" title="Settings"></v-list-item>
        <v-list-item prepend-icon="mdi-account-circle" title="Account"></v-list-item>
      </v-list>
    </v-navigation-drawer>
    <v-btn icon="mdi-menu" @click="toggleMenu" style="position: fixed; top: 10px; left: 10px;"></v-btn>
    <v-main>
      <v-container class="fill-height">
        <v-responsive class="d-flex fill-height">
          <Welcome />
        </v-responsive>
      </v-container>
    </v-main>
  </v-app>
</template>

<script setup lang="ts">
// Import components
import Welcome from '@/components/Welcome.vue'
</script>

<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
  async mounted() {
    // Component is mounted.
  },
  data: () => {
    // Data model.
    var data: {
      showMenu: boolean
    } = {
      showMenu: false,
    }
    return data
  },
  methods: {
    toggleMenu() {
      this.showMenu = !this.showMenu
    }
  }
})
</script>
