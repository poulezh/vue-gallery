<template>
	<v-container>
		<Photo v-for="photo in photos" :key="photo.id"
		:photo="photo">
			
		</Photo>

	</v-container>
</template>

<script>
import Photo from '@/components/photo/Photo.vue';
	export default {
    data: () => ({
        photos: []
    }),
    components: { Photo },
	mounted(){
		
	}
}
</script>

<style scoped>

</style>