<template lang="html">
  <div class="max-h-screen removeBG">
    <div class="w-full bg-current pt-56" :class="{'pb-56 mt-48': !separator}">
      <div class="container mx-auto flex flex-wrap">
        <div v-if="!svgRight" class="w-full md:w-1/3">
          <slot />
        </div>
        <div class="w-full md:w-2/3 my-10 px-10">
          <h1
            class="text-blue-500 text-center font-bold mb-20"
            :class="[titleFontSize ? '' + titleFontSize : 'text-5xl']"
            v-text="title"
          />
          <p
            class="text-gray-900 px-4"
            :class="[textFontSize ? '' + textFontSize : 'text-3xl']"
            v-text="text"
          />
        </div>
        <div v-if="svgRight" class="w-full md:w-1/3">
          <slot />
        </div>
      </div>
    </div>
    <svg v-if="separator" class="separator" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1440 320"><path fill-opacity="1" d="M0,32L48,69.3C96,107,192,181,288,192C384,203,480,149,576,144C672,139,768,181,864,165.3C960,149,1056,75,1152,53.3C1248,32,1344,64,1392,80L1440,96L1440,0L1392,0C1344,0,1248,0,1152,0C1056,0,960,0,864,0C768,0,672,0,576,0C480,0,384,0,288,0C192,0,96,0,48,0L0,0Z" /></svg>
  </div>
</template>

<script>
export default {
  name: 'BlockDiv',
  props: {
    text: {
      type: String,
      default: null
    },
    textFontSize: {
      type: String,
      default: null
    },
    title: {
      type: String,
      default: null
    },
    titleFontSize: {
      type: String,
      default: null
    },
    separator: {
      type: Boolean,
      default: false
    },
    svgRight: {
      type: Boolean,
      default: false
    }
  }
}
</script>

<style lang="css" scoped>
img{
  width: 40rem
}
svg.separator path{
  @apply fill-current text-gray-50;
}
.removeBG{
  /*background-color: white !important;*/
}
</style>
