<template>
	<div class="breadcrumbs">
		<Home class="breadcrumbs--home-icon" />
		<h5 class="breadcrumbs--link breadcrumbs--link---home">Startseite</h5>
		<ArrowRight class="breadcrumbs--arrow-icon" />
		<h5 class="breadcrumbs--link breadcrumbs--link---active">Uber Uns</h5>
	</div>
</template>

<script setup>
import Home from '../assets/svg/home.vue';
import ArrowRight from '../assets/svg/ArrowRight.vue';
</script>

<style lang="scss" scoped>
.breadcrumbs {
	display: flex;
	align-items: center;
	gap: 8px;
	margin: 40px 0px 40px 130px;

	&--home-icon {
		height: 24px;
		width: auto;
	}
	&--link---home {
		font-size: 14px;
		line-height: 22px;
		color: #667085;
	}
	&--arrow-icon {
		height: 16px;
	}
	&--link {
		cursor: pointer;
	}
	&--link---active {
		color: #204497;
		font-weight: 900;
	}
}
@media (max-width: 768px) {
	.breadcrumbs {
		gap: 8px;
		margin: 40px 0px 40px 16px;
	}
}
</style>
