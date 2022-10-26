<template>
  <section id="imgTextType" class="imgText__wrap scroll gray" :class="attr">
    <h2 class="blind">자격증 과정</h2>
    <div class="imgText__inner" :class="layout">
      <div class="imgText__txt">
        <span>CERTIFICATION</span>
        <h3>자격증 과정</h3>
        <p>수강 중, 취득 가능한 자격증 목록입니다.</p>
        <ul>
          <li><a href="#">조리기능사 필기</a></li>
          <li><a href="#">제과·제빵기능사</a></li>
          <li><a href="#">커피 바리스타</a></li>
          <li><a href="#">산업기사/기능장</a></li>
          <li><a href="#">양식조리기능사</a></li>
          <li><a href="#">한식조리기능사</a></li>
        </ul>
      </div>
      <div class="imgText__img img1">
        <a href="#">자세히 보러가기</a>
      </div>
      <div class="imgText__img img2">
        <a href="#" class="blue">큐넷 바로가기</a>
      </div>
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
/* imgTextType */
.imgText__inner {
  display: flex;
  justify-content: space-between;
  flex-wrap: wrap;
}
.imgText__inner > div {
  width: 32%;
  /* height: 500px; */
}
.imgText__txt span {
  font-size: 16px;
  color: #666;
  text-decoration: underline;
  text-underline-position: under;
  margin-bottom: 20px;
  display: block;
}
.imgText__txt h3 {
  font-size: 50px;
  font-weight: 300;
  margin-bottom: 10px;
}
.imgText__txt p {
  font-size: 18px;
  font-weight: 300;
  line-height: 1.5;
  color: #666;
  margin-bottom: 40px;
}
.imgText__txt ul {
  font-size: 18px;
  font-weight: 300;
  line-height: 2;
}
.imgText__txt ul li {
  position: relative;
  padding-left: 20px;
}
.imgText__txt ul li a {
  color: #666;
}
.imgText__txt ul li a:hover {
  text-decoration: underline;
}
.imgText__txt ul li::before {
  content: "";
  width: 5px;
  height: 5px;
  border-radius: 50%;
  position: absolute;
  left: 5px;
  top: 9px;
  background: #666;
}
.imgText__img {
  border-radius: 10px;
  position: relative;
}
.imgText__img a {
  position: absolute;
  left: 30px;
  bottom: 30px;
  background-color: rgb(136, 119, 74);
  color: #fff;
  font-size: 16px;
  padding: 8px 25px;
  border-radius: 30px;
  display: inline-block;
  transition: all 0.3s ease;
}
.imgText__img a.blue {
  background-color: rgb(45, 83, 69);
  color: #fff;
}
.imgText__img a:hover,
.imgText__img a.blue:hover {
  background-color: #fff;
  color: rgb(80, 80, 80);
}

.imgText__img.img1 {
  background: url(../../assets/img/imgTextType/imgText_bg01.jpg) no-repeat center / cover;
}
.imgText__img.img2 {
  background: url(../../assets/img/imgTextType/imgText_bg02.jpg) no-repeat center / cover;
}

/* 반응형 */
@media (max-width: 960px) {
  .imgText__inner {
    flex-wrap: wrap;
  }
  .imgText__inner > .imgText__txt {
    width: 96%;
    height: auto;
    text-align: center;
    margin: 0 auto;
  }
  .imgText__inner > .imgText__img {
    width: 48%;
    height: 300px;
    padding: 10px;
    margin: 0 auto;
    box-sizing: border-box;
  }
  .imgText__txt > h3 {
    font-size: 40px;
  }
  .imgText__txt > p {
    margin-bottom: 60px;
  }
  .imgText__txt ul {
    display: none;
  }
  .imgText__txt ul li::before {
    display: none;
  }
  .imgText__img a {
    left: 20px;
    bottom: 20px;
  }
}

@media (max-width: 600px) {
  .imgText__inner > .imgText__txt {
    margin-bottom: 20px;
  }
  .imgText__inner > .imgText__img {
    width: 96%;
    height: 200px;
  }
  .imgText__inner > .imgText__img.img1 {
    margin-bottom: 20px;
  }
  .imgText__txt > span {
    font-size: 14px;
    margin-bottom: 10px;
  }
  .imgText__txt > h3 {
    font-size: 30px;
  }
  .imgText__txt > p {
    font-size: 16px;
  }
  .imgText__txt ul {
    font-size: 16px;
  }
}
</style>
