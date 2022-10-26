<template>
    <footer id="footerType" class="footer__wrap gray" :class="attr">
        <h2 class="blind">푸터 영역</h2>
        <div class="footer__inner" :class="layout">
            <div class="footer__menu">
                <div>
                    <h3>상담신청</h3>
                    <ul>
                        <li><a href="#">방문 상담신청</a></li>
                        <li><a href="#">온라인 상담신청</a></li>
                        <li><a href="#">1:1 문의</a></li>
                    </ul>    
                </div>
                <div>
                    <h3>시간표 조회</h3>
                    <ul>
                        <li><a href="#">클래스A</a></li>
                        <li><a href="#">클래스B</a></li>
                        <li><a href="#">클래스C</a></li>
                        <li><a href="#">클래스D</a></li>
                    </ul>
                </div>
                <div>
                    <h3>아카데미 찾기</h3>
                    <ul>
                        <li><a href="#">강남 캠퍼스</a></li>
                        <li><a href="#">종로 캠퍼스</a></li>
                        <li><a href="#">구로 캠퍼스</a></li>
                        <li><a href="#">안산 캠퍼스</a></li>
                        <li><a href="#">수원 캠퍼스</a></li>
                    </ul>
                </div>
                <div>
                    <h3>문의 게시판</h3>
                    <ul>
                        <li><a href="#">질문하기</a></li>
                        <li><a href="#">건의사항</a></li>
                    </ul>
                </div>
                <div>
                    <h3>수강료문의</h3>
                    <ul>
                        <li><a href="#">방문 상담신청</a></li>
                        <li><a href="#">온라인 상담신청</a></li>
                        <li><a href="#">전화 상담신청</a></li>
                        <li><a href="#">카카오톡 상담신청</a></li>
                    </ul>
                </div>
            </div>
            <div class="footer__right">
                ⓒ2022 Byeolbit Jeppang Kyoshil<br>
                All rights reserved.
            </div>
        </div>
    </footer>
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
/* footerType */
.footer__menu {
    padding-bottom: 70px;
    display: flex;
    justify-content: space-between;
}
.footer__menu > div h3 {
    font-size: 18px;
    margin-bottom: 20px;
}
.footer__menu li a {
    font-size: 14px;
    color: #666;
    margin-bottom: 10px;
    display: block;
}
.footer__right {
    border-top: 1px solid #d9d9d9;
    text-align: center;
    padding-top: 40px;
    color: #666;
    line-height: 1.5;
}

/* 반응형 */
@media (max-width: 960px) {
    .footer__menu {
        display: none;
    }
    .footer__right {
        padding-top: 0;
        border-top: 0;
    }
    .footer__wrap {
        padding: 40px 0;
    }
}
</style>