<template lang="html">
  <div class="">
    <div class="w-full bg-current pt-56" :class="{'pb-56': !separator}">
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
    },
    animation: {
      type: String,
      default: ''
    },
    test: {
      type: String,
      default: ''
    }
  },
  mounted () {
    const animation = this.fetchAnimation()
    const box = this.$el.querySelector('img')

    document.addEventListener('scroll', function () {
      if (isInViewport(box) && animation.length !== 0) {
        box.classList.add(animation)
      }
    }, {
      passive: true
    })

    function isInViewport (el) {
      const rect = el.getBoundingClientRect()
      return (
        rect.top >= 0 &&
              rect.left >= 0 &&
              rect.bottom <= (window.innerHeight || document.documentElement.clientHeight) &&
              rect.right <= (window.innerWidth || document.documentElement.clientWidth)
      )
    }
  },
  methods: {
    fetchAnimation () {
      const self = this
      return self.animation
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

.animation2{
  animation-fill-mode: both;
  animation-duration: 1000ms;
  animation-delay: 150ms;
  animation-iteration-count: 1;
  opacity: 1;
  animation-name: animation2;

}

@-webkit-keyframes animation2{
  0% {
    transform: translate3d(100%, 0px, 0px) skewX(-30deg);
    opacity: 0;
  }
  60% {
    transform: skewX(20deg);
    opacity: 1;
  }
  80% {
    transform: skewX(-5deg);
    opacity: 1;
  }
  100% {
    transform: none;
    opacity: 1;
  }
}
@keyframes animation2{
  0% {
    transform: translate3d(100%, 0px, 0px) skewX(-30deg);
    opacity: 0;
  }
  60% {
    transform: skewX(20deg);
    opacity: 1;
  }
  80% {
    transform: skewX(-5deg);
    opacity: 1;
  }
  100% {
    transform: none;
    opacity: 1;
  }
}

.animation1{
  animation-fill-mode: both;
  animation-duration: 1000ms;
  animation-delay: 150ms;
  animation-iteration-count: 1;
  opacity: 1;
  animation-name: animation1;

}

@-webkit-keyframes animation1{
  0% {
    transform: scale3d(1, 1, 1);
  }
  10%, 20%{
    transform: scale3d(0.9, 0.9, 0.9) rotate3d(0, 0, 1, -3deg);
  }
  30%, 50%, 70%, 90% {
    transform: scale3d(1.1, 1.1, 1.1) rotate3d(0, 0, 1, 3deg);
  }
  40%, 60%, 80% {
    transform: scale3d(1.1, 1.1, 1.1) rotate3d(0, 0, 1, -3deg);
  }
  100% {
    transform: scale3d(1, 1, 1);
  }
}
@keyframes animation1{
  0% {
    transform: scale3d(1, 1, 1);
  }
  10%, 20%{
    transform: scale3d(0.9, 0.9, 0.9) rotate3d(0, 0, 1, -3deg);
  }
  30%, 50%, 70%, 90% {
    transform: scale3d(1.1, 1.1, 1.1) rotate3d(0, 0, 1, 3deg);
  }
  40%, 60%, 80% {
    transform: scale3d(1.1, 1.1, 1.1) rotate3d(0, 0, 1, -3deg);
  }
  100% {
    transform: scale3d(1, 1, 1);
  }
}

.animation0{
  animation-fill-mode: both;
  animation-duration: 1000ms;
  animation-delay: 150ms;
  animation-iteration-count: 1;
  opacity: 1;
  animation-name: animation0;

}

@-webkit-keyframes animation0{
  0% {
    transform: translate3d(-3000px, 0px, 0px);
    opacity: 0;
  }
  60% {
    transform: translate3d(25px, 0px, 0px);
    opacity: 1;
  }
  75% {
    transform: translate3d(-10px, 0px, 0px);
    opacity: 1;
  }
  90% {
    transform: translate3d(5px, 0px, 0px);
    opacity: 1;
  }
  100% {
    transform: none;
    opacity: 1;
  }
}
@keyframes animation0{
  0% {
    transform: translate3d(-3000px, 0px, 0px);
    opacity: 0;
  }
  60% {
    transform: translate3d(25px, 0px, 0px);
    opacity: 1;
  }
  75% {
    transform: translate3d(-10px, 0px, 0px);
    opacity: 1;
  }
  90% {
    transform: translate3d(5px, 0px, 0px);
    opacity: 1;
  }
  100% {
    transform: none;
    opacity: 1;
  }
}
</style>
