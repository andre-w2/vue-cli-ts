<template>
	<div>
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
	
export default defineComponent({
	props: {
		users: {
			required: true,
			type: Array as PropType<Users[]>
		}
	}
})
</script>