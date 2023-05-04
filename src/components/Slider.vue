<template>
	<swiper
		:modules="modules"
		:slides-per-view="1"
		navigation
		:pagination="{ clickable: true }"
		@swiper="onSwiper"
		@slideChange="onSlideChange"
	>
		<swiper-slide class="slide">
			<div class="slide-item slide-itemA">
				<img
					class="slide--image"
					src="../assets/images/people-min_1.webp"
					alt="people"
					@click="lightbox"
				/>
			</div>
			<div class="slide-item slide-itemB">
				<img
					class="slide--image"
					src="../assets/images/truck-min.webp"
					alt="truck"
					@click="lightbox"
				/>
			</div>
			<div class="slide-item slide-itemC">
				<img
					class="slide--image"
					src="../assets/images/people-min_1.webp"
					alt="people"
					@click="lightbox"
				/>
			</div>
			<div class="slide-item slide-itemD">
				<img
					class="slide--image"
					src="../assets/images/truck-min.webp"
					alt="truck"
					@click="lightbox"
				/>
			</div>
			<div class="slide-item slide-itemE">
				<img
					class="slide--image"
					src="../assets/images/truck-min.webp"
					alt="truck"
					@click="lightbox"
				/>
			</div>
			<div class="slide-item slide-itemF">
				<img
					class="slide--image"
					src="../assets/images/truck-min.webp"
					alt="truck"
					@click="lightbox"
				/>
			</div>
		</swiper-slide>
		<swiper-slide class="slide"
			><div class="slide-item slide-itemA">
				<img
					class="slide--image"
					src="../assets/images/truck-min.webp"
					alt="truck"
					@click="lightbox"
				/>
			</div>
			<div class="slide-item slide-itemB">
				<img
					class="slide--image"
					src="../assets/images/truck-min.webp"
					alt="truck"
					@click="lightbox"
				/>
			</div>
			<div class="slide-item slide-itemC">
				<img
					class="slide--image"
					src="../assets/images/truck-min.webp"
					alt="truck"
					@click="lightbox"
				/>
			</div>
			<div class="slide-item slide-itemD">
				<img
					class="slide--image"
					src="../assets/images/truck-min.webp"
					alt="truck"
					@click="lightbox"
				/>
			</div>
			<div class="slide-item slide-itemE">
				<img
					class="slide--image"
					src="../assets/images/truck-min.webp"
					alt="truck"
					@click="lightbox"
				/>
			</div>
			<div class="slide-item slide-itemF">
				<img
					class="slide--image"
					src="../assets/images/truck-min.webp"
					alt="truck"
					@click="lightbox"
				/></div
		></swiper-slide>
		<swiper-slide class="slide"
			><div class="slide-item slide-itemA">
				<img
					class="slide--image"
					src="../assets/images/truck-min.webp"
					alt="truck"
					@click="lightbox"
				/>
			</div>
			<div class="slide-item slide-itemB">
				<img
					class="slide--image"
					src="../assets/images/truck-min.webp"
					alt="truck"
					@click="lightbox"
				/>
			</div>
			<div class="slide-item slide-itemC">
				<img
					class="slide--image"
					src="../assets/images/truck-min.webp"
					alt="truck"
					@click="lightbox"
				/>
			</div>
			<div class="slide-item slide-itemD">
				<img
					class="slide--image"
					src="../assets/images/truck-min.webp"
					alt="truck"
					@click="lightbox"
				/>
			</div>
			<div class="slide-item slide-itemE">
				<img
					class="slide--image"
					src="../assets/images/truck-min.webp"
					alt="truck"
					@click="lightbox"
				/>
			</div>
			<div class="slide-item slide-itemF">
				<img
					class="slide--image"
					src="../assets/images/truck-min.webp"
					alt="truck"
					@click="lightbox"
				/></div
		></swiper-slide>
	</swiper>
</template>
<script>
import { Navigation, Pagination, Scrollbar, A11y } from 'swiper';
import { Swiper, SwiperSlide } from 'swiper/vue';

import 'swiper/css';
import 'swiper/css/navigation';
import 'swiper/css/pagination';
import 'swiper/css/scrollbar';

export default {
	components: {
		Swiper,
		SwiperSlide,
	},
	setup() {
		function lightbox(e) {
			const div = document.createElement('div');
			div.classList.add('lightbox');
			const img = e.srcElement.cloneNode(true);
			img.classList.add('lightbox-img');
			img.classList.remove('slide--image');

			div.appendChild(img);
			const close = document.createElement('span');
			close.innerHTML =
				'<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 384 512"><!--! Font Awesome Pro 6.4.0 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2023 Fonticons, Inc. --><path d="M342.6 150.6c12.5-12.5 12.5-32.8 0-45.3s-32.8-12.5-45.3 0L192 210.7 86.6 105.4c-12.5-12.5-32.8-12.5-45.3 0s-12.5 32.8 0 45.3L146.7 256 41.4 361.4c-12.5 12.5-12.5 32.8 0 45.3s32.8 12.5 45.3 0L192 301.3 297.4 406.6c12.5 12.5 32.8 12.5 45.3 0s12.5-32.8 0-45.3L237.3 256 342.6 150.6z"/></svg>';
			close.classList.add('lightbox-close');
			close.onclick = function () {
				document.querySelector('.lightbox').remove();
				document.body.classList.remove('fixed');
				document.querySelector('.swiper').scrollIntoView();
			};
			div.appendChild(close);
			document.body.classList.add('fixed');
			document.body.appendChild(div);
		}

		const onSwiper = (swiper) => {
			// console.log(swiper);
		};
		const onSlideChange = () => {
			// console.log('slide change');
		};
		return {
			lightbox,
			onSwiper,
			onSlideChange,
			modules: [Navigation, Pagination, Scrollbar, A11y],
		};
	},
};
</script>
<style lang="scss" scoped>
.slide {
	display: grid;
	grid-template-columns: repeat(4, 1fr);
	height: 678px;
	gap: 24px;

	&-itemB {
		grid-column: 2 / 4;
	}

	&-itemF {
		grid-column: 3 / 5;
	}
	&--image {
		width: 100%;
		height: 100%;
		overflow: hidden;
		object-fit: cover;
	}
	&--image:hover {
		cursor: pointer;
	}
}

@media (max-width: 768px) {
	.slide {
		grid-template-columns: repeat(2, 1fr);
		height: 756px;
		gap: 16px;
		&-itemA,
		&-itemB,
		&-itemC,
		&-itemD,
		&-itemE,
		&-itemF {
			height: 170px;
		}
		&-itemA,
		&-itemD {
			grid-column: 1/3;
		}

		&-itemB {
			grid-column: unset;
		}

		&-itemF {
			grid-column: unset;
		}
	}
}
</style>
