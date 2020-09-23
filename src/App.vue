<template>
	<div id="app">
		<Header />
		<NewsSection />
	</div>
</template>

<script>
import Header from "./components/Header";
import NewsSection from "./components/NewsSection";

export default {
	name: "App",
	components: {
		Header,
		NewsSection,
	},
};
</script>

<style lang="scss">
@import "./scss/app";
</style>
