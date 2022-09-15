<template>
  <div class="bana-container">
    <!-- 헤더 S -->
    <header id="header">
      <div class="bana-container2 header-container">
        <h3 class="logo">
          <router-link to="/bana">
            <img src="@/assets/images/bana/bana_header_logo_img.png" alt="bana header logo">
          </router-link>
        </h3>
        <ul class="header-nav">
          <li v-for="(list, idx) in navList" :key="'navList' + idx"><a href="#">{{list.name}}</a></li>
        </ul>
      </div>
    </header>
    <!-- 헤더 E -->
    <!-- 메인 S -->
    <main id="main" class="main-img">
      <div class="bana-container2"></div>
    </main>
    <!-- 메인 E -->
    <section><div class="bana-container2">2</div></section>
    <section><div class="bana-container2">2</div></section>
    <section><div class="bana-container2">2</div></section>
    <section><div class="bana-container2">2</div></section>
    <footer><div class="bana-container2">2</div></footer>
  </div>  
</template>

<script>
export default {
  data() {
    return {
      navList: [
        {
          name: '바나프레소 소개'
        },
        {
          name: '메뉴 리스트'
        },
        {
          name: '매장 안내'
        },
        {
          name: '소식'
        },
        {
          name: '채용'
        },
        {
          name: '입점제안'
        },
        {
          name: '가맹점 문의'
        },
        {
          name: '멀티링크'
        }
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
// 바나 메인 컬러 #fcd9dd
$mainColor:#fcd9dd;

ul, li {
  list-style: none;
  margin: 0;
  padding: 0;
}

a, a:focus, a:hover {
  text-decoration: none;
  color: #000;
}

.bana-container {
  width: 100%;
  display: grid;
  grid-auto-rows: 70px auto auto auto auto auto 100px;
  overflow: auto;

  #header {
    position: sticky;
    top: 0;
    border-bottom: 1px solid #ededed;
    background: rgba(255,255,255,0.8);
    .header-container {
      display: flex;
      justify-content: space-between;
      align-items: center;
      .logo {
        width: 200px;
      }
      .header-nav {
        width: calc(100% - 250px);
        display: flex;
        justify-content: space-around;
        align-items: center;
        a {
          transition: border-bottom 0.1s ease-in-out;
        }
        a:hover {
          color: #f1648a;
          border-bottom: 1px solid #f1648a;
          font-weight: bold;
        }
      }
    }
  }
  #main {
    min-height: 800px;
    // background: $mainColor;
  }
  section {
    height: 600px;
    background: #fff;
  }
  footer {
    border-top: 1px solid #ededed;
    background: #fff;
  }
  .bana-container2 {
    width: 1200px;
    height: 100%;
    margin: 0 auto;
  }
  .main-img {
    background: $mainColor url(@/assets/images/bana/bana_main_img.PNG) no-repeat center / contain;
  }
}

@media screen and (max-width: 1250px) {
  .bana-container {
    .bana-container2 {
      width: 100%;
      padding: 0 20px;
    }
  }
}
</style>