<template lang="pug">
div
	.flex.items-center.justify-between.my-4
		iconsBurger(class='lg:hidden', @click.native='toggleNavbar', :open='!hidden')
		ul.dir-rtl.gap-8.mt-2.font-tajawal.text-base.text-gray-700.hidden(class='lg:flex')
			li(
				v-for='(item, index) in [{ title: "لماذا نحن؟", link: "#who-we-are" }, { title: "خدماتنا", link: "#our-services" }, { title: "كيف يمكن ان نساعدك؟", link: "#how-can-we-help" },]',
				:key='index',
				class='hover:text-gray-600'
			) 
				nuxt-link(:to='item.link') {{ item.title }}
		img.w-8(
			src='~assets/images/logo.svg',
			alt='WahibWorks Logo',
			draggable='false'
		)
		a(class='lg:hidden', href='tel:212773813843')
			iconsPhone.w-6
	div(:class='{ hidden: hidden }')
		ul.gap-2.font-tajawal.text-base.text-gray-700.flex.flex-col.text-right.bg-gray-100.rounded-lg.shadow-lg.p-2.absolute.z-10(
			class='w-4/5 lg:hidden md:p-4'
		)
			li.text-sm.text-gray-700.rounded-lg(
				v-for='(item, index) in [{ title: "لماذا نحن؟", link: "#who-we-are" }, { title: "خدماتنا", link: "#our-services" }, { title: "كيف يمكن ان نساعدك؟", link: "#how-can-we-help" },]',
				:key='index',
				class='hover:text-black hover:bg-gray-200'
			) 
				nuxt-link.block.p-4(:to='item.link') {{ item.title }}
			button.flex.items-center.justify-between.w-full.p-4.text-sm.text-gray-200.transition-all.rounded-lg.blue-glassmorphism(
				class='hover:bg-green hover:text-gray-100'
				@click='goto("https://calendly.com/wahibworks")'
			) 
				iconsLeftArrow
				div حجز مكالمة فيديو مجانية الآن
</template>

<script>
export default {
	name: 'NavbarComponent',
	data() {
		return {
			hidden: true,
		};
	},
	methods: {
		toggleNavbar() {
			this.hidden = !this.hidden;
		},
		goto(url) {
			window.open(url, '_blank');
		},
	},
};
</script>
