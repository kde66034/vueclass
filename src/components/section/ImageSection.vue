<template>
  <section id="imageType" class="image__wrap scroll" :class="attr">
    <h2>별빛제빵교실 개강 소식🍞</h2>
    <p>
      별빛제빵교실이 올 겨울에 개강합니다. 수강신청 기회는 지금 뿐이니
      서두르세요!
    </p>
    <div class="image__inner" :class="layout">
      <article class="image img1">
        <h3 class="image__title">Class A</h3>
        <p class="image__desc">
          12월 17일부터 23년 3월 18일까지 약 3개월동안 진행되며, 입문자 눈높이에
          맞춰 제빵의 기초에 포커스를 두고 차근차근 수업이 이루어집니다.
        </p>
        <a class="image__btn" href="#" title="자세히 보기"> 자세히 보기 </a>
      </article>
      <article class="image img2">
        <h3 class="image__title">Class B</h3>
        <p class="image__desc">
          12월 22일부터 23년 6월 21일까지 약 6개월동안 진행되며, 베이킹 입문
          제과+제빵 기능사와 실무에서의 기본기, 제조 기술 습득 과정인 디저트
          '올베이직', 케이크디자인 자격증 과정까지 실무 끝판왕 '올마스터' 교육을
          목표로 하는 파티셰 완성 과정입니다.
        </p>
        <a class="image__btn" href="#" title="자세히 보기"> 자세히 보기 </a>
      </article>
    </div>
  </section>
</template>

<script>
  export default {
    props: {
      attr: String,
      layout: String,
    },
  };
</script>

<style>
/* imageType */
#imageType > p {
  font-size: 22px;
  padding: 0 20px;
  word-break: keep-all;
  line-height: 1.6;
}

.image__inner {
  display: flex;
  justify-content: space-between; /* 간격 떨어뜨리기 */
  flex-wrap: wrap;
  width: 100%;
}
.image {
  width: 49%;
  height: 370px;
  padding: 200px 30px 30px 30px;
  color: #fff;
  box-sizing: border-box;
}
.image.img1 {
  background-image: url(../../assets/img/imageType/imageType01_bg01.jpg);
  background-size: cover;
  background-repeat: no-repeat;
  background-position: center;
}
.image.img2 {
  background-image: url(../../assets/img/imageType/imageType01_bg02.jpg);
  background-size: cover;
  background-repeat: no-repeat;
  background-position: center;
}
.image__title {
  font-size: 32px;
  margin-bottom: 10px;
  text-shadow: 0 0 4px rgb(80, 80, 80);
  /* 1줄 */
  overflow: hidden;
  text-overflow: ellipsis;
  white-space: nowrap;
}
.image__desc {
  font-size: 16px;
  line-height: 1.5;
  margin-bottom: 10px;
  font-weight: 300;
  text-shadow: 0 0 4px rgb(80, 80, 80);
  /* 2줄효과 : 글이 넘쳐도 2줄을 넘지 않도록 해줌 */
  overflow: hidden;
  text-overflow: ellipsis;
  display: -webkit-box;
  -webkit-line-clamp: 2;
  -webkit-box-orient: vertical;
  padding-right: 30px;
}
.image__btn {
  background: rgb(80, 80, 80);
  color: #fff;
  padding: 10px 15px;
  font-size: 16px;
  font-weight: 300;
  display: inline-block;
  transition: all 0.3s ease;
}
.image__btn:hover {
  background: #fff;
  color: #000;
}

/* 반응형 */
@media (max-width: 960px) {
  .image__inner .image {
    margin: 0 auto;
    width: 98%;
  }
  .image:first-child {
    margin-bottom: 30px;
  }
  #imageType > h2 {
    font-size: 40px;
  }
  #imageType > p {
    font-size: 18px;
    margin-bottom: 60px;
  }
}

@media (max-width: 600px) {
  #imageType > h2 {
    font-size: 30px;
  }
  #imageType > p {
    font-size: 16px;
    margin-bottom: 50px;
  }
  .image__inner .image {
    width: 96%;
    margin: 0 auto;
    padding: 210px 20px 20px 20px;
  }
  .image:first-child {
    margin-bottom: 20px;
  }
  .image__title {
    font-size: 24px;
  }
}
</style>
