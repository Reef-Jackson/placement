<script>
	import Nav from "../components/nav.svelte";
	import Typewriter from "svelte-typewriter";
	import { fade } from "svelte/transition";
  	import { onMount } from "svelte";

	let mode;
	let open;

	function scrollIntoView({target}) {
		const el = document.querySelector(target.getAttribute('href'));
		if (!el) return;
		el.scrollIntoView({
			behaviour: 'smooth'
		});
	}
</script>


<Nav/>

<div class="wrapper">
	<div class="hero" id="home">
		<div class="container">
			<div class="header-container">
				<Typewriter mode={"cascade"}>
					<h1>Reef Jackson</h1>
					<p>Software Engineering Student</p>
					<p2>I make computers do things!</p2>
				</Typewriter>
			</div>
		</div>
	</div>
	<div class="about-me" id="about">
		<div class="about-container">
			<div class="text">
				<h1>About me!</h1>
				<h3>I'm Reef!<br><br> A software engineering student on a perpetual quest for knowledge. With a solid academic foundation, technical prowess in <a href="#home" on:click|preventDefault={scrollIntoView}>various technologies</a>, and <a href="#work" on:click|preventDefault={scrollIntoView}><i>hands-on project experience</i></a>, I thrive on always learning something new. <br><br>I'm a firm believer in the importance of always learning. Beyond coding, you can find me immersed in Warhammer40K, Star Wars, and anything that can run DOOM.</h3>
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
			box-shadow: rgba(6, 24, 44, 0.4) 0px 0px 0px 2px, rgba(6, 24, 44, 0.65) 0px 4px 6px -1px, rgba(255, 255, 255, 0.08) 0px 1px 0px inset;
		}

		.text a {
			text-decoration: none;
			color: yellow;
		}

		.text a:hover {
			text-decoration: underline;
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

	@media (max-width: 667px) {
		.hero {
			background-position: -110vw;
		}
	}

</style>
