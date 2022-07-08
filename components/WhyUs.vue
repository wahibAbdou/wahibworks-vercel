<template lang="pug">
.mx-auto(class='w-1/2 md:w-2/3')
	.gap-1.mb-32
		h1.font-amiri.text-3xl.pt-4.pb-2.text-ww-blue(class='md:text-4xl') لماذا نحن؟
		p.text-gray-600.font-tajawal.text-xs لتأطير اهداف مشروعك وضمان استمرارها واستقرارها
	.flex.flex-col.space-y-28
		.flex.flex-col.gap-5.text-center.space-y-28.items-center(
			class='lg:space-y-0 lg:flex-row'
		)
			.card.bg-ww-blue.text-white.pb-6.w-56(
				class='lg:w-full',
				v-for='(item, index) in data[0]',
				:key='index'
			)
				img.mx-auto.w-44.buzz-out-on-hover(
					:src='item.image',
					alt='WahibWorks Agency'
				)
				h1.text-xl.mb-2 {{ item.title }}
				p.px-8.text-gray-300.text-xs {{ item.description }}
		.flex.flex-col.gap-5.text-center.space-y-28.items-center(
			class='lg:space-y-0 lg:flex-row'
		)
			.card.bg-ww-blue.text-white.pb-6.w-56(
				class='lg:w-full',
				v-for='(item, index) in data[1]',
				:key='index'
			)
				img.mx-auto.w-44.buzz-out-on-hover(
					:src='item.image',
					alt='WahibWorks Agency'
				)
				h1.text-xl.mb-2 {{ item.title }}
				p.px-8.text-gray-300.text-xs {{ item.description }}
</template>

<script>
	export default {
		name: 'WhyUs',
		data() {
			return {
				data: [
					[
						{
							title: 'الإستراتيجيات والدقة',
							description:
								'نعمل دائما على بناء استراتيجيات ناجحة لضمان نجاح واستمرارية مشروعك',
							image: require('~/assets/images/WhyChooseUs/1.png'),
						},
						{
							title: 'فريق مبدع',
							description:
								'نقوم على إجاد لمسة إبداعية وفنية لمشروعك، كي يتميز وينفرد عن باقي المشاريع الاخرى',
							image: require('~/assets/images/WhyChooseUs/2.png'),
						},
						{
							title: 'الجودة العالية',
							description:
								'لطالما عملنا على إعطاء اقصى جهودنا لأننا لا نرضى الا بأفضل النتائج، لأن هدفنا بالأساس إنجاح مشروعك',
							image: require('~/assets/images/WhyChooseUs/4.png'),
						},
					],
					[
						{
							title: 'المواكبة',
							description:
								'نستمر بمراقبة رحلة تطور مشروعك ليستمر في التقدم والنجاح',
							image: require('~/assets/images/WhyChooseUs/6.png'),
						},
						{
							title: 'نتائج فوق المتوقع',
							description:
								'نحرص على الوصول الى أفضل النتائج، لأننا نعمل بكل حب وفخر لأنها أساس سمعتنا',
							image: require('~/assets/images/WhyChooseUs/5.png'),
						},
						{
							title: 'الالتزام بموعد التسليم',
							description:
								'نمنحك جدولا زمنيا لتنفيذ كل مرحلة وخصوصا الالتزام بالموعد المحدد للتسليم النهائي',
							image: require('~/assets/images/WhyChooseUs/3.png'),
						},
					],
				],
			}
		},
	}
</script>

<style scoped>
	.card {
		border-radius: 60px;
	}

	.card img {
		margin-top: -90px;
	}

	@-webkit-keyframes buzz-out-on-hover {
		10% {
			-webkit-transform: translateX(3px) rotate(2deg);
			transform: translateX(3px) rotate(2deg);
		}
		20% {
			-webkit-transform: translateX(-3px) rotate(-2deg);
			transform: translateX(-3px) rotate(-2deg);
		}
		30% {
			-webkit-transform: translateX(3px) rotate(2deg);
			transform: translateX(3px) rotate(2deg);
		}
		40% {
			-webkit-transform: translateX(-3px) rotate(-2deg);
			transform: translateX(-3px) rotate(-2deg);
		}
		50% {
			-webkit-transform: translateX(2px) rotate(1deg);
			transform: translateX(2px) rotate(1deg);
		}
		60% {
			-webkit-transform: translateX(-2px) rotate(-1deg);
			transform: translateX(-2px) rotate(-1deg);
		}
		70% {
			-webkit-transform: translateX(2px) rotate(1deg);
			transform: translateX(2px) rotate(1deg);
		}
		80% {
			-webkit-transform: translateX(-2px) rotate(-1deg);
			transform: translateX(-2px) rotate(-1deg);
		}
		90% {
			-webkit-transform: translateX(1px) rotate(0);
			transform: translateX(1px) rotate(0);
		}
		100% {
			-webkit-transform: translateX(-1px) rotate(0);
			transform: translateX(-1px) rotate(0);
		}
	}
	@keyframes buzz-out-on-hover {
		10% {
			-webkit-transform: translateX(3px) rotate(2deg);
			transform: translateX(3px) rotate(2deg);
		}
		20% {
			-webkit-transform: translateX(-3px) rotate(-2deg);
			transform: translateX(-3px) rotate(-2deg);
		}
		30% {
			-webkit-transform: translateX(3px) rotate(2deg);
			transform: translateX(3px) rotate(2deg);
		}
		40% {
			-webkit-transform: translateX(-3px) rotate(-2deg);
			transform: translateX(-3px) rotate(-2deg);
		}
		50% {
			-webkit-transform: translateX(2px) rotate(1deg);
			transform: translateX(2px) rotate(1deg);
		}
		60% {
			-webkit-transform: translateX(-2px) rotate(-1deg);
			transform: translateX(-2px) rotate(-1deg);
		}
		70% {
			-webkit-transform: translateX(2px) rotate(1deg);
			transform: translateX(2px) rotate(1deg);
		}
		80% {
			-webkit-transform: translateX(-2px) rotate(-1deg);
			transform: translateX(-2px) rotate(-1deg);
		}
		90% {
			-webkit-transform: translateX(1px) rotate(0);
			transform: translateX(1px) rotate(0);
		}
		100% {
			-webkit-transform: translateX(-1px) rotate(0);
			transform: translateX(-1px) rotate(0);
		}
	}
	.buzz-out-on-hover {
		display: inline-block;
		vertical-align: middle;
		-webkit-transform: perspective(1px) translateZ(0);
		transform: perspective(1px) translateZ(0);
		box-shadow: 0 0 1px rgba(0, 0, 0, 0);
	}
	.buzz-out-on-hover:hover,
	.buzz-out-on-hover:focus,
	.buzz-out-on-hover:active {
		-webkit-animation-name: buzz-out-on-hover;
		animation-name: buzz-out-on-hover;
		-webkit-animation-duration: 0.75s;
		animation-duration: 0.75s;
		-webkit-animation-timing-function: linear;
		animation-timing-function: linear;
		-webkit-animation-iteration-count: 1;
		animation-iteration-count: 1;
	}
</style>