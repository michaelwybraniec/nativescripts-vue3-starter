<script lang="ts" setup>
import { ref, $navigateBack } from 'nativescript-vue';

function logTapping(source) {
  console.log('tap!', source);
}
function navigateBack(source) {
  logTapping(source);
  $navigateBack();
}
</script>

<template>
  <Page backgroundColor="#519f7d">
    <ActionBar backgroundColor="#f7f7f7">
      <Label text="Funnel" class="text-center text-md text-black"></Label>
    </ActionBar>

    <ContentView
      height="550"
      row="1"
      class="bg-[#529f7d] m-2 rounded-t-3xl rounded-b-3xl"
    >
      <WebView
        height="700"
        class="mt-2"
        src="https://assurance.santevet.com/quote-species?_gl=1%2aiapr8h%2a_ga%2aODE5MzYyOTA3LjE3MDc4MzEyODg.%2a_ga_1RVXB9VC2D%2aMTcwNzgzMTI4OC4xLjEuMTcwNzgzMjk0Mi41OC4wLjA."
      />
    </ContentView>
  </Page>
</template>
