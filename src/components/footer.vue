<template>
  <div class="footer__inner">
    <div class="footer-top">
      <ul class="footer-top-list">
        <li class="footer-top-item"><img src="../assets/Framen.svg" alt="" /></li>
        <li class="footer-top-item">
          <a href="#"><span>8 800 841-95-95</span><br />Служба поддержки</a>
        </li>
        <li class="footer-top-item">
          <a href="#"><span>support@sport.ru</span><br />Служба поддержки</a>
        </li>
      </ul>
      <ul class="footer-top-list-right">
        <li class="footer-top-list-righ"><span>Вакансии</span></li>
        <li class="footer-top-list-righ">Блог</li>
        <li class="footer-top-list-righ">Акции</li>
        <li class="footer-top-list-righ elem">Предложить идею</li>
      </ul>
    </div>
    <div class="footer-mid">
      <ul class="footer-mid-list">
        <li class="footer-mid-item">
          <a href="#"><span>Женщинам</span></a>
        </li>
        <li class="footer-mid-item"><a href="#">Одежда</a></li>
        <li class="footer-mid-item"><a href="#">Обувь</a></li>
        <li class="footer-mid-item"><a href="#">Аксессуары</a></li>
        <li class="footer-mid-item"><a href="#">Белье</a></li>
        <li class="footer-mid-item"><a href="#">Bra fitting</a></li>
      </ul>
      <ul class="footer-mid-list">
        <li class="footer-mid-item">
          <a href="#"><span>Мужчинам</span></a>
        </li>
        <li class="footer-mid-item"><a href="#">Одежда</a></li>
        <li class="footer-mid-item"><a href="#">Обувь</a></li>
        <li class="footer-mid-item"><a href="#">Аксессуары</a></li>
        <li class="footer-mid-item"><a href="#">Белье</a></li>
      </ul>
      <ul class="footer-mid-list">
        <li class="footer-mid-item">
          <a href="#"><span>Детям</span></a>
        </li>
        <li class="footer-mid-item"><a href="#">Одежда</a></li>
        <li class="footer-mid-item"><a href="#">Обувь</a></li>
        <li class="footer-mid-item"><a href="#">Аксессуары</a></li>
        <li class="footer-mid-item"><a href="#">Белье</a></li>
        <li class="footer-mid-item"><a href="#">Игрушки</a></li>
        <li class="footer-mid-item"><a href="#">Малыши</a></li>
      </ul>
      <ul class="footer-mid-list">
        <li class="footer-mid-item">
          <a href="#"><span>Виды спорта</span></a>
        </li>
        <li class="footer-mid-item"><a href="#">Велоспорт</a></li>
        <li class="footer-mid-item"><a href="#">Туризм</a></li>
        <li class="footer-mid-item"><a href="#">Тренажеры и фитнес</a></li>
        <li class="footer-mid-item"><a href="#">Командные виды спорта</a></li>
        <li class="footer-mid-item"><a href="#">Самокаты</a></li>
      </ul>
    </div>
    <div class="footer-bottom">
      <ul class="footer-bottom-list">
        <li class="footer-bottom-item">
          <a href="#"><img src="../assets/file.svg" alt="" /> PDF презентация</a>
        </li>
        <li class="footer-bottom-item">
          <a href="#"><img src="../assets/video.svg" alt="" /> Видео инструкция</a>
        </li>
        <li class="footer-bottom-item">
          <a href="#"><img src="../assets/info.svg" alt="" /> FAQ</a>
        </li>
        <li class="footer-bottom-item">
          <a href="#"><img src="../assets/youtube.svg" alt="" /> Мы на YouTube</a>
        </li>
        <li class="footer-bottom-item"><a href="#">Политика конфиденциальности</a></li>
        <li class="footer-bottom-item"><a href="#">Лицензионное соглашение</a></li>
      </ul>
      <p class="footer-text">
        Настоящая Политика обработки персональных данных разработана в соответствии с Конституцией
        Российской Федерации, Трудовым кодексом Российской Федерации, Гражданским кодексом
        Российской Федерации, Федеральным законом от 27 июля 2006 года 149-ФЗ "Об информации,
        информационных технологиях и о защите информации"
      </p>
      <p class="footer-logo"><img src="../assets/Frames.svg" alt="" />Разработка платформы</p>
    </div>
  </div>
</template>

<script>
export default {}
</script>

<style scoped>
.footer-bottom-list {
  display: flex;
  gap: 0 28px;
}
.footer-top-list-righ {
  cursor: pointer;
}
.footer-logo {
  display: flex;
  align-items: center;
  gap: 0 24px;
  color: #8f9bb3;
  font-size: 14px;
  font-family: Gotham;
  font-weight: 700;
  line-height: 16px;
}
.footer-text {
  text-align: center;
  color: #828ead;
  font-size: 12px;
  font-family: Gotham;
  font-weight: 400;
  line-height: 16px;
}
.footer-bottom-item a {
  display: flex;
  align-items: center;
  gap: 0 8px;
  color: #828ead;
  font-size: 12px;
  font-family: Gotham;
  font-weight: 500;
  line-height: 16px;
}
.footer-bottom {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 40px;
  border-top: 1px #e2e4f0 solid;
  padding-top: 48px;
  padding-bottom: 48px;
}
a span {
  color: #050d23;
  font-size: 16px;
  font-family: Gotham;
  font-weight: 700;
  line-height: 24px;
}
.footer-mid-list .footer-mid-item:first-child {
  margin-bottom: 24px;
}
.footer-mid-list {
  display: flex;
  flex-direction: column;
  gap: 16px 0;
}
.footer-mid {
  display: flex;
  justify-content: space-between;
  border-top: 1px #e2e4f0 solid;
  border-bottom: 1px #e2e4f0 solid;
  padding-top: 48px;
  padding-bottom: 48px;
}
.elem {
  background: #f2f6ff;
  padding: 12px 24px;
  color: #1551e5;
  font-size: 14px;
  font-family: Gotham;
  font-weight: 500;
  line-height: 16px;
  cursor: pointer;
}
span {
  color: #050d23;
  font-size: 16px;
  font-family: Gotham;
  font-weight: 700;
  line-height: 20px;
}
a {
  text-decoration: none;
  color: #050d23;
  font-size: 14px;
  font-family: Gotham;
  font-weight: 400;
  line-height: 16px;
}
.footer-top-list,
.footer-top-list-right {
  display: flex;
  align-items: center;
  gap: 0 32px;
}
.footer-top-item a {
  color: #77829e;
  font-size: 12px;
  font-family: Gotham;
  font-weight: 400;
  line-height: 16px;
}
.footer-top {
  display: flex;
  justify-content: space-between;
  align-items: center;
  border-top: 1px #e2e4f0 solid;
  border-bottom: 1px #e2e4f0 solid;
  padding-top: 48px;
  padding-bottom: 48px;
}
.footer__inner {
  padding: 48px 24px;
}
</style>
