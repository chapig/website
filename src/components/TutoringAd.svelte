<script>
    import { Link } from "svelte-navigator";
    let classinfo = 'Imparto clases personalizadas de francés e inglés de <span class="font-bold">lunes a viernes</span> a través de internet.'
    let projectideas = 'Échale un vistazo a mis proyectos de software e ideas que planeo realizar en un futuro cercano.'
</script>

<section class="lg:py-12 lg:flex lg:justify-center bg-transparent">
    <div class="bg-white lg:bg-gray-200 md:bg-gray-200 dark:bg-gray-800 lg:mx-8 lg:flex lg:max-w-5xl lg:shadow-lg lg:rounded-lg">
        <div class="lg:w-1/2">
            <div class="h-64 bg-cover lg:rounded-lg lg:h-full" style="background-image:url('education.svg')" ></div>
        </div>

        <div class="max-w-xl px-6 py-12 lg:max-w-5xl lg:w-1/2">
            <p class="text-2xl font-bold text-black dark:text-white md:text-3xl">Inscríbete en mis clases privadas de francés o inglés</p>
            <p class="mt-4 text-black dark:text-gray-400"> {@html classinfo} </p>
            <div class="mt-8">
                <button class="px-5 py-2 text-md text-black transition-colors duration-200 transform bg-yellow-400 rounded-md hover:bg-gray-800 hover:text-white hover:font-medium">Inscríbete</button>
            </div>
        </div>
    </div>

    <div class="bg-yellow-400 dark:bg-gray-800 lg:mx-8 lg:flex lg:max-w-5xl lg:shadow-lg lg:rounded-lg">
        <div class="lg:w-1/2">
            <div class="h-64 bg-cover lg:rounded-lg lg:h-full" style="background-image:url('panadocument.svg')" ></div>
        </div>

        <div class="max-w-xl px-6 py-12 lg:max-w-5xl lg:w-1/2">
            <p class="text-2xl font-bold text-black dark:text-white md:text-3xl">Conoce mis proyectos de software y otras ideas</p>
            <p class="mt-4 text-gray-900 dark:text-gray-400 font-bold"> {@html projectideas} </p>
            <div class="mt-8">
                <Link to="projects" class="px-5 py-2 text-md text-black transition-colors duration-200 transform bg-white rounded-md hover:bg-gray-800 hover:text-white hover:font-medium">Proyectos</Link>
            </div>
        </div>
    </div>
</section>
