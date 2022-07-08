<template lang="pug">
.flex.flex-col-reverse.mx-auto.container.py-6.px-5.items-center.gap-3(
	class='lg:flex-row lg:justify-between lg:gap-0 lg:py-4'
)
	.flex.gap-3.items-center
		//- iconsTwitter.w-4.text-gray-700(
		//- 	@click.native='goto("https://www.instagram.com/wahibworksagency/")'
		//- )
		iconsFacebook.w-4.text-gray-700(
			@click.native='goto("https://www.facebook.com/wahibworksagency/")'
		)
		iconsInstagram.w-4.text-gray-700(
			@click.native='goto("https://www.instagram.com/wahibworksagency/")'
		)
	.dir-rtl.text-gray-700.text-sm جميع الحقوق محفوظة WahibWorks Agency © {{ new Date().getFullYear() }}
</template>

<script>
	export default {
		name: 'FooterComp',
		methods: {
			goto(url) {
				window.open(url, '_blank')
			},
		},
	}
</script>

<style scoped>
	svg {
		fill: #474747;
		cursor: pointer;
	}
	svg:hover {
		fill: #616161;
	}
</style>