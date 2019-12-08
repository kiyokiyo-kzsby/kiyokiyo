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
            <v-list-group v-for="(skill,index) in skills" :key="index">
              <template v-slot:activator>
                <v-list-item-title><span class="skill-caption">{{skill.caption}}</span></v-list-item-title>
              </template>
              <v-list-item three-line v-for="(content,index) in skill.contents" :key="index">
                <v-list-item-content>
                  <v-list-item-title>{{content.title}}</v-list-item-title>
                  <v-list-item-subtitle>{{content.description}}</v-list-item-subtitle>
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
      skills: [
        {
          caption: "触ったことある",
          contents: [
            {
              title: "AWS全般",
              description: "Solution Architect Associate 取得しました。"
            },
            {
              title: "ElasticSearch",
              description: "内部構造や形態素解析器の挙動など、少しだけ理解しています。"
            },
            {
              title: "heroku",
              description: "アプリのデプロイ先として一時期利用していました。"
            },
            {
              title: "firebase",
              description: "アプリのデプロイ先として一時期利用していました。firestoreも使用していました。"
            }
          ]
        },
        {
          caption: "完全に理解した",
          contents: [
            {
              title: "Vue.js",
              description: "このページはVue.jsで作られています。"
            },
            {
              title: "flask",
              description: "flaskでブログアプリ作成しました。CRUDとログイン処理は一通り書けます。"
            },
            {
              title: "Docker",
              description: "Webサーバ/Appサーバ/DBサーバを別コンテナで立てて繋げるお遊びをしてました。"
            },
            {
              title: "Amazon S3",
              description: "このWebページのデプロイ先としてS3を使用しています。"
            },
            {
              title: "chrome拡張",
              description: "社内業務を効率化するchrome拡張作りました。"
            },
            {
              title: "selenium",
              description: "社内業務を自動化するアプリケーション作りました。"
            }
          ]
        },
        {
          caption: "なにも分からない",
          contents: [
            {
              title: "AtCoder",
              description: "水色です。"
            }
          ]
        },
        {
          caption: "チョットデキル",
          contents: []
        },
        {
          caption: "やってみたい",
          contents: [
            {
              title: "Kaggle",
              description: "GrandMasterになりたい。"
            },
            {
              title: "CircleCI",
              description: "CI/CD周りできるようになったらかっこよくない？"
            }
          ]
        }
      ]
    }),
  }
</script>

<style scoped>
.skill-caption{
  font-size: 18px;
  font-weight: bold;
}
</style>