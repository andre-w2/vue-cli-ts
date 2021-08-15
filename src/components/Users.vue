<template>
	<button @click="handleClick('login')" >order by login</button>
	<button @click="handleClick('name')" >order by name</button>
	<List :users="user" :order="order" />
</template>

<script lang="ts">
import { defineComponent, ref } from 'vue';
import Users from '@/types/Users';
import List from './List.vue';
import OrderTemp from '@/types/OrderTypes';

export default defineComponent({
	components: {List},
	setup() {
		const user = ref<Users[]>([
			{id: 1, login: 'dsada12', name: 'david'},
			{id: 2, login: 'dsada23212', name: 'david2'},
			{id: 3, login: 'dsad3232a12', name: 'david32'},

		])
		const order = ref<OrderTemp>('login')

		const handleClick = (term: OrderTemp) => {
			order.value = term
		}

		return {user,handleClick,order}
	}
})
</script>