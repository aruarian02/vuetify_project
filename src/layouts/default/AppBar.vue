<template>
  <v-card>
    <v-toolbar color="teal-darken-1">
      <v-tabs v-model="currentItem" fixed-tabs>
        <v-menu v-if="extract.length">
          <template v-slot:activator="{ props }">
            <v-btn class="align-self-center me-4" height="100%" v-bind="props">
              정책판별
              <v-icon end> mdi-menu-down </v-icon>
            </v-btn>
          </template>

          <v-list class="bg-grey-lighten-3">
            <v-list-item v-for="item in extract" :key="item">
              {{ item }}
            </v-list-item>
          </v-list>
        </v-menu>

        <v-menu v-if="manual.length">
          <template v-slot:activator="{ props }">
            <v-btn class="align-self-center me-4" height="100%" v-bind="props">
              정책입력
              <v-icon end> mdi-menu-down </v-icon>
            </v-btn>
          </template>

          <v-list class="bg-grey-lighten-3">
            <v-list-item v-for="item in manual" :key="item">
              {{ item }}
            </v-list-item>
          </v-list>
        </v-menu>

        <v-tab v-for="item in other_menus" :key="item" :value="'tab-' + item">
          {{ item }}
        </v-tab>
        <router-link to="/datatable">
          <v-tab> 아이구 </v-tab>
        </router-link>
      </v-tabs>
      <v-spacer></v-spacer>
      <v-btn append-icon="mdi-logout">
        로그아웃

        <template v-slot:append>
          <v-icon color="warning"></v-icon>
        </template>
      </v-btn>
    </v-toolbar>
  </v-card>
</template>

<script>
export default {
  data: () => ({
    currentItem: "tab-Web",
    extract: ["지자체 판별", "기업마당 판별", "창업넷 판별", "기타기관 판별"],
    manual: ["지자체 입력", "기업마당 입력", "창업넷 입력", "기타기관 입력"],
    other_menus: ["정책자금 검색", "데이터판별", "종료공고"],
  }),
};
</script>
