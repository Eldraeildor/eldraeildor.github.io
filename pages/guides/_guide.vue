<template>
	<v-row justify="center">
		<v-col cols="12" sm="12">
			<v-card outlined>
        <v-card-title>{{ guide.title }}</v-card-title>
        <v-card-subtitle class="overline">{{ guide.description }}</v-card-subtitle>
        <v-divider></v-divider>
				<v-card-text>
					<nuxt-content :document="guide" />
				</v-card-text>
			</v-card>
		</v-col>
	</v-row>
</template>
	
<script>

	export default {
		name: 'TutorialsIndexPage',
		head: {
			title: 'Guides'
		},
		data: () => ({

    }),

		async asyncData({ $content, params }) {
      const guide = await $content('guides/'+ params.guide).fetch()
      return { guide }
    }
	}
</script>
	