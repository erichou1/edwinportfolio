<template>
  <section class="scene-intro" id="intro">
    <div class="static-container">
      <h1 class="title">
        <span class="edwin">edwin</span>
        <span class="func">.is()</span>
      </h1>

      <TextBlock>
        <p class="-purple">Edwin Hou</p>
        <p class="-gray">Math Enthusiast</p>
      </TextBlock>
    </div>
  </section>
</template>

<script>
import TextBlock from '../TextBlock.vue'

export default {
  name: 'IntroScene',
  components: { TextBlock },
}
</script>
