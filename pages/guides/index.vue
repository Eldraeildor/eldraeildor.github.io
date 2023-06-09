<template>
	<v-row justify="center">
			<!-- <v-img max-height="200" src="/patterns/pattern.webp">

			</v-img> -->
		<v-col cols="12" sm="12">
			<title-card
				title="Guides and tutorials"
				subtitle="This section of the site will host all of the guides and tutorials, click on the cards below to access them !"
				src="/patterns/header.png"
			>
			</title-card>
			<v-card outlined>
				<v-divider></v-divider>
				<v-card-text>
					<p>Use the dropdown below to filter the guides :</p>
					<code style="color: red;">not implemented yet é_è</code>
					<v-select outlined hide-details
            v-model="value"
            :items="items"
						item-text="title"
						item-value="value"
            chips
            label="Categories"
            multiple
          ></v-select>
				</v-card-text>
			</v-card>
		</v-col>
		<v-col cols="12" sm="12">
			<v-card outlined>
				<v-card-text>
					<v-card v-for="guide in guides" :key="guide.path">
						<v-card-title>{{ guide.title }}</v-card-title>
						<v-card-subtitle>{{ guide.description }}</v-card-subtitle>
						<v-btn :to="guide.path">{{ guide.path }}</v-btn>
					</v-card>
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
      items: [
				{
					title: 'VRChat World Building',
					value: 'vrc-worlds'
				},
				{
					title: 'VRChat Avatar Setup',
					value: 'vrc-avatars'
				},
				{
					title: '3D Modeling',
					value: '3d'
				},
				{
					title: 'Shaders',
					value: 'shaders'
				},
				{
					title: 'SteamVR Addons',
					value: 'steamvr'
				}
			],
      value: ['vrc-worlds', 'vrc-avatars', '3d', 'shaders', 'steamvr'],
    }),

		async asyncData({ $content }) {
      const guides = await $content('guides').fetch()
      return { guides }
    }
	}
</script>
