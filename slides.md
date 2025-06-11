---
# You can also start simply with 'default'
theme: seriph
# random image from a curated Unsplash collection by Anthony
# like them? see https://unsplash.com/collections/94734566/slidev
background: /images/abstract54.jpg
# some information about your slides (markdown enabled)
title: Vita
info: |
  ## Slidev Starter Template
  Presentation slides for developers.

  Learn more at [Sli.dev](https://sli.dev)
# apply unocss classes to the current slide
class: text-center
# https://sli.dev/features/drawing
drawings:
  persist: true
# slide transition: https://sli.dev/guide/animations.html#slide-transitions
transition: slide-left
# enable MDC Syntax: https://sli.dev/features/mdc
mdc: true

# open graph
# seoMeta:
#  ogImage: /images/abstract54.jpg
---

# Vitajte na prezentácii prezentácie

SliDev = ako na prezentáciu inak

<div @click="$slidev.nav.next" class="mt-12 py-1" hover:bg="white op-10">
  <carbon:arrow-right />
</div>

<button @click="playMusic" class="slidev-icon-btn">
  Spustiť hudbu na pozadie
</button>

<audio src="/audio/shittyFl.mp3" id="bg-music" loop hidden />
<div class="abs-br m-6 text-xl">
  <button @click="$slidev.nav.openInEditor()" title="Open in Editor" class="slidev-icon-btn">
    <carbon:edit />
  </button>
  <a href="https://github.com/slidevjs/slidev" target="_blank" class="slidev-icon-btn">
    <carbon:logo-github />
  </a>
</div>



<script setup>
import { onMounted } from 'vue'
function playMusic() {
  const audio = document.getElementById('bg-music')
  if (audio) {
    audio.currentTime = 0
    audio.play()
    setTimeout(() => {
      audio.pause()
    }, 30000) // stop after 30 seconds
  }
}
</script>

<!--
The last comment block of each slide will be treated as slide notes. It will be visible and editable in Presenter Mode along with the slide. [Read more in the docs](https://sli.dev/guide/syntax.html#notes)
-->

<!--
notes notes
-->

---
transition: fade-out
---
<section style="position: fixed; inset: 0; z-index: 50; background: black; display: flex; align-items: center; justify-content: center;">
  <video
    src="/videos/erniIntro.mp4"
    controls
    autoplay
    muted
    style="width: 100vw; height: 100vh; object-fit: cover; display: block;"
  />
</section>

---
transition: fade-out
layout: two-cols
layoutClass: gap-12
---

# Čo si dnes ukážeme?
<v-click>
  <div
    v-motion
    :initial="{ x: -500 }"
    :enter="{ x: 0 }" >
    ako jednoducho sa používa SliDev
  </div>
</v-click>

<br><v-click><img src= "/images/erniLogo.png" inline-block h-2 animate-bounce> Ukážeme si základné funkcie, ktoré môžu, ale nemusia, zákazníkovy odpáliť dekel</v-click>
<br><v-click><img src= "/images/erniLogo.png" inline-block h-3 animate-bounce> Čo dokáže funkcia prezenter</v-click>
<br><v-click><img src= "/images/erniLogo.png" inline-block h-4 animate-bounce> Ukážeme si nahrávanie</v-click>
<br><v-click><img src= "/images/erniLogo.png" inline-block h-5 animate-bounce> Remote session</v-click>
<br><v-click><img src= "/images/erniLogo.png" inline-block h-8 animate-bounce> Erni template</v-click>
<br><v-click><img src= "/images/erniLogo.png" inline-block h-13 animate-bounce> Addons</v-click>
<br>
<br>

::right::

<img :src="randomImage" alt="Random image" class="h-full w-auto object-cover" />


<script setup>
const images = [
  '/images/abstractImages/Abstract web picture (1).jpg',
  '/images/abstractImages/Abstract web picture (17).jpg',
  '/images/abstractImages/Abstract web picture 66.jpg',
  '/images/abstractImages/Abstract web picture 88.jpg'
]
const randomImage = images[Math.floor(Math.random() * images.length)]
</script>

<div class="absolute bottom-4 left-0 w-full text-center text-sm opacity-70">
  <img src= "/images/erniLogo.png" inline-block h-5>
   2025 Matus &middot; All rights reserved
</div>

<!--
You can have `style` tag in markdown to override the style for the current page.
Learn more: https://sli.dev/features/slide-scope-style
-->

<style>
h1 {
  background-color: #2B90B6;
  background-image: linear-gradient(45deg,rgb(85, 136, 194) 20%,rgb(33, 35, 139) 40%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}
.slidev-vclick-target {
  transition: all 2000ms ease 10ms;
}
.slidev-vclick-hidden {
  transform: scale(0);
}
</style>

<!--
Here is another comment.
-->

---
transition: fade-out
---

<section style="position: fixed; inset: 0; z-index: 50; background: black; display: flex; align-items: center; justify-content: center;">
  <video src="/videos/outroBetterask.mp4" controls autoplay muted style="width: 100vw; height: 100vh; object-fit: cover; display: block;" />
</section>

<!--
Here is another comment.
-->

---
transition: fade-out
layout: two-cols
layoutClass: gap-12
preload: false
---

# Jeden testerský na úvod

<img src="/images/realMen.jpg" class="w-full w-auto object-cover" />

::right::

<v-click>
  <div class="flex items-center justify-center h-full"
    v-motion
    :initial="{ x: -250 }"
    :enter="{ x: 0 }" >
    <span class="gradient-text" style="font-size: 2rem;">
    Ako rozbehať&nbsp;<a href="https://sli.dev/guide" target="_blank">SliDev.</a>
    </span>
  </div>
</v-click>

<style>
h1,
.gradient-text {
  background-color: #2B90B6;
  background-image: linear-gradient(45deg,rgb(85, 136, 194) 20%,rgb(33, 35, 139) 40%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}
</style>
