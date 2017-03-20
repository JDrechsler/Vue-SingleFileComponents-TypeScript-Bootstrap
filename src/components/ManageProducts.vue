<template>
	<div>
		<h3>ManageProducts-Component</h3>
		<button class="btn btn-success" @click="addRandom">Add random number</button>
		<span v-for="(numb,index) in randomNumbers">{{numb}},</span>
		<ProductList></ProductList>
	</div>
</template>

<script lang="ts">
	import Vue from 'vue'
	import Component from 'vue-class-component'
	import ProductList from './ProductList.vue'
	import { ClassTest } from './classtest.ts';
	import * as _ from 'lodash'

	@Component({
		components: {
			ProductList
		}
	})
	export default class ManageProducts extends Vue {

		randomNumbers: Array<number> = [1, 2, 3]

		addRandom() {
			this.randomNumbers.push(_.random(1, 9))
			var tes = new ClassTest()
			tes.sayHello()
		}

	}

</script>
