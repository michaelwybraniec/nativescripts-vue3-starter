<script lang="ts" setup>
import { ref, $navigateBack } from 'nativescript-vue';

const items = ref(
  Array(1000)
    .fill(0)
    .map((_, index) => `Item ${index + 1}`)
);
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
        <ListView
          :items="items"
          separatorColor="transparent"
          class="bg-transparent"
        >
          <template #default="{ item }">
            <GridLayout columns="*, auto" class="px-4">
              <Label :text="item" class="text-xl py-4 text-white" />
              <Image
                col="1"
                src="https://icons.duckduckgo.com/ip3/www.santevet.com.ico"
                width="40"
                height="40"
              />
            </GridLayout>
          </template>
        </ListView>
      </ContentView>
    </GridLayout>
  </Page>
</template>
