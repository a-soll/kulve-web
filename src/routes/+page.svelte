<script>
	import { Button } from '$lib/components/ui/button';
	import * as Accordion from '$lib/components/ui/accordion';
	import Autoplay from 'embla-carousel-autoplay';
	import * as Carousel from '$lib/components/ui/carousel/index.js';
	import CarouselContent from '$lib/components/ui/carousel/carousel-content.svelte';
	import CarouselItem from '$lib/components/ui/carousel/carousel-item.svelte';
</script>

<svelte:head>
	<meta charset="UTF-8" />
	<meta name="viewport" content="width=device-width, initial-scale=1.0" />
	<meta
		name="description"
		content="Kulve is a lightweight, fast, and feature-packed Twitch client for macOS users. Join the Kulve community today!"
	/>
	<meta
		name="keywords"
		content="Kulve, Twitch Client, macOS, 7TV, Twitch Emotes, Stream Chat, Customisable Twitch Player"
	/>
	<meta name="author" content="Kulve Team" />
	<meta name="robots" content="index, follow" />

	<title>Kulve - Lightweight Twitch Client for macOS</title>
	<link rel="shortcut icon" href="/src/img/Kulve_Icon_02-64.png" type="image/x-icon" />

	<!-- Open Graph Meta Tags -->
	<meta property="og:title" content="Kulve - Your New macOS Twitch Client" />
	<meta
		property="og:description"
		content="Lightweight, fast, and feature-packed Twitch client for macOS users. Join the Kulve community today!"
	/>
	<meta property="og:image" content="/src/img/Kulve_Icon_02-1024.png" />
	<meta property="og:url" content="https://kulve.org" />
	<meta property="og:type" content="website" />

	<!-- Twitter Card Meta Tags -->
	<meta name="twitter:card" content="summary_large_image" />
	<meta name="twitter:title" content="Kulve - Your New macOS Twitch Client" />
	<meta
		name="twitter:description"
		content="Lightweight, fast, and feature-packed Twitch client for macOS users. Join the Kulve community today!"
	/>
	<meta name="twitter:image" content="/src/img/Kulve_Icon_02-1024.png" />
</svelte:head>

<header>
	<img src="/src/img/Kulve_Icon_02-1024.png" width="120" alt="Kulve Logo" class="center" />
	<h1>Introducing Kulve, your new macOS Twitch client</h1>
	<p>Lightweight, fast, and feature-packed for Twitch users on macOS.</p>
	<p>
		<Button class="bg-indigo-500" href="https://discord.gg/55T4AKJKt3">Join the Discord</Button>
	</p>
</header>

<!-- Features Section -->
<main>
	<section>
		<h2>Features</h2>
		<div class="carousel"> 
		<Carousel.Root
		    plugins={[
				Autoplay({
					delay: 10000
				})
			]}
			opts={{
                align: "center",
                loop: true,
			}}
		>
			<CarouselContent>
				<CarouselItem>
				<div class="carousel-item-content">
					<img src="/src/img/7tv.png" alt="7TV Emotes Feature" class="feature-image" />
					<p class="justify-center">Bring your favourite 7TV emotes into your Twitch experience seamlessly.</p>
				</div>
				</CarouselItem>
				<CarouselItem>
				<div class="carousel-item-content">
					<img src="/src/img/chat.png" alt="Streamlined Chat Feature" class="feature-image" />
					<p>
						Enjoy a clean and responsive chat experience that makes connecting with your community
						effortless.
					</p>
				</div>
				</CarouselItem>
				<CarouselItem>
				<div class="carousel-item-content">
					<img src="/src/img/player.png" alt="Twitch Player Feature" class="feature-image" />
					<p>
						Optimised for macOS, the Kulve player delivers smooth performance with essential Twitch
						controls.
					</p>
				</div>
				</CarouselItem>
				<CarouselItem>
				<div class="carousel-item-content">
					<img src="/src/img/search.png" alt="Search Feature" class="feature-image" />
					<p>
						Find your favourite streams and channels quickly with Kulve’s advanced search
						capabilities.
					</p>
				</div>
				</CarouselItem>
			</CarouselContent>
		</Carousel.Root>
		</div>
	</section>

	<!-- FAQ Section -->
	<section>
		<h2>FAQs</h2>
		<div class="faq-section">
		<Accordion.Root>
			<Accordion.Item value="item-1">
				<Accordion.Trigger>What is Kulve?</Accordion.Trigger>
				<Accordion.Content>
					Kulve is a Twitch client designed for macOS users, offering a lightweight and feature-rich
					experience.
				</Accordion.Content>
			</Accordion.Item>
			<Accordion.Item value="item-2">
				<Accordion.Trigger>Is Kulve free to use?</Accordion.Trigger>
				<Accordion.Content>Yes, Kulve is completely free to download and use</Accordion.Content>
			</Accordion.Item>
			<Accordion.Item value="item-3">
				<Accordion.Trigger>How do I get started with Kulve?</Accordion.Trigger>
				<Accordion.Content>
					Simply download the app from our website and start enjoying a better Twitch experience on
					macOS!
				</Accordion.Content>
			</Accordion.Item>
			<Accordion.Item value="item-4">
				<Accordion.Trigger>Does Kulve support 7TV emotes?</Accordion.Trigger>
				<Accordion.Content>
					Yes! Kulve integrates 7TV emotes seamlessly into your Twitch chat experience
				</Accordion.Content>
			</Accordion.Item>
			<Accordion.Item value="item-5">
				<Accordion.Trigger>Where can I provide feedback or report issues?</Accordion.Trigger>
				<Accordion.Content>
					Join our <a href="https://discord.gg/55T4AKJKt3">Discord server</a> to connect with our community
					and share feedback.
				</Accordion.Content>
			</Accordion.Item>
		</Accordion.Root>
	</div>
	</section>
</main>

<footer>
	<Button class="bg-indigo-500" href="https://discord.gg/k8G2JbQKeR">Discord</Button>
	<Button class="bg-indigo-500" href="https://github.com/a-soll/a-soll.github.io">Github</Button>
	<p>Built with ❤️ for macOS users.</p>
</footer>

<style>
    .faq-section {
        justify-content: left;
    }
    
    .carousel-item-content {
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      text-align: center;
      max-width: 100%;
      margin: 0 auto;
    }
    
    .carousel {
      max-width: 80%;
      overflow: hidden;
      margin-left: auto;
      margin-right: auto;
    }
    
    .carousel p {
      max-width: 100%;
      box-sizing: border-box;
      justify-content: center;
      margin-left: auto;
      margin-right: auto;
    }
    
    .carousel img {
      width: auto;
      height: 500px;
      display: block;
      margin-left: auto;
      margin-right: auto;
      justify-content: center;
      size: 5px;
    }

    
	footer {
		background: #1e1e1e;
		padding: 20px 0;
		text-align: center;
		color: #ddd;
		font-size: 0.9rem;
		border-top: 5px solid #4b0082;
	}

	footer p {
		margin: 0;
	}
</style>
