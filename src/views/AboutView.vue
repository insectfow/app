<template>
  <div class="about">
    <h1>믹스마스터 코어리스트</h1>
    <div class="mix-wrap">
      <div
        class="mix-list"
        v-for="list in list.demon"
        :key="'mix-list' + list.idx"
      >
        <p>{{ list }}</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      list: {
        demon: [
          {
            idx: 1,
            name: "데빌코",
            level: 1,
            maxLevel: 26,
            get: true,
            excited: false,
            range: "short",
            mixList: [],
          },
          {
            idx: 2,
            name: "루루삐",
            level: 3,
            maxLevel: 28,
            get: true,
            excited: false,
            range: "short",
            mixList: [
              {
                left: "데빌코",
                right: "드라코",
              },
            ],
          },
          {
            idx: 3,
            name: "베베",
            level: 5,
            maxLevel: 30,
            get: true,
            excited: false,
            range: "short",
            mixList: [
              {
                left: "데빌코",
                right: "카임",
              },
              {
                left: "데빌코",
                right: "플라코",
              },
              {
                left: "루루삐",
                right: "데빌코",
              },
              {
                left: "루루삐",
                right: "버그코",
              },
            ],
          },
          {
            idx: 4,
            name: "부마",
            level: 7,
            maxLevel: 32,
            get: true,
            excited: false,
            range: "short",
            mixList: [
              {
                left: "데빌코",
                right: "푸란",
              },
            ],
          },
          {
            idx: 5,
            name: "아그작데빌",
            level: 9,
            maxLevel: 34,
            get: true,
            excited: false,
            range: "short",
            mixList: [
              {
                left: "데빌코",
                right: "떡충",
              },
              {
                left: "데빌코",
                right: "팅팅",
              },
              {
                left: "루루삐",
                right: "비이스",
              },
              {
                left: "루루삐",
                right: "카임",
              },
              {
                left: "베베",
                right: "펭귄새",
              },
            ],
          },
          {
            idx: 6,
            name: "아그작데빌",
            level: 9,
            maxLevel: 34,
            get: true,
            excited: false,
            range: "short",
            mixList: [
              {
                left: "데빌코",
                right: "떡충",
              },
              {
                left: "데빌코",
                right: "팅팅",
              },
              {
                left: "루루삐",
                right: "비이스",
              },
              {
                left: "루루삐",
                right: "카임",
              },
              {
                left: "베베",
                right: "펭귄새",
              },
            ],
          },
        ],
      },
    };
  },
};
</script>
<style>
.mix-wrap {
  width: 1200px;
}
</style>
