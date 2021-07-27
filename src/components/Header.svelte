<script>
  import { Link } from "svelte-navigator";
	import { scale, fade } from 'svelte/transition';
	import { quintOut } from 'svelte/easing';
  let menu = { open: false };
  let cv = { open: false };
  let cvmob = { open: false };

  function toggle() {
    menu.open = !menu.open;
    cvmob.open = false;
  }

  function toggleCv() {
    cv.open = !cv.open;
  }

  function toggleCvMobile() {
    cvmob.open = !cvmob.open;
  }

  const chapigblacklogo = '<svg data-v-423bf9ae="" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 168.7815240958042 60" class="font"><!----><!----><!----><g data-v-423bf9ae="" id="b4aae73a-292e-42cc-ad53-12b36a3862ce" fill="black" transform="matrix(4.2016807508382215,0,0,4.2016807508382215,-1.7647057638803432,-7.0588237034820835)"><path d="M1.90 9.38C1.90 8.77 2.10 8.29 2.48 7.93C2.87 7.57 3.41 7.39 4.10 7.39C4.54 7.39 4.96 7.51 5.37 7.73C5.78 7.96 6.05 8.24 6.20 8.55L6.20 6.71C5.75 6.25 5.01 6.02 3.96 6.02C2.89 6.02 2.03 6.33 1.39 6.96C0.74 7.58 0.42 8.39 0.42 9.38C0.42 10.37 0.74 11.18 1.39 11.80C2.03 12.43 2.89 12.74 3.96 12.74C5.03 12.74 5.77 12.51 6.20 12.05L6.20 10.21C6.04 10.54 5.78 10.82 5.40 11.04C5.03 11.26 4.60 11.37 4.10 11.37C3.41 11.37 2.87 11.19 2.48 10.83C2.10 10.47 1.90 9.99 1.90 9.38ZM9.28 8.96C9.28 8.51 9.45 8.13 9.78 7.82C10.11 7.51 10.49 7.35 10.92 7.35C11.33 7.35 11.64 7.45 11.84 7.64C12.05 7.83 12.15 8.18 12.15 8.68L12.15 12.60L13.62 12.60L13.62 8.54C13.62 7.63 13.42 6.98 13.03 6.59C12.63 6.21 12.07 6.02 11.34 6.02C10.45 6.02 9.77 6.40 9.28 7.15L9.28 1.68L7.81 1.68L7.81 12.60L9.28 12.60ZM16.02 8.01C16.66 7.54 17.32 7.31 18.00 7.31C18.91 7.31 19.36 7.56 19.36 8.05L19.36 8.90C18.90 8.65 18.34 8.53 17.70 8.53C16.87 8.53 16.19 8.72 15.64 9.11C15.09 9.51 14.81 10.06 14.81 10.78C14.81 11.43 15.04 11.92 15.50 12.25C15.96 12.58 16.51 12.74 17.16 12.74C17.66 12.74 18.10 12.65 18.49 12.46C18.87 12.27 19.17 12.01 19.36 11.68L19.36 12.60L20.83 12.60L20.83 7.98C20.83 7.32 20.58 6.82 20.06 6.50C19.55 6.18 18.86 6.02 18.00 6.02C17.09 6.02 16.24 6.30 15.47 6.87ZM16.23 10.64C16.23 10.36 16.38 10.12 16.69 9.90C17.00 9.70 17.40 9.59 17.89 9.59C18.42 9.59 18.91 9.67 19.36 9.84L19.36 10.08C19.36 10.65 19.21 11.05 18.92 11.27C18.63 11.49 18.18 11.61 17.58 11.61C16.68 11.61 16.23 11.28 16.23 10.64ZM29.58 9.38C29.58 8.32 29.27 7.49 28.64 6.90C28.02 6.31 27.24 6.02 26.32 6.02C25.32 6.02 24.57 6.45 24.05 7.31L24.05 6.16L22.58 6.16L22.58 15.68L24.05 15.68L24.05 11.45C24.57 12.31 25.32 12.74 26.32 12.74C27.24 12.74 28.02 12.45 28.64 11.86C29.27 11.27 29.58 10.44 29.58 9.38ZM28.10 9.38C28.10 10.03 27.91 10.54 27.53 10.88C27.15 11.23 26.66 11.41 26.04 11.41C25.49 11.41 25.02 11.24 24.63 10.91C24.25 10.58 24.05 10.07 24.05 9.38C24.05 8.69 24.25 8.18 24.63 7.85C25.02 7.52 25.49 7.35 26.04 7.35C26.66 7.35 27.15 7.52 27.53 7.87C27.91 8.22 28.10 8.73 28.10 9.38ZM30.63 3.64C30.63 3.89 30.73 4.11 30.91 4.28C31.10 4.46 31.32 4.55 31.58 4.55C31.85 4.55 32.07 4.46 32.26 4.28C32.44 4.11 32.54 3.89 32.54 3.64C32.54 3.39 32.44 3.17 32.26 3.00C32.07 2.82 31.85 2.73 31.58 2.73C31.32 2.73 31.10 2.82 30.91 3.00C30.73 3.17 30.63 3.39 30.63 3.64ZM30.84 6.16L30.84 12.60L32.33 12.60L32.33 6.16ZM35.07 9.38C35.07 8.73 35.26 8.22 35.64 7.87C36.02 7.52 36.51 7.35 37.13 7.35C37.68 7.35 38.15 7.52 38.54 7.85C38.92 8.18 39.12 8.69 39.12 9.38C39.12 10.07 38.92 10.58 38.54 10.91C38.15 11.24 37.68 11.41 37.13 11.41C36.51 11.41 36.02 11.23 35.64 10.88C35.26 10.54 35.07 10.03 35.07 9.38ZM33.64 13.02C33.64 13.92 33.95 14.63 34.57 15.16C35.19 15.69 36.02 15.96 37.04 15.96C38.00 15.96 38.82 15.65 39.53 15.04C40.23 14.43 40.59 13.57 40.59 12.46L40.59 6.16L39.12 6.16L39.12 7.31C38.60 6.45 37.85 6.02 36.85 6.02C35.92 6.02 35.15 6.31 34.52 6.90C33.90 7.49 33.59 8.32 33.59 9.38C33.59 10.44 33.90 11.27 34.52 11.86C35.15 12.45 35.92 12.74 36.85 12.74C37.85 12.74 38.60 12.31 39.12 11.45L39.12 12.46C39.12 13.15 38.91 13.67 38.49 14.03C38.08 14.38 37.59 14.56 37.04 14.56C36.45 14.56 35.98 14.41 35.64 14.11C35.30 13.80 35.13 13.44 35.13 13.02Z"></path></g><!----><!----></svg>'
