<script lang="ts" setup>
import { ref, $navigateBack } from 'nativescript-vue';
</script>

<template>
  <Page actionBarHidden="true">
    <GridLayout rows="auto, *">
      <Label
        text="Go Back"
        @tap="$navigateBack"
        class="text-center px-2 py-5 text-md text-gray-200 font-bold"
      />

      <ContentView row="1" class="bg-[#529f7d] rounded-t-3xl">
        <WebView
          height="700"
          class="mt-2"
          src="https://www.santevet.com/blog"
        />
      </ContentView>
    </GridLayout>
  </Page>
</template>
