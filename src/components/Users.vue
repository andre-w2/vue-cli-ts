<template>
	<List :users="user" />
</template>

<script lang="ts">
import { defineComponent, ref } from 'vue';
import Users from '@/types/Users';
import List from './List.vue';

export default defineComponent({
	components: {List},
	setup() {
		const user = ref<Users[]>([
			{id: 1, login: 'dsada12', name: 'david'},
			{id: 2, login: 'dsada23212', name: 'david2'},
			{id: 3, login: 'dsad3232a12', name: 'david32'},

		])

		return {user}
	}
})
</script>