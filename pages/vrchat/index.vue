<template>
	<v-row justify="center" align="center">
		<v-col cols="12" sm="12">
			<v-card outlined>
				<v-card-title class="headline">
					VRChat projects
				</v-card-title>
				<v-divider></v-divider>
				<v-card-text>
					<p>This section of the site will host all of my VRChat-related projects, click the project cards below if you want to know more about how i did these !</p>
					<p>Also, when some of these projects are made public, they will most likely be avaiable either on GitHub or Gumroad, click the buttons below to check them out.</p>
					<v-btn color="white" href="https://github.com/Eldraeildor/">
						<img src="~/assets/img/logo_github.png" height="30px"/>
					</v-btn>
					<v-btn color="orange" href="https://ellenaf.gumroad.com/">
						<img src="~/assets/img/logo_gumroad.png" height="30px"/>
					</v-btn>
				</v-card-text>
			</v-card>
		</v-col>
		<v-col cols="12" sm="12">
			<v-card outlined>
				<v-card-title>
					Projects
				</v-card-title>
				<v-divider></v-divider>
				<v-card-text>
					<code style="color: red;">Section has not been implemented yet, nothing to see here</code>
					<!-- <model-fbx
						:width="300"
						:height="300"
						:backgroundColor="'rgb(0, 0, 0)'"
						:src="'/3dmodels/Cubes.fbx'"
						:scale="{ x: .5, y: .5, z: .5 }"
						:controlsOptions="{
							autoRotate: true,
							autoRotateSpeed: 2.0,
							enabled: true,
							enablePan: false
						}"
						>
					</model-fbx> -->
				</v-card-text>
			</v-card>
		</v-col>
	</v-row>
</template>
	
<script>
	// import { ModelFbx } from 'vue-3d-model';
	export default {
		name: 'VRChatIndexPage',
		head: {
			title: 'VRChat related stuff'
		},
		components: {
			// ModelFbx
		}
	}
</script>
	