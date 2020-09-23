<template>
	<header class="header">
		<div class="header__nav nav block">
			<nav>
				<ul>
					<li v-for="link in navLinks" :key="link.name">
						<img v-if="link.icon" :src="require('@/assets/icons/' + link.icon)" />
						<p>{{ link.name }}</p>
					</li>
				</ul>
			</nav>
		</div>
		<div class="header__panel panel block">
			<div class="panel__title">
				<img src="@/assets/images/logo.png" alt="logo" />
				<p>Столовая.</p>
				<strong>ру</strong>
			</div>
			<div class="panel__search">
				<div class="filter">Все</div>
				<input type="text" />
				<button>search</button>
			</div>
		</div>
		<div class="header__categories block">
			<div v-for="category in categories" :key="category.name">
				<img src :alt="category.name" />
				<p>{{ category.name }}</p>
			</div>
		</div>
	</header>
</template>

<script>
export default {
	name: "Header",
	data() {
		return {
			navLinks: [
				{ name: "Компания" },
				{ name: "Портфолио" },
				{ name: "Проектирование" },
				{ name: "Ресторанам" },
				{ name: "Застройщикам" },
				{ name: "Гос.заказчикам" },
				{ name: "Таблет-питание" },
				{ name: "Сервис" },
				{ name: "Контакты" },
				{ name: "info@stolovay.ru", icon: "email-icon.png" },
				{ name: "8 495 790-72-05", icon: "phone-icon.png" },
			],
			categories: [
				{ name: "Тепловое" },
				{ name: "Холодильное" },
				{ name: "Электромеханическое" },
				{ name: "Посудомоечное" },
				{ name: "Хлебопекарное" },
				{ name: "Линии раздачи" },
				{ name: "Нейтральное" },
				{ name: "Для фаст фуда" },
				{ name: "Для залов" },
				{ name: "Вспомогательное" },
				{ name: "Для магазинов" },
			],
		};
	},
};
</script>

<style lang="scss">
.header {
	&__categories {
		display: flex;
		justify-content: space-between;
		flex-wrap: wrap;
		background-color: #fff;
		box-shadow: 4px 6px 18px rgba(0, 0, 0, 0.11);
	}
}

.nav {
	background-color: #00aa4b;
	color: #fff;
	font-size: 16px;

	ul {
		margin: 0;
		padding: 0;
		list-style: none;
		display: flex;
		justify-content: space-between;

		li {
			display: flex;
			align-items: center;

			img {
				padding-right: 5px;
			}
		}
	}
}

.panel {
	display: flex;
	justify-content: space-between;
	background-color: #e8e7e7;
	flex-wrap: wrap;

	&__title {
		display: flex;
		justify-content: center;
		align-items: center;
		font-size: 33px;
		color: #171717;

		img {
			padding-right: 10px;
			padding-bottom: 10px;
		}

		strong {
			color: #121212;
			text-transform: uppercase;
			font-weight: normal;
			padding-left: 0;
		}
	}

	&__search {
		display: flex;
		align-items: center;
	}
}
</style>
