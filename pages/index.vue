<template>
	<v-row justify="center">
		<v-col cols="12" sm="12">
			<v-card outlined>
				<v-card-title class="headline">
					Welcome to Ellena's stash of stuff !
				</v-card-title>
				<v-card-text>
					<p>In this website you'll find some information about the projects i'm currently working on as well as ressources and tutorials, mostly about VRChat, Unity, or Blender.</p>
					<p>While there isn't a lot of content yet, I plan on updating this website and improving the navigation and contents of it.</p>
					<p>
						This website is made using the following technologies and frameworks :
						<ul>
							<li><a href="https://nuxtjs.org/">NuxtJS</a> and the <code>content</code> module as the framework</li>
							<li><a href="https://pages.github.com/">GitHub Pages</a> for hosting the static website (generated from the website's repository on GitHub)</li>
						</ul>
					</p>
					<p>
						Feel free to check out the contents of the website, i hope you'll find something of interest in here !
					</p>
					<v-btn to="guides" color="primary">Guides</v-btn>
					<v-btn to="vrchat" color="primary">Projects</v-btn>
					<v-btn to="models" color="primary">3D Assets</v-btn>
				</v-card-text>
			</v-card>
		</v-col>
	</v-row>
</template>

<script>
export default {
	name: 'IndexPage',
	head: {
		title: 'Homepage'
	}
}
</script>
