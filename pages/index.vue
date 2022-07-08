<template lang="pug">
div
	.mb-4
		LogoSlider(:inverse='true')
		.mx-auto(class='w-4/5 lg:w-2/3')
			Navbar
			Banner
		LogoSlider(:inverse='false')
	div
		SectionOne
		SectionTwo
		OurServices
		CTASection
		Footer
</template>

<script>
	export default {
		name: 'IndexPage',
	}
</script>
