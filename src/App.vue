<template>
	<div id="app">
		<div class="header">
			<h1>Lorem ipsum dolor sit amet consectetur.</h1>
		</div>
		<div class="nav-bar">
			<div class="nav-btn">
				<button v-for="(item, i) in items" :key="i" type="button"><router-link :to="item.to">{{ item.title }}</router-link></button>
			</div>
		</div>
		<div class="content">
			<router-view></router-view>
		</div>
		<div class="footer"><div><p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Adipisci, cupiditate?</p></div></div>
	</div>
</template>

<script>
export default {
	data: () => {
		return {
			items: [
				{ title: 'HOME', to: '/' },
				{ title: 'ABOUT', to: '/about' },
				{ title: 'BLOG', to: '/blog' },
				{ title: 'PRODUCTS', to: '/product' },
				{ title: 'CONTACT US', to: '/contact us' },
			],
		}
	},
}
</script>

<style scoped>
	* {
		font-family: sans-serif;
	}
	h1, h2, h3, h6 {
		font-size: 3ch;
		font-weight: bold;
	}
	p {
		font-size: 2ch;
	}
	.header {
		display: flex;
		justify-content: center;
		flex-direction: column;
		text-align: center;
		background-color: black;
		color: white;
		width: 100%;
		height: 7em;
	}
	.nav-bar {
		height: auto;
		max-width: 60em;
		margin: auto;
	}
	.nav-btn {
		display: flex;
		flex-wrap: wrap;
	}
	.nav-btn > * {
		font-size: 2ch;
		padding: .5rem 1.75rem;
		flex: 0 1 10em;
	}
	.content {
		min-height: 60em;
		height: auto;
		max-width: 60em;
		margin: auto;
	}
	.footer {
		bottom: 0;
		background-color: black;
		color: white;
		width: 100%;
		height: 8em;
		padding: 10px;
		text-align: center;
	}
</style>
