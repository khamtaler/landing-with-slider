<template>
	<div>
		<img class="title-image" src="../assets/images/Uber-uns-min.webp" alt="Uber uns" />
		<div class="section-welcome">
			<figure class="section-welcome--figure">
				<img class="section-welcome--image" src="../assets/images/people-min_1.webp" alt="people" />
			</figure>
			<div class="section-welcome--text-container">
				<header class="section-welcome--header">
					<h5 class="section-welcome--header-text">
						Lorem ipsum dolor sit amet, consectetur adipiscing elit. Cras dapibus, mauris efficitur
						ornare rhoncus, libero ex rutrum tortor, ut viverra mi odio ac purus. Pellentesque
						convallis id lectus auctor efficitur. Donec faucibus, magna quis tristique aliquet
					</h5>
				</header>
				<p class="section-welcome--text">
					Fusce ac finibus ipsum, vel mollis lorem. Interdum et malesuada fames ac ante ipsum primis
					in faucibus. Pellentesque suscipit quam non nulla sollicitudin hendrerit. Praesent dictum
					tempus neque. Donec et lacus quis felis ultrices mattis.
					<br /><br />
					Quisque tempor aliquet dui, sed dignissim augue varius vel. Maecenas ut lacinia orci. Sed
					efficitur finibus arcu in porta. Donec sed tempus neque, eu fringilla orci. Sed tincidunt
					nulla quis est fringilla rhoncus. In neque purus, suscipit id hendrerit quis, pulvinar
					faucibus felis.<br />
					In semper sapien sit amet dolor lobortis, interdum mollis sapien pretium. Phasellus
					euismod ullamcorper turpis vel pretium. Vivamus id convallis enim. Pellentesque eleifend
					felis sit amet elit faucibus, ac auctor urna feugiat. Sed eu sagittis urna. Pellentesque
					nunc felis, molestie a mauris et, pellentesque ultricies velit. Pellentesque elementum eu
					ante lacinia dapibus. In facilisis dolor ac felis vehicula, vitae tincidunt libero
					hendrerit.
					<br /><br />
					Donec ultricies lorem in mi tincidunt ornare. Etiam non turpis lacus. Donec scelerisque
					tellus in turpis tristique, et imperdiet sem mollis. Nam fermentum non sem id viverra. Sed
					quis arcu rutrum, ornare tortor id, lobortis metus. Fusce ornare ligula eu urna dignissim,
					ut condimentum odio tempor. Proin eu est enim. Nam lacus leo, accumsan nec quam nec,
					fermentum molestie orci. Morbi in nisi vitae arcu rutrum ornare eu at nulla.
				</p>
			</div>
		</div>
		<div class="section-about">
			<div class="section-about--text-container">
				<p class="section-about--text">
					Nunc feugiat imperdiet dolor, sit amet consectetur tortor facilisis ac. Vivamus quam
					neque, euismod porttitor magna et, finibus tincidunt justo. Nullam vehicula velit sed diam
					sagittis, eget pretium nisi mollis. Etiam in risus nibh. Curabitur feugiat pulvinar enim,
					in blandit massa suscipit id. Donec mollis vel lacus sit amet rhoncus.
				</p>
				<p class="section-about--list-header">
					Pellentesque tempus nunc sit amet erat placerat, eu varius sem sollicitudin:
				</p>
				<ul class="section-about--list">
					<li class="section-about--list-item">Nam in massa gravida</li>
					<li class="section-about--list-item">Nam in massa gravida</li>
					<li class="section-about--list-item">Nam in massa gravida</li>
				</ul>
				<p class="section-about--end-text">
					Mauris sollicitudin lorem in orci porta, ac tincidunt neque consequat. Sed dictum diam
					vehicula aliquet vehicula. Vivamus ultrices facilisis sollicitudin. Duis vel mi non eros
					porttitor imperdiet. Pellentesque tempor nunc sed mi laoreet venenatis.
				</p>
			</div>
			<figure class="section-about--figure">
				<img class="section-about--image" src="../assets/images/truck-min.webp" alt="truck" />
			</figure>
		</div>
		<Swiper />
	</div>
</template>

<script setup>
import Swiper from './Slider.vue';
</script>

<style lang="scss" scoped>
.title-image {
	width: 100%;
	margin: 0px 0px 25px 130px;
}
.section-welcome {
	display: flex;
	margin-right: 130px;

	&--figure {
		max-width: 50vw;
		margin: 14px 0px 0px 0px;
		flex-shrink: 1;
	}
	&--image {
		max-width: 100%;
		height: auto;
	}
	&--text-container {
		margin-left: 54px;
		color: #546e7a;
		flex: 1;
	}
	&--header-text {
		font-size: 18px;
		line-height: auto;
		font-weight: 900;
		color: #546e7a;
		margin-bottom: 18px;
	}
}
.section-welcome--text,
.section-about--text {
	text-align: justify;
	font-size: 14px;
	line-height: 24px;
	word-spacing: 6px;
}
.section-about {
	display: flex;
	flex-direction: row;
	margin: 0px 0px 102px 130px;

	&--text-container {
		margin-right: 39px;
		color: #546e7a;
		flex: 1;
	}
	&--text {
		margin: 0px 30px 34px 0px;
	}
	&--list-header {
		font-size: 14px;
		line-height: 26px;
		font-weight: 600;
		margin-bottom: 26px;
	}
	&--list {
		margin-bottom: 26px;
	}
	&--list-item {
		list-style: none;
		font-size: 14px;
		line-height: 26px;
		font-weight: 600;
	}
	&--list-item::before {
		content: url('../assets/svg/Rectangle.svg');
		width: 13px;
		height: 13px;
		margin-right: 20px;
	}
	&--end-text {
		font-size: 14px;
		line-height: 26px;
		text-align: left;
		font-weight: 600;
		word-spacing: 3px;
	}

	&--figure {
		width: calc(50vw - 54px);
		margin-top: 91px;
	}
	&--image {
		width: 100%;
		height: auto;
		flex-shrink: 1;
	}
}

@media (max-width: 1440px) {
	.section-welcome {
		display: block;
		margin-right: 80px;
		overflow: auto;
		&--figure {
			margin: 14px 54px 0px 0px;
			float: left;
		}

		&--text-container {
			margin-left: 130px;
			margin-bottom: 20px;
		}
	}
}

@media (max-width: 768px) {
	.title-image {
		width: 100%;
		margin: 0px 0px 24px 16px;
	}
	.section-welcome {
		display: flex;
		flex-direction: column-reverse;
		margin: 24px 0px 0px;
		&--text-container {
			margin: 0px 15px 20px;
		}
		&--figure {
			max-width: 100vw;
			margin: 14px 0px;
		}
	}

	.section-about {
		flex-direction: column;
		margin: 0px 0px 60px 0px;

		&--text-container {
			margin: 0px 15px;
		}
		&--text {
			margin: 0px 0px 34px 0px;
		}

		&--figure {
			width: 100vw;
			margin-top: 42px;
		}
	}
}
</style>
