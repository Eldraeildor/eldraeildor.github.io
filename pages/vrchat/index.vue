<template>
	<v-row justify="center" align="center">
		<v-col cols="12" sm="8" md="6">
			<v-card outlined>
				<v-card-title class="headline">
					VRChat projects
				</v-card-title>
				<v-card-text>
					<p>This section of the site will host all of my VRChat related projects, click the project cards below if you want to know more about how i did these !</p>
					<p>Also, when some of these projects are made public, they will most likely be avaiable either on GitHub or Gumroad, click the buttons below to check them out.</p>
				</v-card-text>
				<v-divider></v-divider>
				<v-card-actions>
					<v-spacer></v-spacer>
					<v-btn color="white" href="https://github.com/Eldraeildor/">
						<img src="~/assets/img/logo_github.png" height="30px"/>
					</v-btn>
					<v-btn color="orange" href="https://ellenaf.gumroad.com/">
						<img src="~/assets/img/logo_gumroad.png" height="30px"/>
					</v-btn>
				</v-card-actions>
			</v-card>
			</v-col>
			<v-col cols="12" sm="12">
				<v-card outlined>
					<v-card-title>
						Projects
					</v-card-title>
					<v-divider></v-divider>
					<v-card-text>
						// To be implemented
					</v-card-text>
				</v-card>
			</v-col>
		</v-row>
	</template>
	
	<script>
	export default {
		name: 'VRChatIndexPage',
		head: {
			title: 'VRChat related stuff'
		}
	}
	</script>
	