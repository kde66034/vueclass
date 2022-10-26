<template>
  <section id="textType" class="text__wrap scroll" :class="attr">
    <span>GOAL</span>
    <h2 class="mb70">강의 목표에 대해 설명합니다.</h2>
    <div class="text__inner">
      <div class="text t1">
        <h3 class="text__title">형태와 맛 표현</h3>
        <p class="text__desc">
          빵과 과자의 고유 형태와 맛을 표현하는 방법을 습득하고 레시피를
          정확하게 이해하며 기초 조리 기술을 습득할 수 있습니다.
        </p>
        <a class="text__btn" href="#">더보기</a>
      </div>
      <div class="text t2">
        <h3 class="text__title">제과/제빵사 자격증 취득</h3>
        <p class="text__desc">
          시험대비에 맞춘 체계적인 실기 수업 진행으로 제과/제빵사 자격증 합격을
          위한 취득 노하우를 확실하게 전수합니다.
        </p>
        <a class="text__btn" href="#">더보기</a>
      </div>
      <div class="text t3">
        <h3 class="text__title">1시간 이내에 빠르게 만들기</h3>
        <p class="text__desc">
          지급된 재료로 요구하는 품목을 시험기간(1시간이내)에 1인분을 만들어내는
          실기 시험 형태로 진행할 수 있게 준비합니다.
        </p>
        <a class="text__btn" href="#">더보기</a>
      </div>
      <div class="text t4">
        <h3 class="text__title">훌륭한 파티시에로 성장하기</h3>
        <p class="text__desc">
          디저트 문화를 이끌어 갈 파티시에 양성을 목표로 최선의 교육을 제공하여
          수강생 모두가 원하는 꿈을 이루실 수 있습니다.
        </p>
        <a class="text__btn" href="#">더보기</a>
      </div>
      <div class="text t5">
        <h3 class="text__title">창업 노하우 학습</h3>
        <p class="text__desc">
          훌륭한 제빵사로 일하는 것도 물론 좋지만 자본이 모이게 된다면 제과점을
          차리는 것도 좋지요. 저희 학원에서 창업 노하우도 알려드립니다.
        </p>
        <a class="text__btn" href="#">더보기</a>
      </div>
      <div class="text t6">
        <h3 class="text__title">맛나게 먹기</h3>
        <p class="text__desc">
          맛있게 만든 빵을 맛나게 먹는 것도 중요합니다. 여기까지 오셨다면 '내가
          만든 게 맞나?' 싶을 정도로 빵의 맛이 무척 맛있을 것입니다.
        </p>
        <a class="text__btn" href="#">더보기</a>
      </div>
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
/* textType */
.text__inner {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
}
.text {
  width: 32%;
  margin-bottom: 2%;
  padding: 20px;
  box-sizing: border-box;
  border-radius: 10px;
  transition: background-color 0.4s ease;
}
.text:hover {
  background-color: #f5f5f5;
}
.text__title {
  font-size: 24px;
  line-height: 1;
  margin-bottom: 10px;
  white-space: nowrap;
  text-overflow: ellipsis;
  position: relative;
  padding-top: 75px;
}
.text__title::before {
  content: "";
  position: absolute;
  left: 0;
  top: 0;
  width: 60px;
  height: 60px;
  border-radius: 50%;
  background: url(../../assets/img/textType/text_icon.svg);
}
.text.t1 .text__title::before {
  background-position: 0 0;
}
.text.t2 .text__title::before {
  background-position: -60px 0;
}
.text.t3 .text__title::before {
  background-position: -120px 0;
}
.text.t4 .text__title::before {
  background-position: -180px 0;
}
.text.t5 .text__title::before {
  background-position: -240px 0;
}
.text.t6 .text__title::before {
  background-position: -300px 0;
}
.text__desc {
  font-size: 18px;
  font-weight: 300;
  line-height: 1.4;

  /* 3줄효과 : 글이 넘쳐도 4줄을 넘지 않도록 해줌 */
  overflow: hidden;
  text-overflow: ellipsis;
  display: -webkit-box;
  -webkit-line-clamp: 3; /* 3줄까지 제한 */
  -webkit-box-orient: vertical;

  color: #666;
  margin-bottom: 20px;
}
.text__btn {
  font-size: 16px;
  line-height: 1;
  text-decoration: underline;
  text-underline-position: under; /* 텍스트와 언더라인 간격 벌려줌 */
  color: #666;
}

/* 반응형 */
@media (max-width: 960px) {
  .text {
    width: 48%;
    margin: 10px auto;
    background: #f5f5f5;
  }
  #textType > h2 {
    font-size: 40px;
  }
  .text__title {
    font-size: 22px;
  }
  .text__desc {
    font-size: 18px;
  }
}

@media (max-width: 600px) {
  #textType > h2 {
    font-size: 30px;
  }
  .text__title {
    font-size: 20px;
  }
  .text__desc {
    font-size: 16px;
  }
  .text {
    width: 96%;
    margin: 10px auto;
  }
}
</style>
