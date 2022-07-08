<template lang="pug">
</template>

<script>
	export default {
		name: 'WhatsApp',
	}
</script>

<style>
	.whatsapp-info,
	.pulse {
		font-family: 'Lato', sans-serif;
		display: inline-block;
		color: #fff;
		background: #1ab744;
		position: fixed;
		bottom: 50px;
		right: 50px;
		font-size: 45px;
		text-align: center;
		z-index: 99;
		border-radius: 90%;
		height: 70px;
		width: 70px;
		line-height: 70px;
		cursor: pointer;
		-webkit-transition: all 0.2s;
		-moz-transition: all 0.2s;
		transition: all 0.2s;
	}

	@-webkit-keyframes pulse {
		0% {
			-webkit-transform: scale(0.1);
			transform: scale(0.1);
			opacity: 0;
		}
		50% {
			opacity: 0.3;
		}
		100% {
			-webkit-transform: scale(2);
			transform: scale(2);
			opacity: 0;
		}
	}

	@keyframes pulse {
		0% {
			-webkit-transform: scale(0.1);
			transform: scale(0.1);
			opacity: 0;
		}
		50% {
			opacity: 0.3;
		}
		100% {
			-webkit-transform: scale(2);
			transform: scale(2);
			opacity: 0;
		}
	}

	.pulse:nth-child(1) {
		-webkit-animation: pulse 2s infinite;
		animation: pulse 2s infinite;
	}

	.pulse:nth-child(2) {
		-webkit-animation: pulse 2s infinite 0.3s;
		animation: pulse 2s infinite 0.3s;
	}

	.pulse:nth-child(3) {
		-webkit-animation: pulse 2s infinite 0.6s;
		animation: pulse 2s infinite 0.6s;
	}

	.fa {
		font: normal normal normal 14px/1 FontAwesome;
		font-size: 14px;
		font-size: inherit;
		text-rendering: auto;
		-moz-osx-font-smoothing: grayscale;
	}

	.fa-whatsapp::before {
		content: '\f234';
	}
</style>