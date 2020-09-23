<template>
	<div class="news">
		<img class="news__image" :src="require('@/assets/images/news/'+news.img)" alt="img" />
		<div class="news__content">
			<div class="news__subtitle">
				<p class="news__manufacturer">Abat</p>
				<p class="news__date">{{news.date}}</p>
			</div>
			<p class="news__title">{{news.title}}</p>
			<p class="news__description">{{news.description}}</p>
		</div>
	</div>
</template>

<script>
export default {
	props: {
		news: {
			title: String,
			img: String,
			date: String,
			description: String,
		},
	},
};
</script>

<style lang="scss" scoped>
.news {
	&__manufacturer {
		color: #00aa4b;
	}
}
</style>