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
    <a href="https://wa.me/5511937324144"><Icon icon="logos:whatsapp-icon" class="text-[24px]" /></a>
</aside>

<main class="bg-zinc-900 min-h-screen text-zinc-300">
    <section id="investigacao-conjugal" class="flex justify-center space-y-10 text-center">
        <div class="flex bg-[url('/mobile-header-bg.jpg')] md:bg-[url('/desktop-header-bg.jpg')] bg-cover w-full h-[500px]">
            
            <div class="m-auto text-center border border-white p-4 backdrop-brightness-50 scale-75 lg:scale-100">
                <h1 in:fade="{{ duration: 1000 }}" class="text-5xl font-bold mb-4 text-blue-400">Descubra a Verdade</h1>
                <p in:fade="{{ duration: 1000, delay: 500 }}" class="text-xl mb-8 font-semibold">Serviços profissionais de investigação para casos pessoais e empresariais</p>
                <a href="#contato" in:fade="{{ duration: 1000, delay: 1000 }}" class="bg-blue-600 text-white px-6 py-3 rounded-full hover:bg-blue-500 transition duration-300 inline-block font-semibold">
                    Fale Conosco
                </a>
            </div>

        </div>
    </section>

    <section id="servicos" class="bg-zinc-800 py-16">
        <div class="flex flex-col container mx-auto px-4">
            <h2 class="text-3xl font-bold mb-12 text-center text-blue-400">Nossos Serviços</h2>
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
                {#if visible}
                <div in:fly="{{ y: 50, duration: 1000, delay: 200 }}" class="bg-zinc-700 p-6 rounded-lg shadow-lg">
                    <h3 class="text-xl font-bold mb-4 text-blue-300">Investigação Conjugal</h3>
                    <p>Investigações discretas e minuciosas para descobrir infidelidades e proteger seus interesses pessoais.</p>
                </div>
                <div in:fly="{{ y: 50, duration: 1000, delay: 400 }}" class="bg-zinc-700 p-6 rounded-lg shadow-lg">
                    <h3 class="text-xl font-bold mb-4 text-blue-300">Espionagem Corporativa</h3>
                    <p>Proteja sua empresa de ameaças internas e externas com nossos serviços especializados de investigação empresarial.</p>
                </div>
                <div in:fly="{{ y: 50, duration: 1000, delay: 600 }}" class="bg-zinc-700 p-6 rounded-lg shadow-lg">
                    <h3 class="text-xl font-bold mb-4 text-blue-300">Verificação de Antecedentes</h3>
                    <p>Investigações completas de antecedentes para fins pessoais ou profissionais, garantindo sua segurança e tranquilidade.</p>
                </div>
                {/if}
            </div>
            <a href="/serviços" in:fade="{{ duration: 1000, delay: 1000 }}" class="bg-blue-600 text-white px-6 py-3 rounded-full hover:bg-blue-500 transition duration-300 inline-block font-semibold mt-10 mx-auto">
                Ver Mais
            </a>
        </div>
    </section>

    <section id="sobre" class="py-16">
        <div class="container mx-auto px-4">
            <h2 class="text-3xl font-bold mb-8 text-center text-blue-400">Sobre Nós</h2>
            <div class="max-w-3xl mx-auto bg-zinc-800 p-8 rounded-lg shadow-lg">
                <p class="text-center mb-6">
                Com mais de 20 anos de experiência, a Fast Time é a agência de detetives de confiança para aqueles que buscam a verdade. 
                Nossa equipe de investigadores especializados utiliza tecnologia de ponta e métodos comprovados para entregar resultados.
                <br/><br/>
                Com equipamentos de última geração e uma equipe de detetive particular especializada, o trabalho da Fast Time é apresentar uma solução para
                o problema de seus clientes, por meio de provas reais (imagens, áudios e documentos) que comprovem ou não a suspeita, com total certeza e máximo
                sigilo. O detetive particular é responsável por atender os mais variados tipos de investigação existentes, encontrando resultados concretos e 
                atingindo os objetivos dos clientes.
                </p>
            </div>
        </div>

        <div class="grid grid-cols-1 md:grid-cols-2 gap-8 mx-auto max-w-[50%] mt-16 text-center">
            <div class="bg-zinc-700 p-6 rounded-lg shadow-lg">
                <Icon icon="fluent:people-team-28-regular" class="text-[32px] text-blue-600 mx-auto" />
                <p>Equipe altamente treinada e licenciada</p>
            </div>
            <div class="bg-zinc-700 p-6 rounded-lg shadow-lg">
                <Icon icon="lets-icons:eye-light" class="text-[32px] text-blue-600 mx-auto" />
                <p>Tecnologia de vigilância avançada</p>
            </div>
            <div class="bg-zinc-700 p-6 rounded-lg shadow-lg">
                <Icon icon="fluent-mdl2:security-group" class="text-[32px] text-blue-600 mx-auto" />
                <p>Confidencialidade garantida</p>
            </div>
            <div class="bg-zinc-700 p-6 rounded-lg shadow-lg">
                <Icon icon="mi:document" class="text-[32px] text-blue-600 mx-auto" />
                <p>Relatórios detalhados e evidências sólidas</p>
            </div>
        </div>
    </section>

    <section id="contato" class="bg-zinc-800 py-16">
        <div class="container mx-auto px-4">
            <h2 class="text-3xl font-bold mb-8 text-center text-blue-400">Entre em Contato</h2>
            <form class="max-w-md mx-auto bg-zinc-700 p-8 rounded-lg shadow-lg">
                <div class="mb-4">
                    <label for="nome" class="block mb-2 font-semibold">Nome</label>
                    <input type="text" id="nome" class="w-full p-2 bg-zinc-600 rounded border border-zinc-500 focus:border-blue-500 focus:outline-none" required>
                </div>
                <div class="mb-4">
                    <label for="email" class="block mb-2 font-semibold">E-mail</label>
                    <input type="email" id="email" class="w-full p-2 bg-zinc-600 rounded border border-zinc-500 focus:border-blue-500 focus:outline-none" required>
                </div>
                <div class="mb-4">
                    <label for="mensagem" class="block mb-2 font-semibold">Mensagem</label>
                    <textarea id="mensagem" rows="4" class="w-full p-2 bg-zinc-600 rounded border border-zinc-500 focus:border-blue-500 focus:outline-none" required></textarea>
                </div>
                <button type="submit" class="bg-blue-600 text-white px-6 py-3 rounded-full hover:bg-blue-500 transition duration-300 w-full font-semibold">Enviar Mensagem</button>
            </form>
        </div>
    </section>
</main>