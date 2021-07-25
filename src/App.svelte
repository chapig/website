<script>
	import { Router, Route, Link } from "svelte-navigator";
	import Header from "./components/Header.svelte";
	import Footer from "./components/Footer.svelte";
	import TutoringAd from "./components/TutoringAd.svelte";
	import Projects from "./components/Project/Project.svelte";
	import Hero from "./components/Hero.svelte";
	import Project from "./components/Project/Project.svelte";
</script>

<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@400&display=swap" rel="stylesheet">

<style global>
	
	@tailwind base;
	@tailwind components;
	@tailwind utilities;

	:global(body) {
			
			/* this will apply to <body> */
			background-color: white;
			font-family: 'Inter', sans-serif;
		}
</style>
<Router>
	<header>
		<Header />
	</header>
	
	<main>
		
		<Route path="/">
			<Hero />
			<Project title="Hola" subtitle="Hola" github="a" tag="a" />
			<TutoringAd />
		</Route>

		<Route path="services">
			<Projects />
		</Route>

		<Route path="cv">
		</Route>

		<Route path="contact">
		</Route>

		<Footer />

	</main>
	
</Router>