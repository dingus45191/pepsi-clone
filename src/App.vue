<template>
<div id="app">
  <section class="sec">
    <header>
      <a href="#"><img src="../logo.png" class="logo"></a>
      <ul>
        <li><a href="#">Home</a></li>
        <li><a href="#">Products</a></li>
        <li><a href="#">What's new</a></li>
        <li><a href="#">Newsletter</a></li>
        <li><a href="#">Contact</a></li>
      </ul>
    </header>
    <div class="content">
      <div class="text-box">
        <h2>That's what <br><span>I like</span></h2>
        <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod
          tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam,
          quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo
        </p>
        <a href="#">View All Products</a>
      </div>
      <div class="imgBox">
        <img src="../pepsi001.png" class="pepsi">
      </div>
    </div>
    <ul class="thumb">
      <li><img src="../pepsi001.png" @mouseover="imageSlider('../pepsi001.png');changeBackground('#0062be')"></li>
      <li><img src="../pepsi002.png" @mouseover="imageSlider('../pepsi002.png');changeBackground('#e60c2c')"></li>
      <li><img src="../pepsi003.png" @mouseover="imageSlider('../pepsi003.png');changeBackground('black')"></li>
    </ul>
    <ul class="sci">
      <li><img src="../facebook.png"></li>
      <li><img src="../twitter.png"></li>
      <li><img src="../instagram.png"></li>
    </ul>
  </section>
</div>
</template>

<script>
export default{
  methods:{
    imageSlider(anything) {
      document.querySelector('.pepsi').src = anything;
    },

    changeBackground(bg) {
      const sec = document.querySelector('.sec');
      sec.style.background = bg;
    }}

}
</script>

<style>

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: 'Poppins', sans-serif;
}

section {
    position: relative;
    width: 100%;
    min-height: 100vh;
    padding: 100px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    background: #0062be;
    transition: 0.5s;
}

header {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    padding: 20px 100px;
    display: flex;
    justify-content: space-between;
    align-items: center;
}

header .logo {
    position: relative;
    max-width: 80px;

}

header ul {
    position: relative;
    display: flex;

}

header ul li {
    list-style: none;
}

header ul li a {
    display: inline-block;
    color: #fff;
    font-weight: 400;
    margin-left: 40px;
    text-decoration: none;
}

.content {
    position: relative;
    width: 100%;
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.content .text-box {
    position: relative;
    max-width: 600px;

}

.content .text-box h2 {
    color: #fff;
    font-size: 4em;
    line-height: 1.5em;
    font-weight: 900;
    text-transform: uppercase;
}

.content .text-box h2 span {
    font-size: 2em;
}

.content .text-box p {
    color: #fff;
}

.content .text-box a {
    display: inline-block;
    margin-top: 20px;
    padding: 8px 20px;
    background-color: #fff;
    color: #111;
    border-radius: 40px;
    font-weight: 500;
    letter-spacing: 1px;
    text-decoration: none;
    text-transform: uppercase;
}

.content .imgBox {
    width: 600px;
    display: flex;
    padding-right: 50px;
    justify-content: flex-end;
    margin-top: 50px;
}

.content .imgBox img {
    max-width: 250px;
}

.thumb {
    position: absolute;
    left: 50%;
    bottom: 20px;
    transform: translateX(-50%);
    display: flex;
}

.thumb li {
    list-style: none;
    display: inline-block;
    margin: 0px 20px;
    cursor: pointer;
    transition: 0.5s;
}

.thumb li:hover {
    transform: translateY(-15px);
}

.thumb li img {
    max-width: 40px;
}

.sci {
    position: absolute;
    top: 50%;
    right: 30px;
    transform: translateY(-50%);
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
}

.sci li {
    list-style: none;
}

.sci li a {
    display: inline-block;
    filter: invert(1);
    margin: 5px 0px;
    transform: scale(0.6);
}
</style>
