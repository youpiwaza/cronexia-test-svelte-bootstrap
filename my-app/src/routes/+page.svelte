<script lang="ts">
	import Counter from './Counter.svelte';
	import welcome from '$lib/images/svelte-welcome.webp';
	import welcomeFallback from '$lib/images/svelte-welcome.png';

	// Bootstrap
	import { Styles } from '@sveltestrap/sveltestrap';

	// Bootstrap test
	import { Button, Col, Row } from '@sveltestrap/sveltestrap';

	import { ListGroup, ListGroupItem } from '@sveltestrap/sveltestrap';
  const colors = [
    'primary',
    'secondary',
    'success',
    'danger',
    'warning',
    'info',
    'light',
    'dark'
  ];
</script>

<Styles />

<svelte:head>
	<title>Home</title>
	<meta name="description" content="Svelte demo app" />

	<!-- Bootstrap -->
	<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/css/bootstrap.min.css">
</svelte:head>

<section>
	<h1>
		<span class="welcome">
			<picture>
				<source srcset={welcome} type="image/webp" />
				<img src={welcomeFallback} alt="Welcome" />
			</picture>
		</span>

		to your new<br />SvelteKit app
	</h1>

	<h2>
		try editing <strong>src/routes/+page.svelte</strong>
	</h2>
	
	<br>

	<Row>
		<Col>
			<Button color="primary" outline><i class="bi bi-airplane-engines"></i> Hello World! <i class="bi bi-airplane-engines"></i></Button>
		</Col>
	</Row>

	<br>

	<Row>
		<Col>
			<ListGroup>
				{#each colors as color}
					<ListGroupItem {color}>{color}</ListGroupItem>
				{/each}
			</ListGroup>
		</Col>
	</Row>

	<Counter />
</section>

<style>
	@import 'https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/css/bootstrap.min.css';

	section {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		flex: 0.6;
	}

	h1 {
		width: 100%;
	}

	.welcome {
		display: block;
		position: relative;
		width: 100%;
		height: 0;
		padding: 0 0 calc(100% * 495 / 2048) 0;
	}

	.welcome img {
		position: absolute;
		width: 100%;
		height: 100%;
		top: 0;
		display: block;
	}
</style>
