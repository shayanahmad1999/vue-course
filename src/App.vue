<script setup>
import { provide, ref } from 'vue';
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
import SchoolComponent from './components/SchoolComponent.vue';
import PracticeComponent from './components/PracticeComponent.vue';
import LifeCycle from './components/LifeCycle.vue';
import BasicCpmponent from './components/BasicCpmponent.vue';
import ReactiveObject from './components/ReactiveObject.vue';
import MultipleSource from './components/MultipleSource.vue';
import BasicTemplateRef from './components/BasicTemplateRef.vue';
import FunctionTemplateRef from './components/FunctionTemplateRef.vue';
import TemplateRefComponent1 from './components/TemplateRefComponent1.vue';
import ToggleFriends from './components/ToggleFriends.vue';
import CounterCompoent from './components/CounterCompoent.vue';

const firstName = ref('Shayan');
const lastName = ref('Ahmad');

// working on prvide and inject
// -- this is hardcode to pass data to actual component using props
// ---- in which from parent component to its child and from his child to its grandchild
//  ------ means data passed to nested child component from paren component

// <!-- const name = "shayan";
// const age = 25;
// const location = ['Pakistan', 'IDK']; --> //

// by using provide and inject
// -- it is very easy to passed data from parent to its nested child any where

provide('name', "shayan");
provide('age', 25);
provide('location', ['Pakistan', 'IDK']);


// Using Provide With Array
provide('friends', ['Alex', 'Jordan', 'HuXn', 'John'])

// Using Provide With Object
provide('games', {
  id: 1,
  title: 'Epic Adventure Game',
  genre: ['Action', 'Adventure', 'RPG'],
  platform: ['PC', 'PlayStation', 'Xbox', 'Nintendo Switch'],
  releaseDate: '2022-03-15',
  developer: {
    name: 'Awesome Game Studios',
    location: 'San Francisco, CA',
    teamSize: 50
  }
})

// Using Provide With Array Of Objects
provide('moreGames', [
  {
    title: 'Space Explorer',
    genre: 'Sci-Fi',
    platform: 'PC',
    releaseDate: '2023-05-20'
  },
  {
    title: 'Fantasy Quest',
    genre: 'Fantasy',
    platform: 'PlayStation',
    releaseDate: '2023-07-10'
  },
  {
    title: 'Inception',
    director: 'Christopher Nolan',
    genre: 'Sci-Fi',
    releaseDate: '2010-07-16'
  },
  {
    title: 'The Shawshank Redemption',
    director: 'Frank Darabont',
    genre: 'Drama',
    releaseDate: '1994-09-23'
  }
]);

let showHideComponent = ref(true);
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
  <hr />
  <h1>Provide & inject</h1>
  <!-- <SchoolComponent :name="name" :age="age" :location="location" /> -->
  <SchoolComponent />
  <hr />
  <PracticeComponent />
  <hr />
  <LifeCycle v-if="showHideComponent" />
  <button @click="showHideComponent = !showHideComponent">Show / Hide</button>
  <hr />
  <BasicCpmponent />
  <ReactiveObject />
  <MultipleSource />
  <hr />
  <BasicTemplateRef />
  <FunctionTemplateRef />
  <TemplateRefComponent1 />
  <hr />
  <ToggleFriends />
  <hr />
  <CounterCompoent />
</template>
<style scoped></style>