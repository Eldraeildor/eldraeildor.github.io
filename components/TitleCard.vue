<template>
  <v-card
    outlined
    class="mx-auto mb-3"
  >
    <v-img v-if="src"
      :src="src"
      class="white--text align-end"
      gradient="to bottom, rgba(0,0,0,.1), rgba(0,0,0,.5)"
      height="200px"
    >
      <v-card-title>{{ title }}</v-card-title>
      <v-card-subtitle>{{ subtitle }}</v-card-subtitle>
    </v-img>
    <v-card-title v-if="!src && title">{{ title }}</v-card-title>
    <v-card-subtitle v-if="!src && subtitle">{{ subtitle }}</v-card-subtitle>
  </v-card>
</template>

<script>

export default {
  props: ['title', 'subtitle', 'src']
}
</script>

<style lang="sass">

</style>