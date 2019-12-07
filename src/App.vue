<template>
  <v-app id="inspire">
    <v-app-bar
      :clipped-left="$vuetify.breakpoint.lgAndUp"
      app
      color="blue darken-3"
      dark
    >
      <v-toolbar-title
        style="width: 300px"
        class="ml-0 pl-4"
      >
        <span>きよきよポータル</span>
      </v-toolbar-title>
    </v-app-bar>

    <v-content>
      <v-container
        fluid
      >
        <v-row
          align="start"
          justify="center"
        >
          <v-col cols="5" sm="2">
            <v-img src="@/assets/kiyokiyo.jpg" max-width="120px"></v-img>
          </v-col>
          <v-col cols="7" sm="8" pa-xs-2 pa-sm-3>
            <h1>きよきよ</h1>
            <p>Software Engineer / IT Consultant</p>
            <div>
              <v-tooltip right>
                <template v-slot:activator="{ on }">
                  <v-btn
                    icon
                    large
                    href="https://kiyokiyo-kzsby.hatenablog.com/"
                    target="_blank"
                    v-on="on"
                  >
                    <v-avatar
                      size="32px"
                      item
                    ><v-img src="@/assets/hatenablog-icon.png"></v-img></v-avatar>
                  </v-btn>
                </template>
                <span>Hatena Blog</span>
              </v-tooltip>
              <v-tooltip right>
                <template v-slot:activator="{ on }">
                  <v-btn
                    icon
                    large
                    href="https://qiita.com/kiyokiyo_kzsby"
                    target="_blank"
                    v-on="on"
                  >
                    <v-avatar
                      size="32px"
                      item
                    ><v-img src="@/assets/qiita-favicon.png"></v-img></v-avatar>
                  </v-btn>
                </template>
                <span>Qiita</span>
              </v-tooltip>
              <v-tooltip right>
                <template v-slot:activator="{ on }">
                  <v-btn
                    icon
                    large
                    href="https://github.com/kiyokiyo-kzsby"
                    target="_blank"
                    v-on="on"
                  >
                    <v-icon large color="black">mdi-github-circle</v-icon>
                  </v-btn>
                </template>
                <span>GitHub</span>
              </v-tooltip>
              <v-tooltip right>
                <template v-slot:activator="{ on }">
                  <v-btn
                    icon
                    large
                    href="https://twitter.com/kiyokiyo_kzsby"
                    target="_blank"
                    v-on="on"
                  >
                    <v-icon color="blue" large>mdi-twitter</v-icon>
                  </v-btn>
                </template>
                <span>Twitter</span>
              </v-tooltip>
            </div>
          </v-col>
        </v-row>
        <v-row
          align="center"
          justify="center"
        >
          <v-col cols="12" sm="10">
            <v-list-group>
              <template v-slot:activator>
                <v-list-item-title><span class="skill-category">完全に理解した</span></v-list-item-title>
              </template>
              <v-list-item three-line>
                <v-list-item-content>
                  <v-list-item-title>Vue.js</v-list-item-title>
                  <v-list-item-subtitle>このページはVue.jsで作られています。</v-list-item-subtitle>
                </v-list-item-content>
              </v-list-item>
              <v-list-item three-line>
                <v-list-item-content>
                  <v-list-item-title>AWS</v-list-item-title>
                  <v-list-item-subtitle>Solution Architect Associate 取得しました。</v-list-item-subtitle>
                </v-list-item-content>
              </v-list-item>
              <v-list-item three-line>
                <v-list-item-content>
                  <v-list-item-title>Docker</v-list-item-title>
                  <v-list-item-subtitle>Webサーバ/Appサーバ/DBサーバを別コンテナで立てて繋げるお遊びをしてました。</v-list-item-subtitle>
                </v-list-item-content>
              </v-list-item>
            </v-list-group>
            <v-list-group>
              <template v-slot:activator>
                <v-list-item-title><span class="skill-category">なにも分からない</span></v-list-item-title>
              </template>
              <v-list-item three-line>
                <v-list-item-content>
                  <v-list-item-title>AtCoder</v-list-item-title>
                  <v-list-item-subtitle>水色です。</v-list-item-subtitle>
                </v-list-item-content>
              </v-list-item>
            </v-list-group>
            <v-list-group>
              <template v-slot:activator>
                <v-list-item-title><span class="skill-category">チョットデキル</span></v-list-item-title>
              </template>
              <v-list-item>
                <v-list-item-content>
                  <v-list-item-title>Nothing</v-list-item-title>
                </v-list-item-content>
              </v-list-item>
            </v-list-group>
            <v-list-group>
              <template v-slot:activator>
                <v-list-item-title><span class="skill-category">やってみたい</span></v-list-item-title>
              </template>
              <v-list-item three-line>
                <v-list-item-content>
                  <v-list-item-title>Kaggle</v-list-item-title>
                  <v-list-item-subtitle>GrandMasterになりたい。</v-list-item-subtitle>
                </v-list-item-content>
              </v-list-item>
              <v-list-item three-line>
                <v-list-item-content>
                  <v-list-item-title>CircleCI</v-list-item-title>
                  <v-list-item-subtitle>CI/CD周りできるようになったらかっこよくない？</v-list-item-subtitle>
                </v-list-item-content>
              </v-list-item>
            </v-list-group>
          </v-col>
        </v-row>
      </v-container>
    </v-content>

  </v-app>
</template>

<script>
  export default {
    data: () => ({
      dialog: false,
      drawer: null,
      items: [
        { icon: 'contacts', text: 'Contacts' },
        { icon: 'history', text: 'Frequently contacted' },
        { icon: 'content_copy', text: 'Duplicates' },
        {
          icon: 'keyboard_arrow_up',
          'icon-alt': 'keyboard_arrow_down',
          text: 'Labels',
          model: true,
          children: [
            { icon: 'add', text: 'Create label' },
          ],
        },
        {
          icon: 'keyboard_arrow_up',
          'icon-alt': 'keyboard_arrow_down',
          text: 'More',
          model: false,
          children: [
            { text: 'Import' },
            { text: 'Export' },
            { text: 'Print' },
            { text: 'Undo changes' },
            { text: 'Other contacts' },
          ],
        },
        { icon: 'settings', text: 'Settings' },
        { icon: 'chat_bubble', text: 'Send feedback' },
        { icon: 'help', text: 'Help' },
        { icon: 'phonelink', text: 'App downloads' },
        { icon: 'keyboard', text: 'Go to the old version' },
      ],
    }),
  }
</script>

<style scoped>
.skill-category{
  font-size: 18px;
  font-weight: bold;
}
</style>