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
            <Label text="Welcome to" class="font-bold text-lg" />
          <Label text="space!" class="font-bold text-lg" />
        </StackLayout>
      </ActionBar>
      <StackLayout backgroundColor="#edf3f7" class="px-2">
        <Button
          height="50"
          @tap="navigateTo('>>> Home to Details', Details)"
          class="mt-5 px-4 py-2 bg-white text-black border-2 border-grey-400 rounded-lg"
        >
          Animal list
        </Button>

        <Button
          height="50"
          @tap="navigateTo('>>> Home to Funnel', Funnel)"
          class="px-4 py-2 mt-5 bg-white text-black border-2 border-grey-400 rounded-lg"
        >
          Funnel
        </Button>

        <Button
          height="50"
          @tap="navigateTo('>>> Home to Blog', Blog)"
          class="px-4 py-2 mt-5 bg-white text-black border-2 border-grey-400 rounded-lg"
        >
          Blog
        </Button>
      </StackLayout>
    </Page>
  </Frame>
</template>

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

function logTapping(source) {
  console.log('tap!', source);
}

function navigateTo(source, target) {
  logTapping(source);
  $navigateTo(target);
}

onMounted(() => {
  console.log('mounted');
});

onUnmounted(() => {
  console.log('unmounted');
});
</script>

<style>
  
</style>
