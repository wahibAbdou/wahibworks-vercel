<template lang="pug">
div
	Hooper(:settings='hooperSettings')
		Slide(v-for='(item, index) in data', :key='index')
			div
				.px-14.pt-8.pb-28.text-center.h-card(class='lg:border-l md:px-6 lg:px-20')
					img.w-44.mb-4.mx-auto(class='lg:w-56', :src='item.image', draggable='false')
					div
						.flex.gap-2.justify-center
							.w-6.h-6.bg-ww-blue.text-white.rounded.mb-4.text-xs.pt-1(v-if='index') {{ index }}
							h1.text-xl.mb-2.text-gray-700.font-semibold {{ item.title }}
						p.text-sm.text-gray-600 {{ item.description }}
		Pagination(slot='hooper-addons')
</template>

<script>
import { Hooper, Slide, Pagination } from 'hooper';
import 'hooper/dist/hooper.css';
export default {
	name: 'SectionTwo',
	components: {
		Hooper,
		Slide,
		Pagination,
	},
	data() {
		return {
			data: [
				{
					image: require('~/assets/images/OurProcess/0.png'),
					title: 'كيف نعمل؟',
					description: 'لتأطير اهداف مشروعك وضمان استمرارها واستقرارها',
					backgroundClass: 'artwork-1',
				},
				{
					image: require('~/assets/images/OurProcess/1.png'),
					title: 'التواصل بين الطرفين',
					description:
						'نقوم بإجراء مكالمة او تحديد موعد من اجل التعرف عليك وعلى اهداف مشروعك، اهم خطوة .لبداية سلسة وناجحة',
					backgroundClass: 'bg-red-100',
				},
				{
					image: require('~/assets/images/OurProcess/2.png'),
					title: 'تقديم اقتراحات والمناقشة',
					description:
						'بعد بحث مكثف، سنقدم لك اقتراحا يحتوي على توصياتنا ورسومنا وفتح مجال للنقاش',
					backgroundClass: 'bg-green-100',
				},
				{
					image: require('~/assets/images/OurProcess/3.png'),
					title: 'الدفع والعقد',
					description:
						'بمجرد الاتفاق بين الطرفين على الأهداف والرسوم، ننتقل الى تسديد اول دفعة وتوقيع عقد عمل',
					backgroundClass: 'bg-green-100',
				},
				{
					image: require('~/assets/images/OurProcess/4.png'),
					title: 'البدأ الفوري',
					description:
						'أفضل مرحلة، حان الوقت لننطلق في رحلتنا لتحقيق أهدافك واستخدام خلطتنا السحرية',
					backgroundClass: 'bg-yellow-100',
				},
				{
					image: require('~/assets/images/OurProcess/5.png'),
					title: 'تلقي مداخلاتك وأفكارك',
					description:
						'.سنطلعك على كل ما وصلنا اليه، لفتح مجال من اجل تلقي مداخلاتك وافكارك لتصبح أكثر مثالية',
					backgroundClass: 'bg-yellow-100',
				},
				{
					image: require('~/assets/images/OurProcess/6.png'),
					title: 'جولات المراجعة',
					description:
						'بعد تلقي مداخلاتك، سنبدل قصارى جهودنا لتنفيذها وتحديث ما وصلنا اليه، لإتمامها في أسرع .وقت ممكن',
					backgroundClass: 'bg-blue-100',
				},
				{
					image: require('~/assets/images/OurProcess/7.png'),
					title: 'التسليم النهائي',
					description:
						'اقتربت على انهاء رحلتك، حان الوقت لنقدم  لك تقريرا كاملا مع جميع ملفات مشروعك الذي بنيناه معًا',
					backgroundClass: 'bg-blue-100',
				},
				{
					image: require('~/assets/images/OurProcess/8.png'),
					title: 'الدفع والإطلاق',
					description:
						'تهانينا 🎉 لقد وصلنا الى اخر محطة، حان الوقت لنحتفل بما انجزناه معا وتسديد باقي الرسوم',
					backgroundClass: 'bg-pink-100',
				},
			],
			hooperSettings: {
				itemsToShow: 1,
				rtl: true,
				breakpoints: {
					768: {
						centerMode: false,
						itemsToShow: 2.5,
					},
					1024: {
						itemsToShow: 2.5,
					},
					1280: {
						itemsToShow: 3.5,
					},
				},
			},
		};
	},
};
</script>

<style>
.hooper-list,
.hooper {
	height: 430px !important;
}

.hooper-list:hover {
	cursor: grabbing;
	cursor: -moz-grabbing;
	cursor: -webkit-grabbing;
}

.hooper-indicator {
	background-color: #ffee99 !important;
	cursor: pointer;
}

.hooper-indicator:hover,
.hooper-indicator.is-active {
	background-color: #181735 !important;
}

.hooper-pagination {
	bottom: 35px !important;
}

@media only screen and (min-width: 768px) {
	.hooper-pagination {
		display: none !important;
	}
}

.artwork-1 {
	width: 500px;
	right: -204px;
	bottom: -93px;
	position: absolute;
}
</style>