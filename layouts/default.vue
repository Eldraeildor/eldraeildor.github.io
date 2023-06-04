<template>
	<v-app dark>
		<v-navigation-drawer
			:mini-variant="miniVariant"
			permanent
			clipped
			fixed
			app
		>
			<v-list nav>
				<v-list-item
					v-for="(item, i) in items"
					color="purple lighten-2"
					:key="i"
					:to="item.to"
					router
					dense
					:disabled="item.dis"
				>
					<v-list-item-action>
						<v-icon>{{ item.icon }}</v-icon>
					</v-list-item-action>
					<v-list-item-content>
						<v-list-item-title>{{ item.title }}</v-list-item-title>
						<v-list-item-subtitle>{{ item.subtitle }}</v-list-item-subtitle>
					</v-list-item-content>
				</v-list-item>
			</v-list>
		</v-navigation-drawer>
		<v-app-bar
			outlined
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
			<v-avatar :size="40" style="margin-right: 10px;">
				<img src="~/assets/img/avatar.png" style="margin: 0 10px;"/>
			</v-avatar>
			<v-toolbar-title>{{ title }}</v-toolbar-title>
		</v-app-bar>
		<v-main style="background-image: url(/pattern.webp); background-repeat: repeat;">
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
					subtitle: '༼ つ ◕_◕ ༽つ',
					to: '/',
					dis: false
				},
				{
					icon: 'mdi-file-document-multiple',
					title: 'Guides',
					subtitle: '(╯‵□′)╯︵┻━┻',
					to: '/guides',
					dis: false
				},
				{
					icon: 'mdi-virtual-reality',
					title: 'VRChat Projects',
					subtitle: '=￣ω￣=',
					to: '/vrchat',
					dis: false
				},
				{
					icon: 'mdi-blender-software',
					title: '3D Models',
					subtitle: '(ヘ･_･)ヘ┳━┳',
					to: '/models'
				},
				{
					icon: 'mdi-headphones',
					title: 'Music recommendations',
					subtitle: '┌( ಠ_ಠ)┘ ㄟ(≧◇≦)ㄏ',
					to: '/music'
				},
			],
			miniVariant: false,
			title: 'Ellena\'s stash of stuff'
		}
	}
}
</script>
