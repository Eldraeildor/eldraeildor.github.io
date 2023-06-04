<template>
	<v-row justify="center" align="center">
		<v-col cols="12" sm="12">
			<v-card outlined>
				<v-card-title class="headline">
					3D Models
				</v-card-title>
				<v-divider></v-divider>
				<v-card-text>
					<p>This section of the site will host both the paid and free 3D models, click on the cards below to check the free ones out or learn where you can get the paid ones !</p>
					<p>Use the dropdown below to filter 3D models :</p>
					<v-select outlined hide-details
            v-model="value"
            :items="items"
            clearable
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
	