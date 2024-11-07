<script>
    import { onMount } from 'svelte';
    import { fade, fly } from 'svelte/transition';
    import Icon from '@iconify/svelte';
  
    let visible = false;
  
    onMount(() => {
      visible = true;
    });
</script>

<aside class="fixed z-10 m-auto left-[90%] lg:left-[95%] top-[80%] bg-white rounded-xl p-3">
    <a href="#contato"><Icon icon="logos:whatsapp-icon" class="text-[24px]" /></a>
</aside>

<main class="bg-zinc-900 min-h-screen text-zinc-300 font-sans">
    <nav class="container mx-auto p-4 flex justify-between items-center">
        <div class="text-2xl font-bold text-pink-500">Fast Time</div>
        <ul class="flex space-x-4">
        <li><a href="#servicos" class="hover:text-pink-400 transition duration-300">Serviços</a></li>
        <li><a href="#sobre" class="hover:text-pink-400 transition duration-300">Sobre</a></li>
        <li><a href="#contato" class="hover:text-pink-400 transition duration-300">Contato</a></li>
        </ul>
    </nav>

    <header class="flex mx-auto py-20 h-[500px] px-4 bg-[url('/mobile-header-bg.jpeg')] md:bg-[url('/desktop-header-bg.jpg')] bg-cover">
        {#if visible}
        <div class="m-auto text-center border border-white p-4 backdrop-brightness-75">
            <h1 in:fade="{{ duration: 1000 }}" class="text-5xl font-bold mb-4 text-pink-400">Descubra a Verdade</h1>
            <p in:fade="{{ duration: 1000, delay: 500 }}" class="text-xl mb-8 font-semibold">Serviços profissionais de investigação para casos pessoais e empresariais</p>
            <a href="#contato" in:fade="{{ duration: 1000, delay: 1000 }}" class="bg-pink-600 text-white px-6 py-3 rounded-full hover:bg-pink-500 transition duration-300 inline-block font-semibold">Fale Conosco</a>
        </div>
        {/if}
    </header>

    <section id="servicos" class="bg-zinc-800 py-16">
        <div class="container mx-auto px-4">
        <h2 class="text-3xl font-bold mb-12 text-center text-pink-400">Nossos Serviços</h2>
        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
            {#if visible}
            <div in:fly="{{ y: 50, duration: 1000, delay: 200 }}" class="bg-zinc-700 p-6 rounded-lg shadow-lg">
                <h3 class="text-xl font-bold mb-4 text-pink-300">Investigação Conjugal</h3>
                <p>Investigações discretas e minuciosas para descobrir infidelidades e proteger seus interesses pessoais.</p>
            </div>
            <div in:fly="{{ y: 50, duration: 1000, delay: 400 }}" class="bg-zinc-700 p-6 rounded-lg shadow-lg">
                <h3 class="text-xl font-bold mb-4 text-pink-300">Espionagem Corporativa</h3>
                <p>Proteja sua empresa de ameaças internas e externas com nossos serviços especializados de investigação empresarial.</p>
            </div>
            <div in:fly="{{ y: 50, duration: 1000, delay: 600 }}" class="bg-zinc-700 p-6 rounded-lg shadow-lg">
                <h3 class="text-xl font-bold mb-4 text-pink-300">Verificação de Antecedentes</h3>
                <p>Investigações completas de antecedentes para fins pessoais ou profissionais, garantindo sua segurança e tranquilidade.</p>
            </div>
            {/if}
        </div>
        </div>
    </section>

    <section id="sobre" class="py-16">
        <div class="container mx-auto px-4">
        <h2 class="text-3xl font-bold mb-8 text-center text-pink-400">Sobre Nós</h2>
        <div class="max-w-3xl mx-auto bg-zinc-800 p-8 rounded-lg shadow-lg">
            <p class="text-center mb-6">
            Com mais de 20 anos de experiência, a Fast Time é a agência de detetives de confiança para aqueles que buscam a verdade. Nossa equipe de investigadores especializados utiliza tecnologia de ponta e métodos comprovados para entregar resultados.
            </p>
            <ul class="list-disc list-inside space-y-2">
            <li>Equipe altamente treinada e licenciada</li>
            <li>Tecnologia de vigilância avançada</li>
            <li>Confidencialidade garantida</li>
            <li>Relatórios detalhados e evidências sólidas</li>
            </ul>
        </div>
        </div>
    </section>

    <section id="contato" class="bg-zinc-800 py-16">
        <div class="container mx-auto px-4">
        <h2 class="text-3xl font-bold mb-8 text-center text-pink-400">Entre em Contato</h2>
        <form class="max-w-md mx-auto bg-zinc-700 p-8 rounded-lg shadow-lg">
            <div class="mb-4">
            <label for="nome" class="block mb-2 font-semibold">Nome</label>
            <input type="text" id="nome" class="w-full p-2 bg-zinc-600 rounded border border-zinc-500 focus:border-pink-500 focus:outline-none" required>
            </div>
            <div class="mb-4">
            <label for="email" class="block mb-2 font-semibold">E-mail</label>
            <input type="email" id="email" class="w-full p-2 bg-zinc-600 rounded border border-zinc-500 focus:border-pink-500 focus:outline-none" required>
            </div>
            <div class="mb-4">
            <label for="mensagem" class="block mb-2 font-semibold">Mensagem</label>
            <textarea id="mensagem" rows="4" class="w-full p-2 bg-zinc-600 rounded border border-zinc-500 focus:border-pink-500 focus:outline-none" required></textarea>
            </div>
            <button type="submit" class="bg-pink-600 text-white px-6 py-3 rounded-full hover:bg-pink-500 transition duration-300 w-full font-semibold">Enviar Mensagem</button>
        </form>
        </div>
    </section>

    <footer class="bg-zinc-900 py-8 text-center">
        <p>&copy; 2023 Sombra Investigações. Todos os direitos reservados.</p>
    </footer>
</main>

<style>
:global(body) {
    margin: 0;
    font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', 'Roboto', 'Oxygen',
    'Ubuntu', 'Cantarell', 'Fira Sans', 'Droid Sans', 'Helvetica Neue',
    sans-serif;
}

:global(html) {
    scroll-behavior: smooth;
}
</style>