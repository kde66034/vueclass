<template>
  <section id="bannerType" class="banner__wrap scroll" :class="attr">
    <h2 class="blind">배너 영역</h2>
    <div class="banner__inner">
      <h3 class="title">김제빵 유튜브</h3>
      <p class="desc">
        별빛제빵교실 유명 강사 김제빵의 유튜브 채널입니다!
        <a
          href="https://www.youtube.com/c/CozyRain"
          title="유튜브 페이지로 이동"
          >https://www.youtube.com/c/kim_baking</a
        >
      </p>
    </div>
  </section>
</template>

<script>
  export default {
    props: {
      attr: String,
    },
  };
</script>

<style>
/* bannerType */
.banner__inner {
  background-image: url(../../assets/img/bannerType/banner_bg01.jpg);
  background-repeat: no-repeat;
  background-position: center;
  background-size: cover;
  text-align: center;
  padding: 120px 0;
  color: #fff;
}
.banner__inner .title {
  font-size: 50px;
  line-height: 1;
  font-weight: 300;
  margin-bottom: 40px;
}
.banner__inner .desc {
  font-size: 24px;
  line-height: 1.5;
  font-weight: 300;
}
.banner__inner .desc a {
  color: #fff;
  display: block;
}
.banner__inner .desc a:hover {
  text-decoration: underline;
}
.banner__inner .small {
  font-size: 16px;
  text-decoration: underline;
}

@media (max-width: 960px) {
  .banner__inner {
    padding: 100px 0;
  }
  .banner__inner .title {
    font-size: 40px;
  }
  .banner__inner .desc {
    font-size: 18px;
  }
}

@media (max-width: 600px) {
  .banner__inner {
    padding: 80px 0;
  }
  .banner__inner .title {
    font-size: 30px;
    margin-bottom: 20px;
  }
  .banner__inner .desc {
    font-size: 16px;
  }
}
</style>
