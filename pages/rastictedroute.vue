<template>
	<div>
		<h1>hello i am rasticted</h1>
		<button @click="setPermisin">permisin</button>
	</div>
</template>
<script>
export default {
	async fetch() {
		await this.check();
	},
	data() {
		return {
			isPermision: 0
		}
	},
	watch: {
		isPermision(nv) {
			if (nv === 1) {
				return
			} else {
				this.check();

			}
		}
	},
	methods: {
		setPermisin() {
			this.isPermision = ''
			this.isPermision = 1
			this.$router.push('/');
		},
		check() {
			window.onbeforeunload = function () {
				return "Dude, are you sure you want to leave? Think of the kittens!";
			};
			window.onunload = function () {
				null
			};
			history.pushState(null, null, location.href);
			window.onpopstate = function () {
				history.go(0);
			};
		}
	},
}
</script>
<style lang="">
	
</style>