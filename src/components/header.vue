<template>
  <div class="header__inner">
    <img src="../assets/Framen.svg" alt="" />
    <button class="btn">
      <img class="btn-img" src="../assets/list.svg" alt="" />
      Меню
    </button>
    <div class="input-icon-wrapper">
      <input class="input" type="text" placeholder="Название запроса" />
    </div>
    <img src="../assets/bell.svg" alt="" />
    <img src="../assets/heart.svg" alt="" />
    <div class="pack">
      <img src="../assets/shopping-cart.svg" alt="" />
      {{ count }}₽
    </div>
    <div class="person">
      <img src="../assets/avatar.png" alt="" />
      Ермаков Е
      <img src="../assets/chevron-down.svg" alt="" />
    </div>
  </div>
  <div class="wrapper">
    <ul class="list-items">
      <li class="list-item">Мои заказы</li>
      <li class="list-item">Сотрубдники</li>
      <li class="list-item">Шаблон заказов</li>
      <li class="list-item">Обращения</li>
    </ul>
    <ul class="wrapper__list-items">
      <li class="wrapper__list-item elem">
        <img src="../assets/message-circle.svg" alt="" />
        Ваш менеджер
      </li>
      <li class="wrapper__list-item">
        <img src="../assets/percent.svg" alt="" />
        Акции
      </li>
      <li class="wrapper__list-item">Блог</li>
    </ul>
  </div>
</template>

<script>
export default {
  props: {
    count: {
      type: Number,
      required: true
    }
  }
}
</script>

<style scoped>
.elem {
  padding: 12px 24px;
  background: #f2f6ff;
}
.wrapper__list-item {
  display: flex;
  align-items: center;
  gap: 0 5px;
  cursor: pointer;
}
.wrapper__list-items {
  display: flex;
  gap: 0 24px;
  color: #1551e5;
  font-size: 14px;
  font-family: Gotham Pro;
  font-weight: 400;
  line-height: 16px;
}
.list-item {
  cursor: pointer;
}
.list-items {
  display: flex;
  gap: 0 24px;
  color: #071435;
  font-size: 14px;
  font-family: Gotham Pro;
  font-weight: 400;
  line-height: 16px;
}
.wrapper {
  display: flex;
  justify-content: space-between;
  padding: 12px 24px;
}
.person {
  display: flex;
  align-items: center;
  gap: 0 16px;
}
.pack {
  padding: 12px 24px;
  color: #1551e5;
  background: #f2f6ff;
  font-size: 14px;
  font-family: Gotham;
  font-weight: 700;
  line-height: 16px;
  display: flex;
  align-items: center;
  gap: 0 12px;
}
.header__inner {
  display: flex;
  justify-content: space-between;
  padding: 16px 24px;
  align-items: center;
}
.btn {
  padding: 12px 24px;
  background-color: #1551e5;
  color: white;
  font-size: 14px;
  font-family: Gotham;
  font-weight: 700;
  line-height: 16px;
  border-radius: 8px;
  border: none;
  display: flex;
  align-items: center;
}
.btn-img {
  width: 24px;
  cursor: pointer;
  margin-right: 15px;
  color: #fff;
}
.input {
  width: 730px; /* Задайте фиксированную ширину */
  max-width: 730px; /* Это ограничит ширину до 730px, но width ее задает */
  padding: 16px 16px;
  border-radius: 8px;
  color: #050d23;
  font-size: 14px;
  font-family: Gotham Pro;
  font-weight: 400;
  line-height: 16px;
}

.input-icon-wrapper {
  position: relative;
}
.input-icon-wrapper::before {
  position: absolute;
  content: '';
  background-image: url(../assets/close.svg);
  background-repeat: no-repeat;
  width: 24px;
  height: 24px;
  right: 40px;
  top: 13px;
  cursor: pointer;
}
.input-icon-wrapper::after {
  position: absolute;
  content: '';
  background-image: url(../assets/search.svg);
  background-repeat: no-repeat;
  width: 24px;
  height: 24px;
  right: 15px;
  top: 13px;
  cursor: pointer;
}
</style>
