<template>
  <v-navigation-drawer color="#0f0f0f" :border="0">
    <v-list :nav="true">
      <v-list-item title="Home" prepend-icon="mdi-home" to="/"/>
      <v-list-item title="Shorts" prepend-icon="mdi-video" to="/shorts" />
      <v-list-item title="Subcriptions" prepend-icon="mdi-youtube-subscription" to="/subcriptions" />
      <v-divider />
    </v-list>
  </v-navigation-drawer>
  <v-main>
    <router-view />
  </v-main>
</template>

<script lang="ts" setup>
  //
</script>
