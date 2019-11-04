<template>
  <div>
    <v-toolbar>
      <v-toolbar-title>
        <g-link to="/">
          {{ $static.metaData.siteName }}
        </g-link>
      </v-toolbar-title>
      <v-spacer />
      <nav class="nav">
        <g-link
          class="nav__link"
          to="/"
        >
          Home
        </g-link>
        <g-link
          class="nav__link"
          to="/about"
        >
          About
        </g-link>
      </nav>
    </v-toolbar>
    <slot />
  </div>
</template>

<static-query>
query {
  metaData {
    siteName
  }
}
</static-query>

<style>
body {
  font-family: -apple-system, system-ui, BlinkMacSystemFont, 'Segoe UI', Roboto,
    'Helvetica Neue', Arial, sans-serif;
  margin: 0;
  padding: 0;
  line-height: 1.5;
}

.layout {
  max-width: 760px;
  margin: 0 auto;
  padding-left: 20px;
  padding-right: 20px;
}

.header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 20px;
  height: 80px;
}

.nav__link {
  margin-left: 20px;
}
</style>
