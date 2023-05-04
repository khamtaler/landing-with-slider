<template>
	<div class="menu">
		<img class="menu--logo" src="../assets/images/LOGO-min_1.webp" alt="Logo" />
		<nav class="menu--navbar">
			<ul class="menu--navbar-list">
				<li class="menu--navbar-item">Startseite</li>
				<li class="menu--navbar-item active">Über uns</li>
				<li class="menu--navbar-item">Kontakt</li>
			</ul>
		</nav>
		<img
			class="menu--mobile-open"
			src="../assets/svg/mobile-menu.svg"
			alt="mobile menu button"
			@click="toggleMobile()"
		/>
		<img
			class="menu--mobile-close"
			src="../assets/svg/closeX.svg"
			alt="mobile menu button"
			@click="toggleMobile()"
		/>
	</div>
</template>

<script setup>
function toggleMobile() {
	document.querySelector('.menu').classList.toggle('mobile');
	document.querySelector('body').classList.toggle('fixed');
}
</script>

<style lang="scss" scoped>
.menu {
	display: flex;
	flex-direction: row;
	align-items: center;
	justify-content: space-between;
	box-shadow: 0px 6px 6px -6px rgba(0, 0, 0, 0.7);
	padding: 28px 130px;
	&--logo {
		height: 48px;
		width: auto;
	}
	&--navbar-list {
		display: flex;
		flex-direction: row;
		gap: 24px;
	}
	&--navbar-item {
		list-style: none;
		font-weight: 700;
		font-size: 24px;
		color: rgba(0, 0, 0, 0.7);
		&.active {
			color: #000;
			text-decoration: underline;
		}
	}
	&--mobile-open {
		display: none;
	}
	&--mobile-close {
		display: none;
	}
}
@media (max-width: 900px) {
	.menu {
		padding: 28px 50px;
	}
}
@media (max-width: 768px) {
	.menu--navbar {
		display: none;
	}
	.menu--mobile-open {
		display: block;
		position: absolute;
		right: 44px;
	}
	.menu--mobile-close {
		position: absolute;
		right: 44px;
		width: 24px;
	}
	.menu.mobile {
		position: absolute;
		top: 0;
		left: 0;
		width: 100vw;
		height: 100vh;
		background: #fff;
	}
	.menu {
		align-items: center;
		padding: 28px 20px;
		&--logo {
			height: 36px;
		}
	}
	.mobile {
		&.menu {
			align-items: baseline;
		}
		.menu--navbar {
			display: flex;

			position: absolute;
			top: 50%;
			left: 50%;
			transform: translate(-50%, -50%);
		}
		.menu--navbar-list {
			flex-direction: column;
			text-align: center;
		}
		.menu--mobile-open {
			display: none;
		}
		.menu--mobile-close {
			display: block;
		}
	}
}
</style>
