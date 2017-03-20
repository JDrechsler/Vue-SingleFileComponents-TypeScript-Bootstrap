<template>
	<section>
		<h3>ManageProducts-Component</h3>
		<SaveProductForm :product="productInForm"></SaveProductForm>
		<ProductList :products="products"></ProductList>
	</section>
</template>

<script lang="ts">
	import Vue from 'vue'
	import Component from 'vue-class-component'
	import uuid from 'uuid';
	import SaveProductForm from './SaveProductForm.vue';
	import ProductList from './ProductList.vue'
	import * as _ from 'lodash'

	@Component({
		components: {
			ProductList,
			SaveProductForm
		}
	})
	export default class ManageProducts extends Vue {

		initialData() {
			return {
				productInForm: {
					id: null,
					name: '',
					description: '',
					price: null
				}
			}
		}

		productInForm = {
			id: null,
			name: '',
			description: '',
			price: null
		}

		products = [
			{
				id: 'cc919e21-ae5b-5e1f-d023-c40ee669520c',
				name: 'COBOL 101 vintage',
				description: 'Learn COBOL with this vintage programming book',
				price: 399,
			},
			{
				id: 'bcd755a6-9a19-94e1-0a5d-426c0303454f',
				name: 'Sharp C2719 curved TV',
				description: 'Watch TV like never before with the brand new curved screen technology',
				price: 1995,
			},
			{
				id: '727026b7-7f2f-c5a0-ace9-cc227e686b8e',
				name: 'Remmington X mechanical keyboard',
				description: 'Excellent for gaming and typing, this Remmington X keyboard ' +
				'features tactile, clicky switches for speed and accuracy',
				price: 595,
			}
		]

		// onFormSave(product) {
		// 	const index = this.products.findIndex((p) => p.id === product.id);
		// 	if (index !== -1) {
		// 		this.products.splice(index, 1, product)
		// 	} else {
		// 		product.id = uuid.v4();
		// 		this.products.push(product);
		// 	}
		// 	this.resetProductInForm();
		// }

		// resetProductInForm() {
		// 	this.productInForm = initialData().productInForm;
		// }

		// onEditClicked(product) {
		// 	// since objects are passed by reference we need to clone the product
		// 	// either by using Object.assign({}, product) or by using object
		// 	// spread like we do here.
		// 	this.productInForm = { ...product };
		// }

	}

</script>
