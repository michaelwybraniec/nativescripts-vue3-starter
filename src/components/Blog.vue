<script lang="ts" setup>
import { ref, $navigateBack } from 'nativescript-vue';
</script>

<template>
  <Page backgroundColor="#519f7d">
    <ActionBar backgroundColor="#f7f7f7">
      <Label text="Blog" class="text-center text-md text-black"></Label>
    </ActionBar>

    <ContentView height="550" row="1" class="bg-[#529f7d] m-2 rounded-t-3xl rounded-b-3xl">
      <WebView  src="https://www.santevet.com/blog" />
    </ContentView>
  </Page>
</template>
