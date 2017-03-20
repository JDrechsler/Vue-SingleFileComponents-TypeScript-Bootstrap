<template>
	<div id="app" class="container-fluid">
		<img src="./assets/logo.png">

		<div class="row">
			<div class="col-md-12">
				<ManageProducts></ManageProducts>
			</div>
		</div>
	</div>
</template>

<script lang="ts">
	import Vue from 'vue'
	import Component from 'vue-class-component'

	import ManageProducts from './components/ManageProducts.vue'
	import SaveProductForm from './components/SaveProductForm.vue'

	@Component({
		components: {
			ManageProducts,
			SaveProductForm
		}
	})

	export default class App extends Vue {

	}

</script>

<style>
	#app {
		font-family: 'Avenir', Helvetica, Arial, sans-serif;
		-webkit-font-smoothing: antialiased;
		-moz-osx-font-smoothing: grayscale;
		color: #2c3e50;
		background-color: mintcream;
	}

</style>
