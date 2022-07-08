<template lang="pug">
.mx-auto.text-center.mt-36.mb-24(class='lg:mb-32')
	h1.font-noto.text-4xl.p-4.mb-5.leading-relaxed(
		class='md:text-6xl lg:text-7xl md:mb-14'
	) رحلة جديدة لمشروعك
	p.dir-rtl.font-tajawal.text-gray-600.text-sm.mb-6(class='md:text-base lg:px-8') ترتكز وكالتنا على إعطاء أفضل التجارب في العالم الرقمي التي يحتاجها عملائنا لضمان نجاح مشاريعهم، وذلك بدءا من خدمة إنشاء العلامات التجارية، وتصميم مواقع الويب وخدمات التسويق الإلكتروني، وذلك لمواكبة تغيرات الوقت الراهن. يعمل فريقنا بإحترافية لأخذكم في رحلة نجاح فريدة من نوعها، لأن نجاحكم أساس نجاحنا.
	button.flex.items-center.text-white.mx-auto.px-4.rounded-full.text-sm.font-tajawal.blue-glassmorphism.transform.transition.duration-400.ease-in-out.mb-4(
		class='py-2.5 gap-1.5 hover:bg-ww-hoverblue hover:scale-105 hover:shadow-lg md:px-6 md:py-3 md:text-base',
		@click='goto("https://calendly.com/wahibworks")'
	)
		.mt-1 حجز مكالمة فيديو مجانية الآن
		iconsVideoCall
	.text-sm.cursor-pointer.mb-28.text-gray-600(class="hover:underline hover:text-gray-800" @click='goto("https://api.whatsapp.com/send/?phone=212773813843&text&type=phone_number&app_absent=0")') أو تواصلوا معنا عبر الواتساب

	iconsDownArrow#arrowDown.mx-auto
</template>

<script>
export default {
	name: 'BannerComponent',
	mounted() {
		this.$gsap
			.fromTo(
				'#arrowDown',
				{ y: 0, opacity: 0 },
				{ y: 25, opacity: 1, duration: 2.5, ease: 'elastic.out(1,0.3)' }
			)
			.repeat(-1);
	},
	methods: {
		goto(url) {
			window.open(url, '_blank');
		},
	},
};
</script>