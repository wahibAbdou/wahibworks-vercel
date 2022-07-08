<template lang="pug">
div
	.gap-1
		h1.font-amiri.text-3xl.pt-4.pb-2.text-ww-blue(class='md:text-4xl') عملاء يضعون ثقتهم بنا
		p.text-gray-600.font-tajawal.text-xs نعتز بكل عملائنا ونفتخر بهم
	.flex.flex-row.items-center.justify-center.gap-6.mt-10(class='md:gap-11')
		img.w-10(
			class='md:w-14',
			src='~/assets/images/clients/nrz-consulting.png',
			alt='WahibWorks Agency Client'
		)
		img.w-24(
			class='md:w-28',
			src='~/assets/images/clients/wahibfarms.png',
			alt='WahibWorks Agency Client'
		)
		img.w-10(
			class='md:w-14',
			src='~/assets/images/clients/giab.svg',
			alt='WahibWorks Agency Client'
		)
</template>

<script>
	export default {
		name: 'ClientsTrustUs',
	}
</script>