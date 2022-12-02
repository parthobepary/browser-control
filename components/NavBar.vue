<template>
	<div>
		<ul>
			<li><nuxt-link to="/">Home</nuxt-link></li>
			<li><nuxt-link to="/forms">From</nuxt-link></li>
			<li><nuxt-link to="/rastictedroute">Rasticted</nuxt-link></li>
		</ul>
	</div>
</template>
<script>
export default {
	name: "NavBar",

}
</script>
<style lang="scss" scoped>
ul {
	display: flex;
	margin: 20px 0px;

	li {
		list-style: none;

		a {
			text-decoration: none;
			margin: 10px;
			color: black;
			font-weight: 700;
		}
	}
}
</style>