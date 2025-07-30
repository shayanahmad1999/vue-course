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
import SlotComponent from './components/SlotComponent.vue';
import FallbackContent from './components/FallbackContent.vue';
import NamedSlot from './components/NamedSlot.vue';

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
  <hr />
  <SlotComponent>
    <h1>Content 1</h1>
    <h2>Content 2</h2>
    <h3>Content 3</h3>
  </SlotComponent>
  <hr />
  <FallbackContent>
    <!-- <p>Fallback will not work because I'm providing content inside the component</p> -->
  </FallbackContent>
  <hr />
  <NamedSlot>
    <!-- v-slot:nameOfSlot -->
    <template v-slot:one>
      <h1>This Content will go to slot "one"</h1>
    </template>

    <template v-slot:two>
      <h1>This Content will go to slot "two"</h1>
    </template>
  </NamedSlot>
  <DefaultSlot>
    <template #default>
      <h1>this is some random content for default slot.</h1>
    </template>
  </DefaultSlot>
</template>
<style scoped></style>