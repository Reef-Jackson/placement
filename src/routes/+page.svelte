<script>
	import { Hamburger } from "svelte-hamburgers";
	import Nav from "../components/nav.svelte";
	import Typewriter from "svelte-typewriter";
	import { fade } from "svelte/transition";

	let mode;

	let open;
</script>

<!-- <Hamburger bind:open --color="white" />
<Menu bind:open /> -->

<Nav />

<div class="wrapper">
	<div class="hero">
		<div class="container">
			<div class="header-container">
				<Typewriter mode={"cascade"}>
					<h1>Reef Jackson</h1>
					<p>Software Engineering Student</p>
					<p2>I create stuff with computers!</p2>
				</Typewriter>
			</div>
		</div>
	</div>
	<div class="about-me">
		<div class="about-container">
			<div class="text">
				<h1>About me!</h1>
				<h3>Hi I'm Reef! I'm currently a student at SHU and am eagerly searching for my first placement opportunity!</h3>
			</div>
			<div class="image">image</div>
		</div>
	</div>
</div>

<style>
	.hero {
		height: 100vh;
		display: flex;
		justify-content: center;
		align-items: center;
		background-color: black;
		background-image: url("$lib/window.jpg");
		background-size: cover;
		background-position: right;
		background-repeat: no-repeat;
	}

	.container {
		text-align: center;
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		--cursor-color: #ffff;
		color: white;
		width: 100%;
		height: 100%;
		background-color: rgba(0, 0, 0, 0.828);
	}
	.header-container h1 {
		font-size: 3rem;
		margin-bottom: 0.5rem;
	}
	.header-container p {
		font-size: 1.5rem;
		margin-top: 0;
		padding-top: 0;
		color: #df5757;
		padding-bottom: 1rem;
	}

	.about-container {
		height: 30rem;
		width: 100%;
		display: flex;
		color: white;
		justify-content: center;
		margin-bottom: 4rem;
		margin-top: 4rem;
	}
		.text,
		.image {
			width: 30rem;
			background-color:#df5757;
			margin: 1rem;
			border-radius: 1rem;
			padding: 3rem;
		}


	@media (max-width: 768px) {
   .header-container h1 {
		font-size: 1.5rem;
	 }
	 .header-container p {
		font-size: 1rem;
	 }
	 .header-container p2 {
		font-size: 1rem;
	 }
	 .hero {
		background-position: -220vw;
	 }
	 .about-container {
		flex-wrap: wrap;
	 }
	}

</style>
