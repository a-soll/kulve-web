<script lang="ts">
	let { children } = $props();
	import '../app.css';
	import * as Breadcrumb from "$lib/components/ui/breadcrumb/index.js";
</script>

<div class="nav">
<Breadcrumb.Root>
  <Breadcrumb.List>
    <Breadcrumb.Item>
      <Breadcrumb.Link href="/">Home</Breadcrumb.Link>
    </Breadcrumb.Item>
    <Breadcrumb.Separator />
    <Breadcrumb.Item>
      <Breadcrumb.Link href="/privacy">Privacy</Breadcrumb.Link>
    </Breadcrumb.Item>
    <Breadcrumb.Separator />
  </Breadcrumb.List>
</Breadcrumb.Root>
</div>

{@render children()}

<style>
	:global(body) {
		background: #2f2f2f;
		color: #eeeeee;
		font-family:
			-apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans',
			'Helvetica Neue', sans-serif;
		margin: 0;
		padding: 0;
		line-height: 1.6;
	}

	/* Global Spacing */
	* {
		box-sizing: border-box;
	}

	/* Hero Section */
	:global(header) {
		text-align: center;
		padding: 40px 20px;
		background: linear-gradient(135deg, #4b0082, #6a5acd);
		color: #fff;
	}

	:global(header img) {
		display: block;
		margin: 0 auto 20px auto;
		width: 120px;
		border-radius: 15px;
		transition: transform 0.3s ease-in-out;
	}

	:global(header img:hover) {
		transform: scale(1.1);
	}

	:global(header h1) {
		font-size: 2.5rem;
		margin: 10px 0;
		font-weight: 600;
		text-shadow: 0 2px 5px rgba(0, 0, 0, 0.3);
	}

	:global(header p) {
		margin: 10px auto;
		max-width: 600px;
		font-size: 1.1rem;
		font-weight: 300;
		line-height: 1.8;
	}

	:global(main) {
		padding: 40px 20px;
	}

	:global(section) {
		max-width: 1100px;
		margin: 0 auto;
		margin-bottom: 60px;
	}

	:global(section h2) {
		font-size: 2rem;
		text-align: center;
		margin-bottom: 20px;
		color: #fff;
		text-shadow: 0 2px 5px rgba(0, 0, 0, 0.3);
		animation: fadeIn 1s ease-in-out;
	}
	.nav {
		display: flex;
		justify-content: space-between;
		align-items: center;
		padding: 10px 20px;
		background-color: #333;
		color: #fff;
	}
	
</style>
