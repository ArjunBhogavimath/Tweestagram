<template>
  <q-layout view="hHh lpR fFf">

    <q-header elevated class="bg-grey-10 text-white">
      <q-toolbar>
        <q-btn dense flat round icon="fab fa-quinscape" @click="toggleLeftDrawer" />

        <q-toolbar-title class="text-weight-bold">
          Tweestagram
        </q-toolbar-title>

       <!-- <q-btn dense flat round icon="menu" @click="toggleRightDrawer" /> -->
      </q-toolbar>
    </q-header>

    <q-drawer show-if-above v-model="leftDrawerOpen" side="left" bordered>
     <!-- <q-icon name="fab fa-quinscape" />-->
      <q-list bordered>
      <q-item to ="/" clickable v-ripple exact>
        <q-item-section avatar>
          <q-icon color="primary" name="fas fa-house-user" />
        </q-item-section>

        <q-item-section >Home</q-item-section>
      </q-item>

     
      <q-item to ="" clickable v-ripple exact>
        <q-item-section avatar>
          <q-icon color="primary" name="fas fa-users" />
          
          
        </q-item-section>

        <q-item-section>Users</q-item-section>
      </q-item>
       <q-item to="/about" clickable v-ripple exact>
        <q-item-section avatar>
          <q-icon color="primary" name="fas fa-info-circle" />
          
        </q-item-section>

        <q-item-section>About</q-item-section>
      </q-item>

      </q-list>
      
    </q-drawer>

    <q-drawer show-if-above v-model="rightDrawerOpen" side="right" bordered>
       <q-input placeholder="Search" class="q-ma-md" outlined rounded dense>
        <template v-slot:prepend>
          <q-icon name="search" />
          
        </template>
      </q-input>
      <q-list separator padding>
      <q-item class="q-pa-md" >
        <q-item-section>
          <q-item-label overline class="text-grey">Trending</q-item-label>
          <q-item-label class="text-weight-bold">#Bitcoin</q-item-label>
          <q-item-label caption>After China ban on bitcoin, the bitcoin is slowly loosing its value</q-item-label>
        </q-item-section>

        <q-item-section side top>
          <q-item-label caption>5 min ago</q-item-label>
        </q-item-section>
      </q-item>

      <q-item class="q-pa-md">
        <q-item-section>
          <q-item-label overline class="text-grey">Trending</q-item-label>
          <q-item-label class="text-weight-bold">#Bitcoin</q-item-label>
          <q-item-label caption>After China ban on bitcoin, the bitcoin is slowly loosing its value</q-item-label>
        </q-item-section>

        <q-item-section side top>
          <q-item-label caption>5 min ago</q-item-label>
        </q-item-section>
      </q-item>

      <q-item class="q-pa-md">
        <q-item-section>
          <q-item-label overline class="text-grey">Trending</q-item-label>
          <q-item-label class="text-weight-bold">#Bitcoin</q-item-label>
          <q-item-label caption>After China ban on bitcoin, the bitcoin is slowly loosing its value</q-item-label>
        </q-item-section>

        <q-item-section side top>
          <q-item-label caption>5 min ago</q-item-label>
        </q-item-section>
      </q-item>
      </q-list>
    </q-drawer>

    <q-page-container>
      <router-view />
    </q-page-container>

  </q-layout>
</template>

<script>
import { ref } from 'vue'

export default {
  setup () {
    const leftDrawerOpen = ref(false)
    const rightDrawerOpen = ref(false)

    return {
      leftDrawerOpen,
      toggleLeftDrawer () {
        leftDrawerOpen.value = !leftDrawerOpen.value
      },

      rightDrawerOpen,
      toggleRightDrawer () {
        rightDrawerOpen.value = !rightDrawerOpen.value
      }
    }
  }
}
</script>