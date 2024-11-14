<script lang="ts">
	import { i18n } from "$lib/i18n";
	import { ParaglideJS } from "@inlang/paraglide-sveltekit";
	import { Sheet, SheetClose, SheetTrigger } from "$lib/components/ui/sheet";
	import Icon from "@iconify/svelte";
	import '../app.css';
    import SheetContent from "$lib/components/ui/sheet/sheet-content.svelte";

	let { children } = $props();
</script>

<ParaglideJS {i18n}>
	<nav class="w-full mx-auto py-4 px-10 flex justify-between items-center bg-zinc-900 text-zinc-300">
		<div class="flex items-center space-x-4 text-2xl font-bold text-blue-500">
			<img src="/logo.png" alt="" class="object-contain w-[64px] h-[64px]" />
			<a href="/">Fast Time<br/><p class="text-lg italic">Investigações</p></a>
		</div>
		<ul class="hidden lg:flex space-x-4">
			<li><a href="/serviços" class="hover:text-blue-400 transition duration-300">Serviços</a></li>
			<li class="border-x border-x-white px-4">
				<a href="/#sobre" class="hover:text-blue-400 transition duration-300">Sobre</a>
			</li>
			<li><a href="/contato" class="hover:text-blue-400 transition duration-300">Contato</a></li>
		</ul>
		<Sheet>
			<SheetTrigger class="lg:hidden">
				<Icon icon="ic:baseline-menu" class="text-[24px]" />
			</SheetTrigger>
			<SheetContent class="h-full border-l border-l-white bg-zinc-950 text-white">
				<ul class="flex flex-col space-y-4">
					<li>
						<SheetClose>
							<a href="/serviços" class="hover:text-blue-400 transition duration-300">Serviços</a>
						</SheetClose>
					</li>
					<li>
						<SheetClose>
							<a href="/#sobre" class="hover:text-blue-400 transition duration-300">Sobre</a>
						</SheetClose>
					</li>
					<li>
						<SheetClose>
							<a href="/contato" class="hover:text-blue-400 transition duration-300">Contato</a>
						</SheetClose>
					</li>
				</ul>
			</SheetContent>
		</Sheet>
	</nav>
	{@render children()}
	<footer class="bg-zinc-900 py-8 text-center text-white space-y-1">
        <p>&copy; 2024 Fast Time Investigações. Todos os direitos reservados.</p>
		<p>Email: <b>fasttimeparticular@gmail.com</b></p>
		<p>Telefone: <b>+55 (11) 93732-4144</b></p>
		<p>CNPJ: <b>53.166.267/0001-10</b></p>
    </footer>
</ParaglideJS>
