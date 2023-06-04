<template>
	<v-row justify="center" align="center">
		<v-col cols="12" sm="12">
			<v-card outlined>
				<v-card-title class="headline">
					Music recommendations
				</v-card-title>
				<v-divider></v-divider>
				<v-card-text>
					<p>This section of the site will host links to some of the music i listen to, i don't make music myself maybe you'll find something that suits your taste ?</p>
				</v-card-text>
			</v-card>
		</v-col>
		<v-col cols="12" sm="12">
			<v-card outlined>
				<v-card-text>
					<code style="color: red;">Section has not been implemented yet, nothing to see here</code>
				</v-card-text>
			</v-card>
		</v-col>
	</v-row>
</template>
	
<script>
	export default {
		name: 'ModelsIndexPage',
		head: {
			title: 'Guides'
		},
		data: () => ({
      items: [
        {
          header: 'Categories'
        },
        {
          title: 'Food & Drinks',
          value: 'food'
        },
				{
          title: 'Furniture',
					value: 'furniture'
        },
				{
          title: 'Lights and Lamps',
					value: 'lighting'
        },
			],
      value: ['food', 'furniture', 'lighting'],
    }),
	}
</script>
	