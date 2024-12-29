<script>
  export let status; // Código de estado HTTP (404, 500, etc.)
</script>

<svelte:head>
  <title>{status === 404 ? "404 - Página no encontrada" : "Error"}</title>
</svelte:head>

<div class="bg-indigo-900 relative overflow-hidden h-screen">
  <img
    src="https://external-preview.redd.it/4MddL-315mp40uH18BgGL2-5b6NIPHcDMBSWuN11ynM.jpg?width=960&crop=smart&auto=webp&s=b98d54a43b3dac555df398588a2c791e0f3076d9"
    class="absolute h-full w-full object-cover"
    alt="Background"
  />
  <div class="inset-0 bg-black opacity-25 absolute"></div>
  <div
    class="container mx-auto px-6 md:px-12 relative z-10 flex items-center py-32 xl:py-40"
  >
    <div class="w-full font-mono flex flex-col items-center relative z-10">
      <h1
        class="font-extrabold text-5xl text-center text-white leading-tight mt-4"
      >
        {status === 404 ? "You are all alone here" : "Something went wrong"}
      </h1>
      {#if status === 404}
        <p class="font-extrabold text-8xl my-44 text-white animate-bounce">
          404
        </p>
      {:else}
        <p class="font-extrabold text-8xl my-44 text-white animate-bounce">
          {status}
        </p>
      {/if}
    </div>
  </div>
</div>

<style>
  * {
    height: 100%;
    width: 100%;
  }
</style>
