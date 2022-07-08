<template lang="pug">
#who-we-are.flex.flex-col(class='lg:flex-row')
	.bg-blue.squares.hidden(class='xl:block lg:w-1/3')
	.bg-ww-beige.flex-1.text-center.pt-14.pb-20.space-y-20
		ClientsTrustUs
		WhyUs
</template>

<script>
	export default {
		name: 'SectionOne',
	}
</script>

<style scoped>
	.squares {
		background: url('~/assets/images/squares.png');
		background-size: contain;
	}
</style>