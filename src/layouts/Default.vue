<template>
  <v-app>
    <div>
      <v-app-bar>
        <v-btn
          icon
          router
          exact
          :to="$url('/')"
        >
          <v-icon>mdi-home</v-icon>
        </v-btn>
        <v-toolbar-title>
          {{ $static.metadata.siteName }}
        </v-toolbar-title>
        <v-spacer />

        <v-btn :to="$url('/')">
          Home
        </v-btn>
        <v-btn :to="$url('/about')">
          About
        </v-btn>
      </v-app-bar>
    </div>
    <v-content>
      <slot />
    </v-content>
  </v-app>
</template>

<static-query>
  query {
    metadata {
      siteName
    }
  }
</static-query>