</script>

<nav class="fixed w-full md:relative z-50 lg:relative px-4 py-4 flex justify-between items-center">
  <Link to="/" class="text-3xl font-bold leading-none">
    <svg class="h-16" alt="logo" viewBox="0 0 10240 10240">
      {@html chapigblacklogo}
    </Link>

  <div class="lg:hidden md:hidden">
    <button on:click={toggle} class="navbar-burger flex items-center text-black  p-3">
      <svg class="block h-5 w-5 fill-current" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg">
        <title>Mobile menu</title>
        <path d="M0 3h20v2H0V3zm0 6h20v2H0V9zm0 6h20v2H0v-2z"></path>
      </svg>
    </button>
  </div>
  <div class="hidden lg:items-center md:flex lg:flex">
  <ul class="flex flex-col md:flex-row md:mx-6 bg-gray-100 rounded-md">
    <li>
      <Link to="/" class="flex items-center px-4 py-4 rounded hover:bg-gray-200 transition-colors duration-200">
        <svg xmlns="http://www.w3.org/2000/svg" class="h-4 w-4" viewBox="0 0 20 20" fill="currentColor">
          <path d="M10.707 2.293a1 1 0 00-1.414 0l-7 7a1 1 0 001.414 1.414L4 10.414V17a1 1 0 001 1h2a1 1 0 001-1v-2a1 1 0 011-1h2a1 1 0 011 1v2a1 1 0 001 1h2a1 1 0 001-1v-6.586l.293.293a1 1 0 001.414-1.414l-7-7z" />
        </svg>
        <span class="mx-2 font-medium">Inicio</span>
      </Link>
      </li>

    <li>
      <Link to="projects" class="flex items-center px-4 py-4 rounded hover:bg-gray-200 transition-colors duration-200">
        <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5" viewBox="0 0 20 20" fill="currentColor">
          <path fill-rule="evenodd" d="M2 5a2 2 0 012-2h12a2 2 0 012 2v10a2 2 0 01-2 2H4a2 2 0 01-2-2V5zm3.293 1.293a1 1 0 011.414 0l3 3a1 1 0 010 1.414l-3 3a1 1 0 01-1.414-1.414L7.586 10 5.293 7.707a1 1 0 010-1.414zM11 12a1 1 0 100 2h3a1 1 0 100-2h-3z" clip-rule="evenodd" />
        </svg>
        <span class="mx-2 font-medium">Proyectos</span>
      </Link>
    </li>
    <li>
      <Link to="services" class="flex items-center px-4 py-4 rounded hover:bg-gray-200 transition-colors duration-200">
        <svg xmlns="http://www.w3.org/2000/svg" class="h-4 w-4" viewBox="0 0 20 20" fill="currentColor">
          <path d="M7 3a1 1 0 000 2h6a1 1 0 100-2H7zM4 7a1 1 0 011-1h10a1 1 0 110 2H5a1 1 0 01-1-1zM2 11a2 2 0 012-2h12a2 2 0 012 2v4a2 2 0 01-2 2H4a2 2 0 01-2-2v-4z" />
        </svg>
        <span class="mx-2 font-medium">Servicios</span>
      </Link>
    </li>
    <li>
      <button on:click={toggleCv} class="flex items-center px-4 py-4 rounded-r-md bg-gray-100 hover:bg-yellow-400 transition-colors duration-200">
          <span class="mx-2 font-medium">Currículum</span>
          <svg xmlns="http://www.w3.org/2000/svg" class="h-4 w-4" viewBox="0 0 20 20" fill="currentColor">
            <path fill-rule="evenodd" d="M15.707 4.293a1 1 0 010 1.414l-5 5a1 1 0 01-1.414 0l-5-5a1 1 0 011.414-1.414L10 8.586l4.293-4.293a1 1 0 011.414 0zm0 6a1 1 0 010 1.414l-5 5a1 1 0 01-1.414 0l-5-5a1 1 0 111.414-1.414L10 14.586l4.293-4.293a1 1 0 011.414 0z" clip-rule="evenodd" />
          </svg>
      </button>

      {#if cv.open}
      <div class="absolute z-20 w-48 py-2 mt-2 -ml-12 bg-gray-100 rounded-md shadow-xl dark:bg-gray-800" transition:scale="{{duration: 200, opacity: 0.5, start: 0.5, easing: quintOut}}">
        <a href="lchaparroresume.pdf" class="block px-4 py-2 text-sm text-black transition-colors duration-200 transform dark:text-gray-300 hover:bg-blue-400 hover:text-white dark:hover:text-white" rel="noopener noreferrer" target="_blank">
            Ver en sitio web
        </a>
        <a href="lchaparroresume.pdf" class="block px-4 py-2 text-sm text-black transition-colors duration-200 transform dark:text-gray-300 hover:bg-blue-400 hover:text-white dark:hover:text-white" download>
            Descargar
            <div class="block text-blue-600">
            <svg xmlns="http://www.w3.org/2000/svg" class="h-4 w-4 inline" fill="none" viewBox="0 0 24 24" stroke="currentColor">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 10v6m0 0l-3-3m3 3l3-3m2 8H7a2 2 0 01-2-2V5a2 2 0 012-2h5.586a1 1 0 01.707.293l5.414 5.414a1 1 0 01.293.707V19a2 2 0 01-2 2z" />
            </svg>
            <span class="text-xs font-bold ">PDF</span> <span class="text-xs text-black">65 kB</span>
            </div>
        </a>
    </div>
    {/if}
    </li>
  </ul>
  </div>
</nav>


<!--Mobile menu-->
{#if menu.open}
<div class="navbar-menu relative z-50" transition:fade="{{delay: 100, duration: 200}}">
  <div class="navbar-backdrop fixed inset-0 bg-gray-900 opacity-25"></div>
  <nav class="fixed top-0 left-0 bottom-0 flex flex-col w-5/6 max-w-sm py-6 px-6 overflow-y-auto bg-yellow-400">
    <div class="flex items-center mb-8">
      <Link on:click={toggle} to="/" class="mr-auto text-3xl font-bold leading-none">
        <img src="black-chapig.svg" class="h-8 pt-2" alt="logo">
      </Link>
      <button on:click={toggle} class="navbar-close">
        <svg class="h-6 w-6 text-white cursor-pointer hover:text-gray-100" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12"></path>
        </svg>
      </button>
    </div>
    <div>
      <ul>
        <li class="mb-1">
          <Link to="projects" on:click={toggle} class="flex items-center px-4 py-2 text-gray-800 bg-gray-100 rounded-md hover:bg-white hover:text-black">
            <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5" viewBox="0 0 20 20" fill="currentColor">
              <path fill-rule="evenodd" d="M2 5a2 2 0 012-2h12a2 2 0 012 2v10a2 2 0 01-2 2H4a2 2 0 01-2-2V5zm3.293 1.293a1 1 0 011.414 0l3 3a1 1 0 010 1.414l-3 3a1 1 0 01-1.414-1.414L7.586 10 5.293 7.707a1 1 0 010-1.414zM11 12a1 1 0 100 2h3a1 1 0 100-2h-3z" clip-rule="evenodd" />
            </svg>
            <span class="mx-4 font-medium">Proyectos</span>
          </Link>
        </li>
        <li class="mb-1">
          <Link to="services" on:click={toggle} class="flex items-center px-4 py-2 text-gray-800 bg-gray-100 rounded-md hover:bg-white hover:text-black transition-colors duration-200">
            <svg xmlns="http://www.w3.org/2000/svg" class="h-4 w-4" viewBox="0 0 20 20" fill="currentColor">
              <path d="M7 3a1 1 0 000 2h6a1 1 0 100-2H7zM4 7a1 1 0 011-1h10a1 1 0 110 2H5a1 1 0 01-1-1zM2 11a2 2 0 012-2h12a2 2 0 012 2v4a2 2 0 01-2 2H4a2 2 0 01-2-2v-4z" />
            </svg>
              <span class="mx-4 font-medium">Servicios</span>
          </Link>
        </li>
        <li class="mb-1">
          <button on:click={toggleCvMobile} class="w-full flex items-center px-4 py-2 text-gray-800 bg-gray-100 rounded-md hover:bg-white hover:text-black transition-colors duration-200">
            <svg xmlns="http://www.w3.org/2000/svg" class="w-5 h-5 inline" fill="none" viewBox="0 0 24 24" stroke="currentColor">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M7 21h10a2 2 0 002-2V9.414a1 1 0 00-.293-.707l-5.414-5.414A1 1 0 0012.586 3H7a2 2 0 00-2 2v14a2 2 0 002 2z" />
            </svg>
              <span class="mx-4 font-medium">Currículum</span>
          </button>
        </li>
        {#if cvmob.open}
        <div transition:scale="{{duration: 200, opacity: 0.5, start: 0.5, easing: quintOut}}">
          <li class="mb-1">
            <a href="lchaparroresume.pdf" rel="noopener noreferrer" target="_blank" class="w-full flex items-center px-2 py-2 text-gray-800 bg-gray-100 rounded-md hover:bg-white hover:text-black transition-colors duration-200">
                <span class="mx-2 text-sm">Abrir</span>
            </a>
          </li>
          <li class="mb-1">
            <a href="lchaparroresume.pdf"  class="w-full flex items-center px-2 py-2 text-gray-800 bg-gray-100 rounded-md hover:bg-white hover:text-black transition-colors duration-200" download>
                <div class="block text-blue-600">
                  <span class="mx-2 text-sm text-gray-800">Descargar</span>
                  <svg xmlns="http://www.w3.org/2000/svg" class="h-4 w-4 inline" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 10v6m0 0l-3-3m3 3l3-3m2 8H7a2 2 0 01-2-2V5a2 2 0 012-2h5.586a1 1 0 01.707.293l5.414 5.414a1 1 0 01.293.707V19a2 2 0 01-2 2z" />
                  </svg>
                  <span class="text-xs font-bold ">PDF</span> <span class="text-xs text-black">65 kB</span>
                </div>
            </a>
          </li> 
        </div>             
        {/if}
      </ul>
    </div>
    <div class="mt-auto">
      <div class="pt-6">
        <Link to="contact" class="block px-4 py-3 mb-2 leading-loose text-sm text-center text-black">Contáctame</Link>
      </div>
      <p class="my-4 text-xs text-center text-black">
        <span>Luis Alfredo Chaparro Gómez © Copyright 2021. Todos los derechos reservados</span>
      </p>
    </div>
  </nav>
</div>
{/if}
