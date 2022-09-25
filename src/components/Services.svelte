<script>
    import { Link } from "svelte-navigator";
</script>

<section class="lg:py-12 lg:flex lg:justify-center">
    <div class="bg-gradient-to-r from-white  to-yellow-100 lg:mx-8 lg:flex lg:max-w-5xl lg:shadow-lg lg:rounded-lg">
        <div class="lg:w-1/2">
            <div class="h-64 bg-cover lg:rounded-lg lg:h-full" style="background-image:url('https://images.unsplash.com/photo-1593642532400-2682810df593?ixlib=rb-1.2.1&ixid=MXwxMjA3fDF8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&auto=format&fit=crop&w=750&q=80')"></div>
        </div>

        <div class="max-w-xl px-6 py-12 lg:max-w-5xl lg:w-1/2">
            <h2 class="text-2xl font-bold text-gray-800 dark:text-white md:text-3xl">Moderniza tu empresa</h2>
            <p class="mt-4 text-black">Ofrezco servicios de diseño gráfico para redes sociales, creación de sitios web, programas y asesorado para la modernización de tu empresa.</p>
            
            <div class="mt-8">
                <Link to="/contact" class="px-5 py-2 text-black transition-colors duration-200 transform bg-yellow-400 rounded-md hover:bg-gray-900 hover:text-white">Contacto</Link>
            </div>
        </div>
    </div>
</section> 
