<template>
  <section id="cardType" class="card__wrap scroll" :class="attr">
    <h2>과정 소개</h2>
    <p>
      기초 과정부터 심화 과정까지, 그리고 나만의 제빵 포트폴리오를 만들기까지의
      과정을 소개합니다.
    </p>
    <div class="card__inner">
      <article class="card">
        <!-- 이미지 넣을 때 그냥 img태그 쓰지말고 figure 태그 안에 넣어서 써야 웹표준 준수한거임 -->
        <figure class="card__header">
          <img src="../../assets/img/cardType/card_bg01.jpg" alt="제빵 기초 강의" />
        </figure>
        <div class="card__body">
          <h3 class="title">제빵 기초 강의</h3>
          <p class="desc">
            제빵의 기초가 되는 강의입니다. 초심자도 이해하기 쉽게 강의가
            진행되며 초반에는 이론 강의부터 시작해 중반부터는 실습을 시작하여
            제빵의 기초를 익히도록 합니다.
          </p>
          <a class="btn" href="#">
            더 자세히 보기
            <span aria-hidden="true">
              <!-- 시각장애인용 스크린리더기가 필요없는 부분을 읽지 못하도록 막아주는 기능 -->
              <svg
                width="65"
                height="8"
                viewBox="0 0 65 8"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  d="M64.3536 4.35355C64.5488 4.15829 64.5488 3.84171 64.3536 3.64645L61.1716 0.464466C60.9763 0.269204 60.6597 0.269204 60.4645 0.464466C60.2692 0.659728 60.2692 0.976311 60.4645 1.17157L63.2929 4L60.4645 6.82843C60.2692 7.02369 60.2692 7.34027 60.4645 7.53553C60.6597 7.7308 60.9763 7.7308 61.1716 7.53553L64.3536 4.35355ZM0 4.5H64V3.5H0V4.5Z"
                  fill="black"
                />
              </svg>
            </span>
          </a>
        </div>
      </article>
      <article class="card">
        <figure class="card__header">
          <img src="../../assets/img/cardType/card_bg02.jpg" alt="제빵 심화 과정" />
        </figure>
        <div class="card__body">
          <h3 class="title">제빵 심화 과정</h3>
          <p class="desc">
            이제 기초 강의가 너무 쉬워 시시하다고 느껴질 즈음 심화과정에
            들어가게 될 겁니다. 시중에 판매되고 있는 제과점 빵들을 직접
            만들어보는 시간을 갖게 됩니다.
          </p>
          <a class="btn" href="#">
            더 자세히 보기
            <span aria-hidden="true">
              <svg
                width="65"
                height="8"
                viewBox="0 0 65 8"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  d="M64.3536 4.35355C64.5488 4.15829 64.5488 3.84171 64.3536 3.64645L61.1716 0.464466C60.9763 0.269204 60.6597 0.269204 60.4645 0.464466C60.2692 0.659728 60.2692 0.976311 60.4645 1.17157L63.2929 4L60.4645 6.82843C60.2692 7.02369 60.2692 7.34027 60.4645 7.53553C60.6597 7.7308 60.9763 7.7308 61.1716 7.53553L64.3536 4.35355ZM0 4.5H64V3.5H0V4.5Z"
                  fill="black"
                />
              </svg>
            </span>
          </a>
        </div>
      </article>
      <article class="card">
        <figure class="card__header">
          <img
            src="../../assets/img/cardType/card_bg03.jpg"
            alt="나만의 제빵 포트폴리오 만들기"
          />
        </figure>
        <div class="card__body">
          <h3 class="title">나만의 제빵 포트폴리오 만들기</h3>
          <p class="desc">
            이제 빵집 창업해도 문제 없을 정도의 실력을 갖추게 되셨을 겁니다!
            이제는 능숙해진 제빵 실력에 나만의 개성을 더하여 튼튼한 포트폴리오를
            만들어보아요!
          </p>
          <a class="btn" href="#">
            더 자세히 보기
            <span aria-hidden="true">
              <svg
                width="65"
                height="8"
                viewBox="0 0 65 8"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  d="M64.3536 4.35355C64.5488 4.15829 64.5488 3.84171 64.3536 3.64645L61.1716 0.464466C60.9763 0.269204 60.6597 0.269204 60.4645 0.464466C60.2692 0.659728 60.2692 0.976311 60.4645 1.17157L63.2929 4L60.4645 6.82843C60.2692 7.02369 60.2692 7.34027 60.4645 7.53553C60.6597 7.7308 60.9763 7.7308 61.1716 7.53553L64.3536 4.35355ZM0 4.5H64V3.5H0V4.5Z"
                  fill="black"
                />
              </svg>
            </span>
          </a>
        </div>
      </article>
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
/* cardType */
.card__inner {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between; /* 간격 떨어뜨리기 */
}
.card {
  width: 32%;
  background: #fff;
}
.card__body {
  padding: 24px;
  background: #f5f5f5;
}
.card__body .title {
  font-size: 22px;
  padding-bottom: 10px;
  /* 한 줄 효과 */
  overflow: hidden;
  white-space: nowrap;
  text-overflow: ellipsis;
  padding-right: 30px; /* 제목 길어져도 한 줄 유지 */
}
.card__body .desc {
  font-size: 18px;
  font-weight: 300;
  line-height: 1.4;
  padding-bottom: 20px;
  color: #666;
  /* 4줄효과 : 글이 넘쳐도 4줄을 넘지 않도록 해줌 */
  overflow: hidden;
  text-overflow: ellipsis;
  display: -webkit-box;
  -webkit-line-clamp: 4; /* 4줄까지 제한 */
  -webkit-box-orient: vertical;
}

/* 반응형 */
@media (max-width: 960px) {
  .card__inner {
    justify-content: space-around;
  }
  #cardType > h2 {
    font-size: 40px;
  }
  #cardType > p {
    font-size: 18px;
    line-height: 1.6;
  }
  .card__body .desc {
    margin-bottom: 16px;
    /* 3줄효과 */
    overflow: hidden;
    text-overflow: ellipsis;
    display: -webkit-box;
    -webkit-line-clamp: 3;
    -webkit-box-orient: vertical;
    padding-bottom: 0;
  }
}

@media (max-width: 600px) {
  #cardType > h2 {
    font-size: 30px;
  }
  #cardType > p {
    font-size: 16px;
    padding: 0px 20px;
  }
  .card__inner .card {
    width: 96%;
    margin-bottom: 20px;
  }
  .card__body {
    padding: 20px;
  }
  .card__body .title {
    font-size: 20px;
  }
  .card__body .desc {
    font-size: 16px;
  }
}
</style>
