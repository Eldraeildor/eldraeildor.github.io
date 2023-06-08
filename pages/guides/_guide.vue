<template>
	<v-row justify="center">
		
		<v-col cols="12" sm="12" md="9">
			<title-card :title="guide.title" :subtitle="guide.description"></title-card>
			<v-card outlined class="mb-3">
				<v-card-title>Table of contents</v-card-title>
				<v-divider></v-divider>
				<ul class="my-2">
					<li
						v-for="anchor of guide.toc"
						:key="anchor.id"
						:class="{ 'ml-0': anchor.depth === 2, 'ml-4': anchor.depth === 3 }"
					>
						<NuxtLink :to="`#${anchor.id}`">{{ anchor.text }}</NuxtLink>
					</li>
				</ul>
			</v-card>
			<v-card outlined>
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