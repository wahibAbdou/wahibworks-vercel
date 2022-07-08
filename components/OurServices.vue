<template lang="pug">
#our-services.bg-ww-blue.py-24
	.mx-auto.text-center(class='w-4/5 lg:w-2/3')
		.gap-1.mb-11
			h1.font-amiri.text-3xl.pt-4.pb-2.text-gray-100(class='md:text-4xl') خدماتنا
			p.text-gray-300.font-tajawal.text-xs خدماتنا في تطور مستمر لتناسب متطلبات السوق
		.flex.flex-wrap.justify-center
			.py-8(
				v-for='(item, index) in data',
				:key='index',
				class='md:px-11 lg:px-8 w-11/12 md:w-1/2 2xl:w-1/4'
			)
				.rounded-card.px-11.py-16(:class='`2xl:h-100 ${item.bgColor}`')
					img.mx-auto.w-44.buzz-out-on-hover.mb-6(
						:src='item.image',
						alt='WahibWorks Agency',
						draggable='false'
					)
					h1.font-amiri.text-2xl.text-ww-blue.mb-6 {{ item.title }}
					p.font-tajawal.text-xs.text-gray-600 {{ item.description }}
</template>

<script>
	export default {
		name: 'OurServices',
		data() {
			return {
				data: [
					{
						image: require('~/assets/images/OurServices/1.png'),
						title: 'بناء الهوية التجارية',
						description:
							'نصمم بكل احترافية علامة تجارية فريدة تحمل اهم قيم مشروعك ، لأنها اهم خطوة لبروز مشروعك.',
						bgColor: 'bg-ww-green',
					},
					{
						image: require('~/assets/images/OurServices/2.png'),
						title: 'البرمجة',
						description:
							'نبرمج مواقع، تطبيقات ونطور أنظمة وقواعد البيانات التي ستساعدك بشكل كبير على تحسين نموك',
						bgColor: 'bg-ww-pink',
					},
					{
						image: require('~/assets/images/OurServices/3.png'),
						title: 'الإنتاج المرئي',
						description:
							'نقوم بإنتاج كل ما يرغب به عملاؤنا من تصوير وتعديل على الفيديوهات بكل دقة و احترافية',
						bgColor: 'bg-ww-lightblue',
					},
					{
						image: require('~/assets/images/OurServices/4.png'),
						title: 'التسويق الرقمي',
						description:
							'نساعد عملاءنا على تطوير وتحسين حملاتهم الاعلانية على جميع المنصات، ئ الجمهور .الأنسب لمشروعهم',
						bgColor: 'bg-ww-yellow',
					},
				],
			}
		},
	}
</script>