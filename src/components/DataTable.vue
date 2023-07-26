<template>
  <v-card>
    <v-card-title>
      Nutrition
      <v-spacer></v-spacer>
      <v-text-field
        v-model="search"
        append-icon="mdi-magnify"
        label="Search"
        single-line
        hide-details
      ></v-text-field>
    </v-card-title>

    <v-data-table
      :headers="headers"
      :items="dummies"
      :search="search"
      show-select
    >
      <template v-slot:[`header.data-table-select`]="{ props, on }">
        <v-simple-checkbox
          :value="props.value || props.indeterminate"
          v-on="on"
          :indeterminate="props.indeterminate"
          color="primary"
        />
      </template>
    </v-data-table>
  </v-card>
</template>
<script>
import { VDataTable } from "vuetify/lib/labs/components.mjs";

export default {
  data() {
    return {
      search: "",
      headers: [
        {
          align: "start",
          key: "siteCat",
          sortable: false,
          title: "카테고리",
        },
        { key: "siteSeq", title: "순번" },

        { key: "name", title: "기관명" },
        { key: "title", title: "제목" },
        { key: "id", title: "아이디" },
        { key: "scrpDateTime", title: "수집일시" },
        { key: "no", title: "정책판별" },
      ],
      dummies: [
        {
          siteCat: "지자체",
          siteSeq: 145,
          id: "31359",
          title: "2023년 충북 일류벤처기업 선정 공고",
          scrpDateTime: "2023/07/22 12:30:57",
          newYn: null,
          name: "충청북도청",
          pbanncIdKey: null,
          startPageNo: 0,
          minPageNo: 0,
          maxPageNo: 0,
          curPageNo: 0,
        },
        {
          siteCat: "지자체",
          siteSeq: 145,
          id: "31356",
          title: "2023년 충청북도 자랑스러운 직업인 선정 공고",
          scrpDateTime: "2023/07/14 12:30:57",
          newYn: null,
          name: "충청북도청",
          pbanncIdKey: null,
          startPageNo: 0,
          minPageNo: 0,
          maxPageNo: 0,
          curPageNo: 0,
        },
        {
          siteCat: "지자체",
          siteSeq: 145,
          id: "31314",
          title: "종합검사 지정정비사업자 지정 공고",
          scrpDateTime: "2023/07/06 12:30:57",
          newYn: null,
          name: "충청북도청",
          pbanncIdKey: null,
          startPageNo: 0,
          minPageNo: 0,
          maxPageNo: 0,
          curPageNo: 0,
        },
        {
          siteCat: "지자체",
          siteSeq: 145,
          id: "31289",
          title: "2023년 양성평등주간사업 시행 재공고",
          scrpDateTime: "2023/06/30 12:30:57",
          newYn: null,
          name: "충청북도청",
          pbanncIdKey: null,
          startPageNo: 0,
          minPageNo: 0,
          maxPageNo: 0,
          curPageNo: 0,
        },
        {
          siteCat: "지자체",
          siteSeq: 145,
          id: "31278",
          title: "제2기 충청북도 재난심리회복지원단 단원 모집 공고",
          scrpDateTime: "2023/06/28 12:30:56",
          newYn: null,
          name: "충청북도청",
          pbanncIdKey: null,
          startPageNo: 0,
          minPageNo: 0,
          maxPageNo: 0,
          curPageNo: 0,
        },
        {
          siteCat: "지자체",
          siteSeq: 145,
          id: "31270",
          title:
            "충북혁신도시 공공기관 연관산업 기업유치 등 지원사업(2분기) 공고",
          scrpDateTime: "2023/06/28 12:30:56",
          newYn: null,
          name: "충청북도청",
          pbanncIdKey: null,
          startPageNo: 0,
          minPageNo: 0,
          maxPageNo: 0,
          curPageNo: 0,
        },
        {
          siteCat: "지자체",
          siteSeq: 145,
          id: "31261",
          title: "제17회 충북우수시장박람회 설치·운영 제안 모집 재공고",
          scrpDateTime: "2023/06/23 12:30:56",
          newYn: null,
          name: "충청북도청",
          pbanncIdKey: null,
          startPageNo: 0,
          minPageNo: 0,
          maxPageNo: 0,
          curPageNo: 0,
        },
        {
          siteCat: "지자체",
          siteSeq: 145,
          id: "31231",
          title:
            "2023년도 하반기 충청북도 수렵면허시험 장소 및 응시자 준수사항 공고",
          scrpDateTime: "2023/06/21 12:30:56",
          newYn: null,
          name: "충청북도청",
          pbanncIdKey: null,
          startPageNo: 0,
          minPageNo: 0,
          maxPageNo: 0,
          curPageNo: 0,
        },
        {
          siteCat: "지자체",
          siteSeq: 145,
          id: "31209",
          title: "충북 지역특화형 비자 시범사업 지역우수인재 모집 공고",
          scrpDateTime: "2023/06/19 12:30:57",
          newYn: null,
          name: "충청북도청",
          pbanncIdKey: null,
          startPageNo: 0,
          minPageNo: 0,
          maxPageNo: 0,
          curPageNo: 0,
        },
        {
          siteCat: "지자체",
          siteSeq: 145,
          id: "31189",
          title: "제천시 택시 자율감차 계획(변경)",
          scrpDateTime: "2023/06/16 12:30:57",
          newYn: null,
          name: "충청북도청",
          pbanncIdKey: null,
          startPageNo: 0,
          minPageNo: 0,
          maxPageNo: 0,
          curPageNo: 0,
        },
        {
          siteCat: "지자체",
          siteSeq: 145,
          id: "31153",
          title: "2023년 충청북도 명장 선정 계획 공고",
          scrpDateTime: "2023/06/16 12:30:57",
          newYn: null,
          name: "충청북도청",
          pbanncIdKey: null,
          startPageNo: 0,
          minPageNo: 0,
          maxPageNo: 0,
          curPageNo: 0,
        },
      ],
    };
  },
  components: {
    VDataTable,
  },
};
</script>
