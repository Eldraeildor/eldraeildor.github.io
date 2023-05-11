<template>
	<v-app dark>
		<v-navigation-drawer
			:mini-variant="miniVariant"
			permanent
			clipped
			fixed
			app
		>
			<v-list>
				<v-list-item
					v-for="(item, i) in items"
					:key="i"
					:to="item.to"
					router
					exact
					:disabled="item.dis"
				>
					<v-list-item-action>
						<v-icon>{{ item.icon }}</v-icon>
					</v-list-item-action>
					<v-list-item-content>
						<v-list-item-title>{{ item.title }}</v-list-item-title>
					</v-list-item-content>
				</v-list-item>
			</v-list>
		</v-navigation-drawer>
		<v-app-bar
			clipped-left
			fixed
			app
		>
			<v-btn
				icon
				@click.stop="miniVariant = !miniVariant"
			>
				<v-icon>mdi-{{ `chevron-${miniVariant ? 'right' : 'left'}` }}</v-icon>
			</v-btn>
			<img width="40px" height="40px" src="~/assets/img/avatar.png" style="margin: 0 10px;"/>
			<v-toolbar-title>{{ title }}</v-toolbar-title>
		</v-app-bar>
		<v-main>
			<v-container>
				<Nuxt />
			</v-container>
		</v-main>
		<v-footer
			:absolute="!fixed"
			app
		>
			<span>&copy; {{ new Date().getFullYear() }}</span>
		</v-footer>
	</v-app>
</template>

<script>
export default {
	name: 'DefaultLayout',
	data () {
		return {
			fixed: false,
			items: [
				{
					icon: 'mdi-home-variant',
					title: 'Homepage',
					to: '/',
				},
				{
					icon: 'mdi-virtual-reality',
					title: 'VRChat stuff (WIP)',
					to: '/vrchat',
					dis: true
				},
				{
					icon: 'mdi-file-document-multiple',
					title: 'Tutorials (WIP)',
					to: '/tutorials',
					dis: true
				}
			],
			miniVariant: false,
			title: 'Ellena\'s stash of stuff'
		}
	}
}
</script>
