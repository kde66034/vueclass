<template>
  <section id="headerType" :class="fonts">
    <div class="header__inner">
      <h1 class="header__logo">
        <a href="#">별빛제빵교실 <em>Baking Class</em></a>
      </h1>
      <div class="header__menu">
        <ul>
          <li class="active"><a href="#headerType">MAIN</a></li>
          <li><a href="#imageType">NOTICE</a></li>
          <li><a href="#imgTextType">CERTIFICATION</a></li>
          <li><a href="#cardType">CLASS</a></li>
          <li><a href="#bannerType">YOUTUBE</a></li>
          <li><a href="#textType">GOAL</a></li>
        </ul>
      </div>
      <div class="header__member">
        <a href="#">SIGN IN</a>
      </div>
      <div class="header__ham">
        <span></span>
        <span></span>
        <span></span>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  props: {
    fonts: String,
  },
};
</script>

<style>
/* headerType */
.header__inner {
  /* height: 70px; */
  display: flex;
  flex-wrap: wrap;
  align-items: center;
  justify-content: space-between;
  padding: 20px;
  box-sizing: border-box;
  border-bottom: 1px solid #ccc;
  position: fixed;
  left: 0;
  top: 0;
  right: 0;
  z-index: 10000;
  background: #fff;
  backdrop-filter: blur(10px);
  box-shadow: 0 0 4px #999;
}
.header__logo {
  font-size: 30px;
  font-weight: 700;
  text-transform: uppercase;
}
.header__logo a {
  color: rgb(80, 80, 80);
}
.header__logo em {
  font-size: 16px;
  font-weight: 400;
  color: rgb(130, 130, 130);
}
.header__menu {
  text-align: center;
}
.header__menu li {
  display: inline;
}
.header__menu li a {
  padding: 8px 30px;
  margin: 0 5px;
  transition: background-color 0.3s;
}
.header__menu li.active a {
  background: rgb(80, 80, 80);
  border-radius: 5px;
  color: #fff;
}
.header__menu li a:hover {
  background: rgb(130, 130, 130);
  border-radius: 5px;
  color: #fff;
}

.header__member {
  text-align: right;
}
.header__member a {
  font-size: 16px;
  border: 1px solid rgb(80, 80, 80);
  padding: 8px 30px;
  border-radius: 50px;
  transition: all 0.3s ease;
}
.header__member a:hover {
  background: rgb(80, 80, 80);
  color: #fff;
}
.header__ham {
  position: absolute;
  right: 10px;
  top: 12px;
  z-index: 1000;
  width: 50px;
  height: 50px;
  display: none;
  cursor: pointer;
}
.header__ham span {
  display: block;
  background: rgb(80, 80, 80);
  width: 30px;
  height: 2px;
  border-radius: 3px;
  margin-left: 10px;
  margin-top: 5px;
  transition: 0.25s margin 0.25s, 0.25s transform; /* margin에 딜레이 */
}
.header__ham span:nth-child(1) {
  margin-top: 18px;
}
.header__ham.active span {
  transition: 0.25s margin, 0.25s transform 0.25s; /* transform에 딜레이 */
}

.header__ham.active span:nth-child(1) {
  margin-top: 25px;
  margin-bottom: -7px;
  transform: rotate(45deg);
}
.header__ham.active span:nth-child(2) {
  transform: rotate(45deg);
}
.header__ham.active span:nth-child(3) {
  transform: rotate(135deg);
  margin-top: -2px;
}

/* 반응형 */
/* @media (max-width: 1420px) {
    .header__inner {
        display: flex;
        justify-content: flex-start;
        align-items: center;
        overflow-y: unset;
        overflow-x: unset;
    }
    .menu__bar {
        cursor: pointer;
        position: fixed;
        right: 20px;
        top: 30px;
    }
    .menu__bar .ico {
        width: 20px;
        height: 20px;
        background-image: url("../img/bars-solid.svg");
        background-repeat: no-repeat;
        background-position: center;
    }
    
    .header__menu {
        display: none;
    }
    .header__menu.on {
        display: block;
    }
    .header__menu ul {
        padding: 20px;
        position: fixed;
        right: 20px;
        top: 60px;
        display: flex;
        flex-direction: column;
        background-color: #fff;
        box-shadow: 0 0 4px #999;
        border-radius: 5px;
    }
    .header__menu ul li {
        margin: 20px 0;
        text-align: center;
    }
    .header__menu ul li a {
        font-size: 16px;
        font-weight: 400;
        padding: 10px 20px;
        transition: all 0.3s ease;
    }

    .header__logo {
        margin-right: 10px;
    }
    .header__member {
        text-align: left;
    }
}

@media (max-width: 1080px) {
    .header__inner > h1 {
        font-size: 24px;
        margin-right: 10px;
    }
    .header__logo em {
        display: none;
    }
    .header__inner .header__menu ul li a {
        font-size: 18px;
        padding: 10px 25px;
    }
    .header__member a {
        font-size: 14px;
        margin-right: 10px;
    }
} */

@media (max-width: 1300px) {
  .header__ham {
    display: block;
  }
  .header__member {
    margin-right: 50px;
  }
  .header__menu {
    position: fixed;
    right: -100%;
    top: 69px;
    background: #fff;
    width: 60%;
    height: 100vh;
    padding: 20px;
    text-align: right;
    transition: right 0.4s ease-in;
    font-size: 16px;
  }
  .header__menu ul li {
    display: block;
    margin: 20px;
  }
  .header__menu ul li a {
    padding: 10px;
    white-space: nowrap;
  }
  .header__menu.active {
    right: 0;
  }
  .header__menu.overlay {
  }
}

@media (max-width: 600px) {
  .header__logo {
    font-size: 24px;
  }
  .header__logo em {
    display: none;
  }
  .header__member {
    width: 40%;
  }
  .header__member a {
    padding: 8px 20px;
  }
}
</style>
