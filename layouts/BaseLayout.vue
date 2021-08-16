<template>
  <div>
    <nav
      class="flex items-center justify-between flex-wrap bg-blue-500 p-6 mb-2"
    >
      <div class="flex items-center flex-shrink-0 text-white mr-6">
        <span class="font-semibold text-xl tracking-tight"
          >SPACEX LAUNCHES</span
        >
      </div>
      <div class="block lg:hidden">
        <button
          class="
            flex
            items-center
            px-3
            py-2
            border
            rounded
            text-teal-200
            border-teal-400
            hover:text-white hover:border-white
          "
        >
          <svg
            class="fill-current h-3 w-3"
            viewBox="0 0 20 20"
            xmlns="http://www.w3.org/2000/svg"
          >
            <title>Menu</title>
            <path d="M0 3h20v2H0V3zm0 6h20v2H0V9zm0 6h20v2H0v-2z" />
          </svg>
        </button>
      </div>
      <div class="w-full block flex-grow lg:flex lg:items-center lg:w-auto">
        <div class="text-sm lg:flex-grow"></div>
        <div>
          <a
            href="https://www.spacex.com/"
            class="
              inline-block
              text-sm
              px-4
              py-2
              leading-none
              border
              rounded
              text-white
              border-white
              hover:border-transparent hover:text-blue-500 hover:bg-white
              mt-4
              lg:mt-0
            "
            >More</a
          >
        </div>
      </div>
    </nav>
    <div class="max-w-screen-lg mx-auto">
      <main>
        <Nuxt />
      </main>
    </div>
    <footer class="footer bg-white relative pt-1 border-b-2 border-blue-500">
      <div class="container mx-auto px-6"></div>
      <div class="container mx-auto px-6">
        <div
          class="mt-16 border-t-2 border-gray-300 flex flex-col items-center"
        >
          <div class="sm:w-2/3 text-center py-6">
            <p class="text-sm text-blue-500 font-bold mb-2">
              © 2021 by Griffin Harris
            </p>
          </div>
        </div>
      </div>
    </footer>
  </div>
</template>

<script>
export default {}
</script>
