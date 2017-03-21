<template>
	<section>
		<h3>SocketTest-Component</h3>
		<button class="btn btn-success btn-sm" @click="loadSocketTest">Load socket.ts</button>
	</section>
</template>

<script lang="ts">
	import Vue from 'vue'
	import Component from 'vue-class-component'

	@Component({
		components: {

		}
	})
	export default class SocketTest extends Vue {
		loadSocketTest() {
			require('./SocketTest.ts')
		}
	}

</script>
