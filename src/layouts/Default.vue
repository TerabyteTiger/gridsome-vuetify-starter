<template>
  <div>
    <div>
      <v-app-bar>
        <v-btn icon :to="$url('/')" title="Home">
          <v-icon>mdi-home</v-icon>
        </v-btn>
        <v-toolbar-title>{{ $static.metadata.siteName }}</v-toolbar-title>
        <v-spacer />

        <v-btn :to="$url('/')">
          Home
        </v-btn>
        <v-btn :to="$url('/about')">
          About
        </v-btn>
      </v-app-bar>
    </div>
    <v-container>
      <v-card>
        <slot />
      </v-card>
    </v-container>
  </div>
</template>

<static-query>
  query {
    metadata {
      siteName
    }
  }
</static-query>
