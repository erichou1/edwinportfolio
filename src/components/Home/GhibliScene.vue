<template>
  <div class="ghibliScene">
    <SceneSection id="Ghibli">
    <TextBlock>
        <p class="-big">(Summer 2024) <br>
          <strong class="-purple" style="font-size: 1em;">Independent Research</strong>
          <strong style="font-size: 1em;"> On </strong>
          <a
            href="https://github.com/edwin-hou/AIDetectorResearch/blob/main/Research%20Paper.pdf"
            target="_blank"
            title="Visit Biz Commerce's website"
            style="font-size: 1em;"
          >AI Accuracy</a
          >
          </p>
          <p style="font-size: 1.1em;">Independent research paper on the accuracy AI detectors published in a<a style="color: #682ae9; text-decoration: none;"> Well Respected Journal</a>.</p>

      </TextBlock>
      

      <template #container>
        <div class="sky">
          <div class="cloud c1"></div>
          <div class="cloud c2"></div>
        </div>

        <HolwsCastle :isPlaying="isPlaying" />

        <div class="grass1"></div>
        <div class="grass2"></div>
      </template>
    </SceneSection>
    <SceneSection id="Ghibli2" />
    <SceneSection id="Ghibli3">
    <TextBlock>
        <p class="-big">(Fall 2023) <br>
          <strong class="-purple" style="font-size: 1em;">Full Stack Engineer Internship</strong>
          <strong style="font-size: 1em;"> @ </strong>
          <a
            href="https://thecommonsxr.com/"
            target="_blank"
            title="Visit Biz Commerce's website"
            style="font-size: 1em;"
          >The CommonsXR</a
          >
          </p>
          <p style="font-size: 1.1em;">Only high school intern in revolutionary EdTech Startup that is multiple times published in<a style="color: #682ae9; text-decoration: none;"> IEEE Explorer</a>.</p>

      </TextBlock>
      
    </SceneSection>
    <SceneSection>
    <TextBlock>
        <p class="-big">
          Studying
          <span class="-purple"
            >Math, Coding, Video Games</span
          >
        </p>
        <p>
          And publishing memes on Reddit & .
        </p>
      </TextBlock>
    </SceneSection>
    <SceneSection id="Ghibli4" />
  </div>
</template>

<script>
import HolwsCastle from '../Characters/HolwsCastle/HolwsCastle.vue'
import SceneSection from '../SceneSection.vue'
import TextBlock from '../TextBlock.vue'

export default {
  name: 'GhibliScene',
  props: {
    isPlaying: Boolean,
  },
  components: { TextBlock, SceneSection, HolwsCastle },
}
</script>

<style lang="scss">
.ghibliScene {
  .castle-container {
    position: absolute;
    top: 70%;
    left: 100%;
    transform: scale(0.5);

    @media screen and (max-width: 568px) {
      transform: scale(0.3);
    }
  }

  .sky {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;

    .c1 {
      position: absolute;
      transform-origin: left bottom;
      bottom: 0;
      left: 0;
      width: 45vw;
      height: 50vh;
      background: url('../../components/Characters/HolwsCastle/assets/cloud1.png')
        no-repeat 0 bottom;
      background-size: contain;
    }

    .c2 {
      position: absolute;
      transform-origin: right bottom;
      bottom: 0;
      right: 0;
      width: 60vw;
      height: 60vh;
      background: url('../../components/Characters/HolwsCastle/assets/cloud2.png')
        no-repeat right bottom;
      background-size: contain;
    }

    @media screen and (max-width: 768px) {
      .c1,
      .c2 {
        width: 100vw;
        height: 90vh;
        background-size: 100% auto;
      }
    }
  }

  .grass1 {
    transform-origin: left bottom;
    position: absolute;
    bottom: 0;
    left: 0;
    width: 50vw;
    height: 25vh;
    transform: scale(1.2);
    background: url('../../components/Characters/HolwsCastle/assets/grass1.png')
      no-repeat 0 bottom;
    background-size: contain;
    filter: blur(2px);
  }

  .grass2 {
    transform-origin: right bottom;
    position: absolute;
    bottom: 0;
    right: 0;
    width: 40vw;
    height: 20vh;
    transform: scale(1.2);
    background: url('../../components/Characters/HolwsCastle/assets/grass2.png')
      no-repeat right bottom;
    background-size: contain;
    filter: blur(2px);
  }
}
</style>
