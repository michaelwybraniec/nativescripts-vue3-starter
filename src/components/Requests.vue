<template>
  <Page>
    <ActionBar backgroundColor="#f7f7f7">
      <Label text="Demandes" class="text-center text-md text-black"></Label>
    </ActionBar>

    <ListView for="item in items" @itemTap="onItemTap" backgroundColor="#f7f7f7">
      <v-template>
        <StackLayout orientation="horizontal" class="px-2">
          <Label :text="item.name" textWrap="true"></Label>
        </StackLayout>
      </v-template>
    </ListView>
  </Page>
</template>

<script>

export default {
  data() {
    return {
      items: [
        {
          name: 'Item 1',
          description: 'Description for Item 1'
        },
        {
          name: 'Item 2',
          description: 'Description for Item 2'
        },
        {
          name: 'Item 3',
          description: 'Description for Item 3'
        },
        {
          name: 'Item 4',
          description: 'Description for Item 4'
        },
        {
          name: 'Item 5',
          description: 'Description for Item 5'
        },
        {
          name: 'Item 6',
          description: 'Description for Item 6'
        },
        {
          name: 'Item 7',
          description: 'Description for Item 7'
        },
        {
          name: 'Item 8',
          description: 'Description for Item 8'
        },
        {
          name: 'Item 9',
          description: 'Description for Item 9'
        },
        {
          name: 'Item 10',
          description: 'Description for Item 10'
        },
        {
          name: 'Item 11',
          description: 'Description for Item 11'
        },
        {
          name: 'Item 12',
          description: 'Description for Item 12'
        },
        {
          name: 'Item 13',
          description: 'Description for Item 13'
        },
        {
          name: 'Item 14',
          description: 'Description for Item 14'
        },
        {
          name: 'Item 15',
          description: 'Description for Item 15'
        },
        {
          name: 'Item 16',
          description: 'Description for Item 16'
        }
      ]
    };
  },
  methods: {
    onItemTap(args) {
      this.$navigateTo(ItemDetails, {
        frame: 'items',
        props: { item: args.item },
        animated: true,
        transition: {
          name: 'slide',
          duration: 200,
          curve: 'ease'
        }
      });
    }
  }
};
</script>

<style scoped lang="scss"></style>
