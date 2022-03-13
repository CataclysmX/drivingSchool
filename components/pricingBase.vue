<template>
  <div class="xl:w-1/4 md:w-1/2 w-full " :class="[!popular ? 'p-4 mx-8' : 'p-1']">
    <div class="main h-full p-6 rounded-lg border-2 flex flex-col relative overflow-hidden transition-shadow ease-in-out duration-300 hover:shadow-lg" :class="[popular ? 'border-blue-500' : '']">
      <span v-if="popular" class="bg-blue-500 text-white px-3 py-1 tracking-widest text-xs absolute right-0 top-0 rounded-bl">POPULAIRE</span>
      <h2 class="text-md tracking-widest title-font mb-1 font-medium">
        <span class="text-xl" v-text="prefixEmoji" />
        {{ nomOffre }}
        <span class="text-xl" v-text="suffixEmoji" />
      </h2>
      <h1 class="text-5xl text-gray-900 leading-none flex items-center pb-4 mb-4 border-b border-gray-200">
        <span v-text="prix" />
        <span class="text-lg ml-1 font-normal text-gray-500">/mo</span>
      </h1>
      <p v-for="(option, index) in options" :key="index" class="flex items-center text-gray-600 mb-2">
        <span class="w-4 h-4 mr-2 inline-flex items-center justify-center bg-gray-400 text-white rounded-full flex-shrink-0">
          <svg
            fill="none"
            stroke="currentColor"
            stroke-linecap="round"
            stroke-linejoin="round"
            stroke-width="2.5"
            class="w-3 h-3 transition-background ease-in-out duration-300"
            viewBox="0 0 24 24"
          >
            <path d="M20 6L9 17l-5-5" />
          </svg>
        </span>
        <span>
          {{ option }}
        </span>
      </p>
      <button class="hidden flex items-center mt-auto text-white bg-blue-500 border-0 py-2 px-4 w-full focus:outline-none hover:bg-blue-600 rounded">
        Button
        <svg
          fill="none"
          stroke="currentColor"
          stroke-linecap="round"
          stroke-linejoin="round"
          stroke-width="2"
          class="w-4 h-4 ml-auto"
          viewBox="0 0 24 24"
        >
          <path d="M5 12h14M12 5l7 7-7 7" />
        </svg>
      </button>
      <p class="text-xs text-gray-500 mt-3" v-text="info" />
      </h2>
    </div>
  </div>

  </div>
</template>

<script>
export default {
  props: {
    popular: {
      type: Boolean,
      default: false
    },
    nomOffre: {
      type: String,
      default: null
    },
    prix: {
      type: String,
      default: ''
    },
    options: {
      type: Array,
      default () {
        return []
      }
    },
    info: {
      type: String,
      default: null
    },
    prefixEmoji: {
      type: String,
      default: null
    },
    suffixEmoji: {
      type: String,
      default: null
    }
  }
}
</script>

<style lang="css" scoped>
.main:hover p svg{
  @apply bg-blue-500;
}
</style>
