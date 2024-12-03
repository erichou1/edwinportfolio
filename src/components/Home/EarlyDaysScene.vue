<template>
  <div class="earlyDays">
    <TitleSection scene="earlyTitle">
      <TitleFunction
        params="2018,2021"
        subtitle="&lt;table&gt;&lt;tr&gt;&lt;td&gt;..."
        >otherDays</TitleFunction
      >
      <div class="clouds cloud-1"></div>
      <Pepe v-bind="{ isPlaying }" />
      <div class="clouds cloud-2"></div>
      <div class="clouds cloud-3"></div>
      <Ocean v-bind="{ isPlaying }" />
    </TitleSection>

    <SceneSection id="early-days">
      <TextBlock>

        <p class="-big">
          (Spring 2024) <br>
          <strong class="-purple" style="font-size: 1.4em;">USAMO Qualification</strong>
          </p>
          <p style="font-size: 1.1em; font-weight: bold;">Prestigious Invitational <a style="color: #682ae9; text-decoration: none;"> Mathematics </a> Commpetition. </p>
          <strong style="font-size: 1.4em;">Top<a style="color: #682ae9; text-decoration: none;"> 250 (0.4%)</a> in the United States.</strong>
      </TextBlock>
    </SceneSection>
    <SceneSection id="early-days2">
    <TextBlock>
        <p class="-big">(2021, now)<br>
          <strong class="-purple" style="font-size: 1em;">President</strong>
          <strong style="font-size: 1em;"> @ </strong>
          <a
            target="_blank"
            title="Visit Biz Commerce's website"
            style="font-size: 1em;"
          >Los Gatos High School Math Club</a
          >
          </p>
          <p style="font-size: 1.3em;">Organized math club with <a style="color: #682ae9; text-decoration: none;"> 20+</a> members and led them to high placement in the <a style="color: #682ae9; text-decoration: none;"> Stanford Math Tournament</a>.</p>

      </TextBlock>
      
    </SceneSection>
    <SceneSection id="early-days3">
    <TextBlock>
  
        <p class="-big">
          (2023, now) <br>
          <strong class="-purple" style="font-size: 1.4em;">Co-Founder</strong>
          <strong style="font-size: 1.4em;"> @ </strong>
          <a
            href="losgatoshacks.com"
            target="_blank"
            title="Visit Biz Commerce's website"
            style="font-size: 1.4em;"
          >Los Gatos Hacks</a
          >
          </p>
          <p style="font-size: 1.1em;">One of the largest high school hackathon on the West Coast <a style="color: #682ae9; text-decoration: none;"> 1k+ in prizes </a> and <a style="color: #682ae9; text-decoration: none;"> 50+ participants</a>.</p>
      </TextBlock>

    </SceneSection>
  </div>
</template>

<script>
import Pepe from '../Characters/Pepe/Pepe.vue'
import Ocean from '../Characters/Ocean/Ocean.vue'
import TitleSection from '../TitleSection.vue'
import TitleFunction from '../TitleFunction.vue'
import TextBlock from '../TextBlock.vue'
import SceneSection from '../SceneSection.vue'

export default {
  name: 'EarlyDaysScene',
  components: {
    TitleSection,
    Pepe,
    Ocean,
    TitleFunction,
    TextBlock,
    SceneSection,
  },
  props: {
    isPlaying: Boolean,
  },
}
</script>

<style lang="scss">
.earlyDays {
  .pepe {
    position: absolute;
    z-index: 2;
    top: 50%;
    left: 100%;
    transform: scale(0.4) translate3d(0, -50%, 0);
    transform-origin: 0 0;

    @media screen and (max-width: 568px) {
      transform: scale(0.2) translate3d(0, -50%, 0);
    }
  }

  .clouds {
    position: absolute;
    width: 150vw;
    height: 150vh;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    transform-origin: 50% 50%;
    background: url('../Characters/Pepe/assets/clouds-1.png') no-repeat center;
    background-size: contain;
    opacity: 0.5;

    &.cloud-2 {
      background-image: url('../Characters/Pepe/assets/clouds-2.png');
    }

    &.cloud-3 {
      background-image: url('../Characters/Pepe/assets/clouds-3.png');
      width: 100vw;
      height: 100vh;
      z-index: -1;
      opacity: 0.25;
    }
  }
}
</style>
