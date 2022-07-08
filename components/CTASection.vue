<template lang="pug">
#how-can-we-help
	LogoSlider
	.mx-auto.text-center.mt-32.mb-24.relative(class='lg:mt-36 lg:mb-32')
		img.opacity-30.absolute.-top-16.z-11(
			class='lg:-top-32',
			src='~/assets/images/cupid-print.png'
		)
		h1.font-noto.text-4xl.p-4.mb-5.leading-relaxed(class='md:text-6xl md:mb-14') لقد حان الوقت للانتقال للعالم الرقمي
		p.dir-rtl.font-tajawal.text-gray-600.text-sm.mb-6(class='md:text-base lg:px-8') متشوّقون للعمل معا! نود أن نسمع عن مشروعك
		button.flex.items-center.text-white.mx-auto.px-4.rounded-full.text-sm.font-tajawal.blue-glassmorphism.transform.transition.duration-400.ease-in-out.mb-28(
			class='py-2.5 gap-1.5 hover:bg-ww-hoverblue hover:scale-105 hover:shadow-lg md:px-6 md:py-3 md:text-base',
			@click='goto("https://calendly.com/wahibworks")'
		)
			.mt-1 حجز مكالمة فيديو مجانية الآن
			iconsVideoCall
	LogoSlider(:inverse='true')
</template>

<script>
	export default {
		name: 'CTASection',
		methods: {
			goto(url) {
				window.open(url, '_blank')
			},
		},
	}
</script>

<style>
</style>