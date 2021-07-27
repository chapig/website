<script>
	import { Router, Route } from "svelte-navigator";
	import Header from "./components/Header.svelte";
	import Footer from "./components/Footer.svelte";
	import TutoringAd from "./components/TutoringAd.svelte";
	import Hero from "./components/Hero.svelte";
	import Project from "./components/Project/Project.svelte";
	import Services from "./components/Services.svelte";
	import Contact from "./components/Contact.svelte";
	import { fly, fade } from 'svelte/transition';
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
			<div in:fly>
				<Hero />
				<TutoringAd />
			</div>
		</Route>

		<Route path="projects">
			<div in:fly>
					<h1 class="pt-16 mb-4 text-4xl font-extrabold leading-none tracking-normal text-gray-900 md:text-6xl md:tracking-tight text-center">
						<span>Estos son mis</span>  <span class="lg:block md:block w-full py-2 text-transparent bg-clip-text leading-12 bg-gradient-to-r from-yellow-600 to-yellow-900">proyectos.</span>
					</h1>

					<section class="py-6 lg:py-12 lg:flex lg:justify-center">
						<Project
							backgroundcolor = "bg-gray-100"
							title="Alfonso"
							titlecolor = "text-black"
							subtitle="Bot para Discord"
							subtitlecolor = "text-gray-900"
							tag="Python"
							tagcolor = "bg-yellow-300"
							tagtextcolor = "text-black"
							description="Bot usando la API de Discord escrita en Python, soporta distintos prefijos para
							cada servidor en que el bot se encuentre, reproducción de música, calculadora
							de matemáticas, precio de monedas fiat y criptomonedas, búsqueda en
							Wikipedia, juegos y comandos de ocio."
							descriptioncolor = "text-black"
							github = "https://www.github.com/chapig/alfonso"
							githubcolor = "text-black"
						/>

						<Project
							backgroundcolor = "bg-gray-100"
							title="Base de datos para tutoría"
							titlecolor = "text-black"
							subtitle="Puente de bases de datos"
							subtitlecolor = "text-gray-900"
							tag="Python & SQLite"
							tagcolor = "bg-gradient-to-r from-yellow-300 to-blue-500"
							tagtextcolor = "text-black"
							description="Puente para controlar datos de la base de datos, que contiene fecha de pago, monto, deuda, código de estudiante, nacionalidad y país de residencia."
							descriptioncolor = "text-black"
							github = "https://www.github.com/chapig/tutoringdb"
							githubcolor = "text-black"
						/>

						<Project
						backgroundcolor = "bg-gray-100"
						title="Mathenize"
						titlecolor = "text-black"
						subtitle="Parser de operaciones matemáticas"
						subtitlecolor = "text-gray-900"
						tag="Julia"
						tagcolor = "bg-pink-500"
						tagtextcolor = "text-white"
						description="Realiza operaciones matemáticas desde strings usando el lenguaje de
						programación Julia, la mayoría de las funciones matemáticas y expresiones son
						compatibles, incluyendo matrices y operaciones con paréntesis."
						descriptioncolor = "text-black"
						github = "https://www.github.com/chapig/mathenizejl"
						githubcolor = "text-black"
						/>

						<Project
							backgroundcolor = "bg-gray-100"
							title="chapig.com"
							titlecolor = "text-black"
							subtitle="Sitio web"
							subtitlecolor = "text-gray-900"
							tag="Svelte"
							tagcolor = "bg-red-700"
							tagtextcolor = "text-white"
							description="Sitio web que muestra el currículum de Luis C. Gómez, sus servicios y proyectos."
							descriptioncolor = "text-black"
							github = "https://www.github.com/chapig/website"
							githubcolor = "text-black"
						/>
					</section>
				</div>
		</Route>

		<Route path="services">
			<div in:fly>
				<Services />
			</div>
		</Route>

		<Route path="contact">
			<div in:fly>
				<Contact />
			</div>
		</Route>

		<Footer />

	</main>
	
</Router>
