<template lang="html">
  <Frame>
    <Page>
      <ActionBar backgroundColor="#f7f7f7">
        <StackLayout orientation="horizontal">
          <Image
            src="https://cdn.cookielaw.org/logos/d55a1ac7-091c-4ec1-b143-bee746dded5b/12d5690a-2784-4f03-9fc1-081d698ceeb6/d6f59c31-74f5-4b19-a17e-6e8c13c15c62/Logo_Sant%C3%A9vet_RVB_-_No_baseline.png"
            width="140"
            verticalAlignment="center"
            class="pb-5"
          />
        </StackLayout>
      </ActionBar>
      <TabView androidTabsPosition="bottom" tabBackgroundColor="white" selectedTabTextColor="black">
        <TabViewItem title="Mes demandes" iconSource="~/images/request.png">
          <Frame id="requests">
            <Requests />
          </Frame>
        </TabViewItem>

        <TabViewItem title="Mes animaux" iconSource="~/images/pawprint.png">
          <Frame id="blog">
            <Blog />
          </Frame>
        </TabViewItem>

        <TabViewItem title="Urgencies" iconSource="~/images/siren.png">
          <Frame id="funnel">
            <Funnel />
          </Frame>
        </TabViewItem>

         <TabViewItem title="Mon compte" iconSource="~/images/user.png">
          <Frame id="account">
            <Account />
          </Frame>
        </TabViewItem>

      </TabView>
    </Page>
  </Frame>
</template>

<script>
import Requests from './Requests.vue';
import Blog from './Blog.vue';
import Funnel from './Funnel.vue';
import Account from './Account.vue';



export default {
  components: {
    Requests,
    Blog,
    Funnel,
    Account
  }
};
</script>

<style lang="scss"></style>
