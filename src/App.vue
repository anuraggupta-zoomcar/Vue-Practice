<script setup>
  import Header from '@/components/Header.vue';
  import Counter from '@/components/Counter.vue';
  import Conditional from '@/components/Conditional.vue';
  import MultiStepForm from '@/components/MultiStepForm.vue';
  import EventHandling from './components/EventHandling.vue';
  import HandleInput from './components/HandleInput.vue';
  import FormHandling from './components/FormHandling.vue';
  import Watchers from './components/Watchers.vue';
  import APIcalling from './components/APIcalling.vue';
  import Props from './components/Props.vue';
  import ListRender from './ListRender.vue';
  import SlotTag from './components/SlotTag.vue';

</script>

<template>
  <!-- <Header /> -->
  <!-- <Counter /> -->
  <!-- <Conditional/> -->
  <!-- <MultiStepForm/> -->
  <!-- <EventHandling />
  <HandleInput />
  <FormHandling />
  <Watchers /> -->
  <APIcalling />
  <Props title="Welcome To Zoomcar!"/>
  <ListRender />
  <SlotTag>
    <h1>Dynamic Title</h1>
    <p>Description comes from Parent!</p>
  </SlotTag>
</template>

<style scoped>
</style>
