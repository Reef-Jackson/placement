<script>
  import Nav from "../components/nav.svelte";
  import Typewriter from "svelte-typewriter";
  import { fade } from "svelte/transition";
  import { onMount } from "svelte";

  let mode;
  let open;

  function scrollIntoView({ target }) {
    const el = document.querySelector(target.getAttribute("href"));
    if (!el) return;
    el.scrollIntoView({
      behaviour: "smooth",
    });
  }
</script>

<Nav />

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
    <h1 style="color: white; text-align:center; font-size: 2rem; margin-top: 3rem;">About me!</h1>
    <div class="about-container">
      <div class="text">
        <h3>
          <h1>I'm Reef!</h1><br /><br /> A software engineering student on a perpetual
          quest for knowledge. With a solid academic foundation, technical
          prowess in
          <a href="#tech" on:click|preventDefault={scrollIntoView}
            >various technologies</a
          >, and
          hands-on project experience
          , I thrive on always learning something new. <br /><br />I'm a firm
          believer in the importance of always learning. <br><br>Beyond coding, you can
          find me immersed in Warhammer40K, Star Wars, and anything that can run
          DOOM.
        </h3>
      </div>
      <div class="image">image</div>
    </div>
  </div>
  <div class="work-wrapper" id="work">
    <h1 style="text-align: center; color: white;">My Work:</h1>
    <div class="work" id="work">
    <div class="work-item" id="bucketlist">
      <h1>BucketList!</h1>
      <button>Learn more</button>
    </div>
    <div class="work-item">item2</div>
    <div class="work-item">item2</div>
    <div class="work-item">item2</div>
  </div>
  </div>
  
  <div class="tech" id="tech">
    <h2 style="font-size: 2rem; color: white; margin-bottom: .5rem">
      My tech:
    </h2>
    <div class="tech-container">
      <a href="https://svelte.dev/">
        <button id="svelte">Svelte</button>
      </a>
      <a href="https://kit.svelte.dev">
        <button id="sveltekit">SvelteKit</button>
      </a>
      <button id="nodejs">NodeJS</button>
      <button id="php">PHP</button>
      <button id="html">HTML</button>
      <button id="css">CSS</button>
      <button id="js">JavaScript</button>
      <button id="csharp">C#</button>
      <button id="python">Python</button>
      <button id="sql">SQL</button>
      <button id="pocketbase">Pocketbase</button>
    </div>
  </div>
</div>

<style>

  a {
    text-decoration: none;
    color: white;
  }

  button {
    transition: transform .2s;
  }

  button:hover {
    transform: scale(1.1);
  }
  .wrapper {
    display: flex;
    flex-direction: column;
    justify-content: center;
  }
  .hero {
    height: 100vh;
    width: 100vw;
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
  }
  .text,
  .image {
    width: 30rem;
    background-color: #df5757;
    margin: 1rem;
    border-radius: 1rem;
    padding: 3rem;
    box-shadow: rgba(6, 24, 44, 0.4) 0px 0px 0px 2px,
      rgba(6, 24, 44, 0.65) 0px 4px 6px -1px,
      rgba(255, 255, 255, 0.08) 0px 1px 0px inset;
  }

  .text {
    background-color: #df5757;
  }

  .image {
    background-image: url($lib/eva.png);
    background-position: center;
  }

  .text a {
    text-decoration: none;
    color: yellow;
  }

  .text a:hover {
    text-decoration: underline;
  }

  .tech {
    width: 100vw;
    background-color: #111020;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
  }

  .tech-container {
    height: fit-content;
    width: fit-content;
    background: #df57578f;
    border-radius: 1rem;
    margin: 1rem;
    padding: 1rem;
    flex-wrap: 1;
  }

  button {
    padding-left: 0.8rem;
    padding-right: 0.8rem;
    padding-top: 0.5rem;
    padding-bottom: 0.5rem;
    margin: 0.4rem;
    border-radius: 0.8rem;
    font-size: 1.2rem;
    font-family: "Ubuntu", monospace;
    color: white;
    border: none;
    box-shadow: rgba(0, 0, 0, 0.35) 0px 5px 15px;
    transition: transform 0.2s;
    background-color: #df5757;
  }

  .tech-container button:hover {
    transform: scale(1.1);
  }
  #svelte,
  #sveltekit {
    background-color: #ff3c00;
  }
  #nodejs {
    background-color: #9bb48f;
  }
  #php {
    background-color: #6c7eb7;
  }
  #html {
    background-color: #db4c25;
  }
  #css {
    background-color: #29a6db;
  }
  #csharp {
    background-color: #802d97;
  }
  #python {
    color: black;
    background: linear-gradient(
      to right,
      rgb(94, 94, 255) 0%,
      rgb(73, 73, 231) 50%,
      rgb(239, 239, 135) 50%,
      rgb(225, 225, 106) 100%
    );
  }
  #js {
    background-color: #edd84d;
  }

  .work {
    background-color: #df5757;
    margin: 1rem;
    border-radius: 1rem;
    display: flex;
    flex-wrap: wrap;
  }

  .work-item {
    width: calc(
      33.33% - 2rem
    ); 
    display: flex;
    flex-direction: column;
    justify-content: flex-end;
    align-items: center;
    height: 20rem;
    border-radius: 1rem;
    margin: 1rem; 
    background-image: url("$lib/eva.png");
    box-shadow: rgba(0, 0, 0, 0.25) 0px 54px 55px, rgba(0, 0, 0, 0.12) 0px -12px 30px, rgba(0, 0, 0, 0.12) 0px 4px 6px, rgba(0, 0, 0, 0.17) 0px 12px 13px, rgba(0, 0, 0, 0.09) 0px -3px 5px;
    transition: transform 0.2s;
  }


  .work-item:hover {
    transform: scale(1.03);
  }

  
  .work-item h1 {
    color: white;
  }

  #bucketlist {
    background-image: url('$lib/bucketlist.png');
    background-size: cover;
    background-repeat: no-repeat;
    background-position: center center;
  }

  @media (max-width: 768px) {
    .work-item {
      width: calc(
        50% - 2rem
      ); 
    }
  }

  @media (max-width: 480px) {
    .work-item {
      width: 100%;
      margin: 0.8rem; 
    }
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
    .about-me {
      display: block;
      margin-bottom: 1rem;
      height: fit-content;
    }
    .about-container {
      flex-wrap: wrap;
      margin-bottom: 2rem;
      height: fit-content;
    }
    .text {
      padding: 0.8rem;
      width: 100%;
    }

    .image {
      padding: 0.8rem;
      margin: 1rem;
      height: 30rem;
      max-width: 100%;
    }

    .tech-container {
      margin: 1rem;
      border-radius: 1rem;
    }
  }

  @media (max-width: 667px) {
    .hero {
      background-position: -110vw;
    }
  }
</style>
