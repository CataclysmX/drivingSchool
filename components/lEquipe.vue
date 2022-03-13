<template lang="html">
  <section class="text-gray-600 body-font">
    <div class="container px-5 py-24 mx-auto">
      <div class="flex flex-col text-center w-full mb-20">
        <h1 class="sm:text-3xl text-2xl font-medium title-font mb-4 text-gray-900">
          Nos formatrice / formateur
        </h1>
        <p class="lg:w-2/3 mx-auto leading-relaxed text-base">
          Whatever cardigan tote bag tumblr hexagon brooklyn asymmetrical gentrify, subway tile poke farm-to-table. Franzen you probably haven't heard of them.
        </p>
      </div>
      <div class="flex flex-wrap -m-2">
        <div v-for="(enseignant, index) in enseignants" :key="index" class="p-4 lg:w-1/2">
          <div class="h-full flex sm:flex-row flex-col items-center sm:justify-start justify-center text-center sm:text-left">
            <img alt="team" class="flex-shrink-0 rounded-lg w-40 h-40 object-cover object-center sm:mb-0 mb-4" :src="'/PP/'+enseignant.prenom+'.jpeg'">
            <div class="flex-grow sm:pl-8">
              <h2 class="title-font font-medium text-lg text-gray-900">
                <span class="uppercase">{{ enseignant.nom }}</span> <span class="capitalize">{{ enseignant.prenom }}</span>
              </h2>
              <h3 class="text-gray-500 mb-3">
                <ul>
                  <li v-for="type in enseignant.type" :key="type">
                    {{ type }}
                  </li>
                </ul>
              </h3>
              <p class="mb-4 text-xs">
                Autorisaton d'enseigner : <span>{{ enseignant.autorisation }}<span /></span>
              </p>
              <span class="inline-flex">
                <a class="text-gray-500">
                  <svg
                    fill="none"
                    stroke="currentColor"
                    stroke-linecap="round"
                    stroke-linejoin="round"
                    stroke-width="2"
                    class="w-5 h-5"
                    viewBox="0 0 24 24"
                  >
                    <path d="M18 2h-3a5 5 0 00-5 5v3H7v4h3v8h4v-8h3l1-4h-4V7a1 1 0 011-1h3z" />
                  </svg>
                </a>
                <a class="ml-2 text-gray-500">
                  <svg
                    fill="none"
                    stroke="currentColor"
                    stroke-linecap="round"
                    stroke-linejoin="round"
                    stroke-width="2"
                    class="w-5 h-5"
                    viewBox="0 0 24 24"
                  >
                    <path d="M23 3a10.9 10.9 0 01-3.14 1.53 4.48 4.48 0 00-7.86 3v1A10.66 10.66 0 013 4s-4 9 5 13a11.64 11.64 0 01-7 2c9 5 20 0 20-11.5a4.5 4.5 0 00-.08-.83A7.72 7.72 0 0023 3z" />
                  </svg>
                </a>
                <a class="ml-2 text-gray-500">
                  <svg
                    fill="none"
                    stroke="currentColor"
                    stroke-linecap="round"
                    stroke-linejoin="round"
                    stroke-width="2"
                    class="w-5 h-5"
                    viewBox="0 0 24 24"
                  >
                    <path d="M21 11.5a8.38 8.38 0 01-.9 3.8 8.5 8.5 0 01-7.6 4.7 8.38 8.38 0 01-3.8-.9L3 21l1.9-5.7a8.38 8.38 0 01-.9-3.8 8.5 8.5 0 014.7-7.6 8.38 8.38 0 013.8-.9h.5a8.48 8.48 0 018 8v.5z" />
                  </svg>
                </a>
              </span>
            </div>
          </div>
        </div>
      </div>
      <div class="flex my-4">
        <hr class="my-auto grow">
        <span class="mx-4">OU</span>
        <hr class="my-auto grow">
      </div>
      <div class="flex flex-wrap -m-2">
        <div v-for="(enseignant, index) in enseignants" :key="index" class="p-2 lg:w-1/3 md:w-1/2 w-full">
          <div class="h-full flex items-center border-gray-200 border p-4 rounded-lg hover:shadow-lg transition-all duration-300 ease-in-out hover:scale-105 ">
            <img alt="team" class="w-32 h-32 bg-gray-100 object-cover object-center flex-shrink-0 rounded-lg mr-4" :src="'/PP/'+enseignant.prenom+'.jpeg'">
            <div class="flex-grow">
              <h2 class="text-gray-900 title-font font-medium">
                <span class="uppercase">{{ enseignant.nom }}</span> <span class="capitalize">{{ enseignant.prenom }}</span>
              </h2>
              <ul class="text-gray-500 mb-4 mt-1">
                <li v-for="type in enseignant.type" :key="type">
                  {{ type }}
                </li>
              </ul>
              <!-- <p class="text-gray-500 mb-4 mt-1">
                {{ enseignant.type }}
              </p> -->
              <hr>
              <p class="text-xs text-gray-500 mt-4">
                Autorisaton d'enseigner : <span>{{ enseignant.autorisation }}<span /></span>
              </p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  props: {
    enseignants: {
      type: Array,
      default () {
        return []
      }
    }
  }
}
</script>

<style lang="css" scoped>
</style>
