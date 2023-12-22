<template>
  <v-app-bar flat color="#0f0f0f">
    <template #prepend>
      <v-app-bar-nav-icon />
      <v-app-bar-title>
        <router-link to="/" class="text-decoration-none text-grey-lighten-4">
          <v-icon>
            mdi-youtube
          </v-icon>
          Youtube
        </router-link>
      </v-app-bar-title>
    </template>
    <template #default>
      <v-sheet class="d-flex justify-center align-center bg-transparent w-33">
        <v-text-field
          density="compact"
          placeholder="Search"
          variant="outlined"
          rounded
          hide-details
        />
        <v-btn variant="tonal" icon="mdi-magnify" class="ms-3" />
        <v-btn icon="mdi-microphone" class="ms-3" variant="tonal"/>
      </v-sheet>
    </template>
    <template #append>
      <v-sheet class="d-flex align-center w-100 bg-transparent pe-5">
        <v-btn icon="mdi-video-box" class="mx-1" />
        <v-menu
          :location="'bottom start'"
          :width="'300'"
          :max-width="'300'"
          :content-class="'rounded-xl'"
        >
          <template #activator="{ props }">
            <v-btn icon="mdi-bell" class="mx-1" v-bind="props" />
          </template>
          <v-sheet>
            <v-sheet class="d-flex justify-space-between align-center px-3 py-1">
              <span>Notifications</span>
              <v-btn icon="mdi-cog" variant="plain"/>
            </v-sheet>
            <v-divider />
            <v-sheet class="overflow-y-auto" style="max-height: 300px; height: 300px;">

            </v-sheet>
          </v-sheet>
        </v-menu>
        <v-menu
          :location="'bottom start'"
          :width="'300'"
          :max-width="'300'"
          :content-class="'rounded-xl'"
        >
          <template #activator="{ props }">
            <v-avatar class="ms-1" :color="'primary'" :image="'https://cdn.vuetifyjs.com/images/lists/1.jpg'" v-bind="props" />
          </template>
          <v-list lines="one">
            <v-list-item
              prepend-avatar="https://cdn.vuetifyjs.com/images/lists/1.jpg"
              title="Rolando Guerra"
              subtitle="rolandoguerra1991"
            >
              <template #default>
                <router-link to="/" class="text-decoration-none">
                  View your channel
                </router-link>
              </template>
            </v-list-item>
            <v-divider />
            <v-list-item
              prepend-icon="mdi-google"
              title="Google Account"
            />
            <v-list-item
              prepend-icon="mdi-swap-horizontal"
              append-icon="mdi-chevron-right"
              title="Switch Account"
            />
            <v-list-item
              prepend-icon="mdi-logout-variant"
              title="Sign out"
            />
            <v-divider />
            <v-list-item
              prepend-icon="mdi-youtube-studio"
              title="Youtube studio"
            />
            <v-list-item
              prepend-icon="mdi-cash-multiple"
              title="Purchases and memberships"
            />
            <v-divider />
            <v-list-item
              prepend-icon="mdi-shield-account"
              title="Your data in youtube"
            />
            <v-list-item
              prepend-icon="mdi-moon-waning-crescent"
              title="Aparence: device theme"
            />
            <v-list-item
              prepend-icon="mdi-translate"
              title="Language: english"
            />
            <v-list-item
              prepend-icon="mdi-security"
              title="Restricted Mode: off"
            />
            <v-list-item
              prepend-icon="mdi-earth"
              title="Location"
            />
            <v-list-item
              prepend-icon="mdi-keyboard"
              title="Keyboard Shortcuts"
            />
            <v-divider />
            <v-list-item
              prepend-icon="mdi-cog"
              title="Settings"
            />
            <v-divider />
            <v-list-item
              prepend-icon="mdi-help-circle-outline"
              title="Help"
            />
            <v-list-item
              prepend-icon="mdi-message-alert"
              title="Send Feedback"
            />
          </v-list>
        </v-menu>
      </v-sheet>
    </template>
  </v-app-bar>
</template>

<script lang="ts" setup>
  //
</script>
