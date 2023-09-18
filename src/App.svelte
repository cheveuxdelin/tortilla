<script lang="ts">
  import makina from "./assets/makina.jpg";
  import videoo from "./assets/pexels-cottonbro-5532774 (2160p).mp4";
  import "./app.css";
  import { onMount } from "svelte";
  import { fly, blur, slide, draw } from "svelte/transition";

  let initialTransition = false;

  onMount(() => {
    initialTransition = true;
  });
</script>

<svelte:head>
  <script
    src="https://kit.fontawesome.com/a06c8b31d1.js"
    crossorigin="anonymous"
  ></script>
</svelte:head>

{#if initialTransition}
  <main class="text-slate-300 bg-slate-900 antialiased font-light">
    <header
      class="flex w-full justify-between px-24 py-5 bg-slate-300 text-slate-700 mb-24"
    >
      <h1 class="text-5xl w-fit font-extralight">Maqinnova</h1>
      <div class="flex flex-col text-right">
        <a href="tel:+526441234567"
          ><i class="fa-solid fa-phone" /> +52 644-69696969</a
        >
        <a href="mailto:cheveuxdelin@icloud.com"
          ><i class="fa-solid fa-envelope" /> cheveuxdelin@icloud.com</a
        >
      </div>
    </header>

    <div class="h-full px-24 relative">
      <div transition:fly={{duration: 1000}}>
        <div class="flex w-full justify-between mb-20">
          <img
            src={makina}
            alt="tortilla maquina"
            class="rounded-2xl h-[400px]"
          />

          <div
            class="flex flex-col mt-10 space-y-3 text-5xl text-right items-end"
          >
            <p>Capacidad de 15 litros</p>
            <p>3000 bolas de masa por hora</p>
            <p>Acero inoxidable</p>
            <p class="bg-green-600 w-fit text-right">$37,500.00</p>
          </div>
        </div>

        <p class="text-center text-lg mb-14 px-28">
          Presentamos nuestra revolucionaria Cortadora de Acero Inoxidable,
          diseñada para optimizar la producción al rebanar bolas de masa con
          precisión y eficiencia. Con capacidad para procesar hasta 3000 bolas
          por hora, garantiza cumplir pedidos exigentes sin comprometer la
          calidad. Fabricada con acero inoxidable de alta calidad, su diseño
          ergonómico y características de seguridad avanzadas la convierten en
          la elección ideal para mejorar tu proceso de producción y elevar la
          calidad de tus productos finales.
        </p>
      </div>

      <img src={videoo} alt="video"/>
    </div>
  </main>
{/if}
