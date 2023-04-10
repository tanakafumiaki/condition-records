<template>
  <v-app>
    <!-- サイドメニュー -->
    <v-navigation-drawer app clipped v-model="drawer" dark color="info">
    </v-navigation-drawer>

    <!-- ヘッダー -->
    <v-app-bar app clippedLeft flat dark color="indigo darken-3">
      <v-app-bar-nav-icon @click.stop="drawer=!drawer" color="info"></v-app-bar-nav-icon>
    </v-app-bar>

    <!-- メイン -->
    <v-main>
      <v-container fluid>
        <v-card>
          <v-tabs
            v-model="tab"
            bg-color="primary"
          >
            <v-tab value="one">Item One</v-tab>
            <v-tab value="two">Item Two</v-tab>
            <v-tab value="three">Item Three</v-tab>
          </v-tabs>
      
          <v-card-text>
            <v-window v-model="tab">
              <v-window-item value="one">
                <div v-on:click="hello">
                  <PrimaryButton/>
                </div>
              </v-window-item>
      
              <v-window-item value="two">
                 <DataTable/>
              </v-window-item>
      
              <v-window-item value="three">
                Three
              </v-window-item>
            </v-window>
          </v-card-text>
        </v-card>
      </v-container>
    </v-main>

    <!-- フッター -->
    <v-footer app color="primary">
    </v-footer>
  </v-app>
</template>

<script>
import PrimaryButton from '@/components/atoms/buttons/primary_button.vue'
import DataTable from '@/components/module/data_table.vue'
export default {
  name: 'HelloWorld',
  components: {
    PrimaryButton,
    DataTable,
  },
  data(){
    return{
      drawer: false,
      model: null,
      tabNum: 'one',
      tab: null,
    }
  },
  mounted () {
    
  },
  methods: {
    hello () {
      console.log("Hello World!");
    },
    clickTab(value) {
      console.log(value);
      this.tabNum=value;
      console.log(this.tabNum);

    },
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}

</style>