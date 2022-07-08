<template lang="pug">
.logo-slider
	div(:class='inverse ? "slider-track-inverse" : "slider-track"')
		.slide(
			v-for='(item, index) in [1, 2, 3, 4, 5, 6, 7, 1, 2, 3, 4, 5, 6, 7, 1, 2, 3, 4, 5, 6, 7, 1, 2, 3, 4, 5, 6, 7, 1, 2, 3, 4, 5, 6, 7, 1, 2, 3, 4, 5, 6, 7]',
			:key='index'
		)
			img.w-10(
				src='/logo.png',
				alt='WahibWorks Agency, A new journey for your business.',
				draggable='false'
			)
</template>

<script>
export default {
	name: 'LogoSlider',
	props: {
		inverse: {
			type: Boolean,
		},
	},
}
</script>

<style scoped>
.logo-slider {
	direction: ltr;
	max-width: 100vw;
	overflow: hidden;
	position: relative;
	margin: auto;
}

.logo-slider .slider-track {
	gap: 20px;
	display: flex;
	width: calc(82.51px * 42);
	animation: scroll 25s infinite linear;
}

.logo-slider .slider-track-inverse {
	gap: 20px;
	display: flex;
	width: calc(82.51px * 42);
	animation: scrollInverse 25s infinite linear;
}

.logo-slider .slide img {
	width: auto;
}

@keyframes scroll {
	0% {
		transform: translateX(0%);
	}
	100% {
		transform: translateX(calc(-47.3px * 21));
	}
}

@keyframes scrollInverse {
	0% {
		transform: translateX(calc(-47.3px * 21));
	}
	100% {
		transform: translateX(0%);
	}
}
</style>
