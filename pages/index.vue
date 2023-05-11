<template>
  <v-row justify="center" align="center">
    <v-col cols="12" sm="8" md="6">
      <v-card>
        <v-card-title class="headline">
          Hey, is this a work in progress website ?!
        </v-card-title>
        <v-card-text>
          <p>It sure is, i only just managed to setup Github pages to generate and deploy the application automatically, i think it should work now.</p>
          <p>Now i should be able to see changes when i push stuff on the repo, wish me luck !</p>
        </v-card-text>
        <v-card-actions>
          <v-spacer />
          <v-btn
            color="primary"
            nuxt
            to="/inspire"
          >
            Continue
          </v-btn>
        </v-card-actions>
      </v-card>
    </v-col>
  </v-row>
</template>

<script>
export default {
  name: 'IndexPage'
}
</script>
