<script>
    import { Link } from "svelte-navigator";
    import { scale } from 'svelte/transition';
    let cv = {open: false};

    function toggle() {
        cv.open = !cv.open;
    };

</script>
<section class="pt-28 lg:pt-24">
    <div class="px-12 mx-auto max-w-7xl">
        <div class="w-full mx-auto text-left md:w-11/12 xl:w-9/12 md:text-center">
            <p class="mb-8 text-4xl font-bold leading-none tracking-normal text-gray-900 md:text-6xl md:tracking-tight">
                <span>Bienvenid@, soy</span>  <span class="lg:block md:block w-full py-2 text-transparent bg-clip-text leading-12 bg-gradient-to-r from-yellow-600 to-yellow-900">Luis C. Gómez</span>
            </p>

                <div class="px-0 mb-8 text-lg text-gray-600 md:text-xl lg:px-24">
                    <div class="gap-6 md:grid-cols-2 lg:grid-cols-3">
                        <div>
                            <img src="lcgomez.jpg" class="w-36 h-36 rounded-full inline" alt="Luis C. Gomez face"/> 
                            <p class="mt-2 text-black font-medium dark:text-gray-400">Soy <span class="font-semibold">programador</span>, políglota y <span class="font-semibold">TSU en idiomas mención inglés.</span> Me encanta la informática, jugar videojuegos y cantar. Conoce un poco de mis servicios, proyectos y más!</p>
                        </div>
                    </div>
                </div>

            <div class="space-x-0 md:space-x-2 md:mb-8">
                <button on:click={toggle} class="inline-flex items-center justify-center w-full px-6 py-3 mb-2 text-lg text-black bg-yellow-400 rounded-md sm:w-auto sm:mb-0 hover:bg-gray-800 hover:text-white transition duration-200">
                    Currículum
                    <svg class="w-4 h-4 ml-1" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20" fill="currentColor"><path fill-rule="evenodd" d="M10.293 3.293a1 1 0 011.414 0l6 6a1 1 0 010 1.414l-6 6a1 1 0 01-1.414-1.414L14.586 11H3a1 1 0 110-2h11.586l-4.293-4.293a1 1 0 010-1.414z" clip-rule="evenodd"></path></svg>
                </button>
                <Link to="contact" class="inline-flex items-center justify-center w-full px-6 py-3 mb-2 text-lg bg-gray-200 rounded-md sm:w-auto sm:mb-0 hover:bg-gray-800 hover:text-white transition duration-200">
                    Contáctame
                    <svg class="w-4 h-4 ml-1" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9.663 17h4.673M12 3v1m6.364 1.636l-.707.707M21 12h-1M4 12H3m3.343-5.657l-.707-.707m2.828 9.9a5 5 0 117.072 0l-.548.547A3.374 3.374 0 0014 18.469V19a2 2 0 11-4 0v-.531c0-.895-.356-1.754-.988-2.386l-.548-.547z"></path></svg>
                </Link>
                {#if cv.open}
                <div class="pt-2 lg:pt-6 md:pt-6" in:scale>
                    <div class="mb-1">
                      <a href="lchaparroresume.pdf" rel="noopener noreferrer" target="_blank" class="bg-gray-200 w-full flex items-center px-2 py-2 text-gray-800 hover:bg-blue-400  rounded-md hover:text-white transition-colors duration-200">
                          <span class="mx-2 text-sm">Abrir</span>
                      </a>
                    </div>
                    <div class="mb-1 ">
                      <a href="lchaparroresume.pdf"  class="bg-gray-200 w-full flex items-center px-2 py-2 text-gray-800 rounded-md hover:bg-blue-400 hover:text-white transition-colors duration-200" download>
                          <div class="block text-blue-600 ">
                            <span class="mx-2 text-sm text-gray-800 ">Descargar</span>
                            <svg xmlns="http://www.w3.org/2000/svg" class="h-4 w-4 inline" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 10v6m0 0l-3-3m3 3l3-3m2 8H7a2 2 0 01-2-2V5a2 2 0 012-2h5.586a1 1 0 01.707.293l5.414 5.414a1 1 0 01.293.707V19a2 2 0 01-2 2z" />
                            </svg>
                            <span class="text-xs font-bold ">PDF</span> <span class="text-xs text-black">65 kB</span>
                          </div>
                      </a>
                    </div> 
                  </div>             
                {/if}
            </div>
        </div>
    </div>
</section>
