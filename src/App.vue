<template>
  <div>
    <HeaderLayout fonts="gmarket container"/>
    <SliderSection />
    <ImageSection attr="section nexon" layout="container"/>
    <ImgTextSection attr="section nexon" layout="container" />
    <CardSection attr="section nexon container" />
    <BannerSection attr="section nexon" />
    <TextSection attr="section nexon container" />
    <FooterLayout attr="section nexon" layout="container" />
  </div>
</template>

<script>
import HeaderLayout from './components/layout/HeaderLayout.vue';
import SliderSection from './components/section/SliderSection.vue';
import ImageSection from './components/section/ImageSection.vue';
import ImgTextSection from './components/section/ImgTextSection.vue';
import CardSection from './components/section/CardSection.vue';
import BannerSection from './components/section/BannerSection.vue';
import TextSection from './components/section/TextSection.vue';
import FooterLayout from './components/layout/FooterLayout.vue';

export default {
  name: 'App',
  components: {
    HeaderLayout,
    SliderSection,
    ImageSection,
    ImgTextSection,
    CardSection,
    BannerSection,
    TextSection,
    FooterLayout,
  }
}
</script>

<style>
</style>
