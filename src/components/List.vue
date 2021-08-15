<template>
	<div>
		<p>{{order}}</p>
		<ul>
			<li v-for="user in users" :key="user.id">
				{{user.login}} in {{user.name}}
			</li>
		</ul>
	</div>
</template>

<script lang="ts">
import { defineComponent, PropType } from 'vue';
import Users from '@/types/Users';
import OrderTemp from '@/types/OrderTypes';
	
export default defineComponent({
	props: {
		users: {
			required: true,
			type: Array as PropType<Users[]>
		},
		order: {
			required: true,
			type: String as PropType<OrderTemp>
		}
	}
})
</script>