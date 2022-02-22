<template>
	<button @click="eliminar(contact.id)" class="btn btn-danger">Eliminar</button>
</template>
<script>

	export default {
		props:{
	 		ContactEliminar: null
	 	},
	 	methods: {
	 		async eliminar(id) {
	 			const res = await axios.delete('/contacts/' +id);
	 			this.list();
	 		},
         }

	}
</script>