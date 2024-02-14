<script lang="ts" setup>
import {
  ref,
  computed,
  onMounted,
  onUnmounted,
  $navigateTo
} from 'nativescript-vue';
import Details from './Details.vue';
import Funnel from './Funnel.vue';
import Blog from './Blog.vue';

const counter = ref(0);
// const message = computed(() => {
//   return `Spam counter: ${counter.value}`;
// });

function logMessage() {
  console.log('Tap!');
}

let interval: any;
onMounted(() => {
  console.log('mounted');
  interval = setInterval(() => counter.value++, 100);
});

onUnmounted(() => {
  console.log('unmounted');
  clearInterval(interval);
});
</script>

<template>
  <Frame>
    <Page>
      <ActionBar>
        <StackLayout orientation="horizontal">
          <Label text="Welcome to" class="font-bold text-lg" />
          <Image
            src="https://icons.duckduckgo.com/ip3/www.santevet.com.ico"
            width="40"
            height="40"
            verticalAlignment="center"
          />
          <Label text="space!" class="font-bold text-lg" />
        </StackLayout>
      </ActionBar>
      <StackLayout backgroundColor="#edf3f7" class="px-2">
        <!-- <Label
          height="70"
          class="text-xl align-middle text-center text-gray-500"
          :text="message"
          @tap="logMessage"
        /> -->
        <Button
          height="50"
          @tap="$navigateTo(Details)"
          class="px-4 py-2 bg-white text-black border-2 border-grey-400 rounded-lg"
          @tap="logMessage"
        >
          Animal list
        </Button>

        <Button
          height="50"
          @tap="$navigateTo(Funnel)"
          class="px-4 py-2 mt-5 bg-white text-black border-2 border-grey-400 rounded-lg"
        >
          Funnel
        </Button>

        <Button
          height="50"
          @tap="$navigateTo(Blog)"
          class="px-4 py-2 mt-5 bg-white text-black border-2 border-grey-400 rounded-lg"
        >
          Blog
        </Button>
      </StackLayout>
    </Page>
  </Frame>
</template>

<style>
/* .info {
    font-size: 20;
  } */
</style>
