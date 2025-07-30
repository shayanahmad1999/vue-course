<script setup>
import { ref } from 'vue';
import AttritubeBinding from './components/AttritubeBinding.vue';
import ComputedPropreties from './components/computedPropreties.vue';
import ConditionalRendering from './components/ConditionalRendering.vue';
import DynamicProps from './components/DynamicProps.vue';
import EventHandler from './components/EventHandler.vue';
import GlobalStyle from './components/GlobalStyle.vue';
import HelloWorld from './components/HelloWorld.vue';
import ItrationComponent from './components/ItrationComponent.vue';
import LocalStyle from './components/LocalStyle.vue';
import ModelComponent from './components/ModelComponent.vue';
import ModuleStyle from './components/ModuleStyle.vue';
import ReactiveComponent from './components/ReactiveComponent.vue';
import RefComponent from './components/RefComponent.vue';
import StaticProps from './components/StaticProps.vue';
import TextInterpolation from './components/TextInterpolation.vue';
import ValidtionProps from './components/ValidtionProps.vue';
import ComplexProps from './components/ComplexProps.vue';
import CustomeValidatorProps from './components/CustomeValidatorProps.vue';
import EventsParent from './components/EventsParent.vue';

const firstName = ref('Shayan');
const lastName = ref('Ahmad');
</script>
<template>
  <HelloWorld />
  <hr />
  <TextInterpolation />
  <hr />
  <AttritubeBinding />
  <hr />
  <GlobalStyle />
  <hr />
  <LocalStyle />
  <hr />
  <ModuleStyle />
  <hr />
  <EventHandler />
  <hr />
  <ReactiveComponent />
  <hr />
  <RefComponent />
  <hr />
  <ComputedPropreties />
  <hr />
  <ConditionalRendering />
  <hr />
  <ItrationComponent />
  <hr />
  <ModelComponent />
  <hr />
  <StaticProps name="Shayan" />
  <hr />
  <DynamicProps :first="firstName" :last="lastName" />
  <hr />
  <ValidtionProps fullName="Shayan Ahmad" :age=20 />
  <hr />
  <ComplexProps :friends="['alex', 'john', 'jordan', 'huxn']"
    :userInfo="{ name: 'alex', age: 20, location: ['Earth', 'IDK'] }" />
  <hr />
  <CustomeValidatorProps name="Shayan" :age="25" password="impossiblePassword" />
  <hr>
  <h1>events are child communicate with parent</h1>
  <EventsParent />
</template>
<style scoped></style>