<template>
  <div class="main-inner">
    <div class="main-list">
      <div class="main-item">Каталог</div>
      <div class="main-item">/</div>
      <div class="main-item">Обувь</div>
      <div class="main-item">/</div>
      <div class="main-item">Кроссовки</div>
      <div class="main-item">/</div>
      <div class="main-item">Беговые</div>
    </div>
    <h1>Кроссовки мужские Skechers Sunny Dale</h1>
    <div class="sneakers">
      <div>
        <img src="../assets/Rectangle1.png" alt="" />
      </div>
      <div class="product__inner">
        <div class="product">
          <div class="product-left">
            <p class="action">166 534.00 цена без скидки</p>
            <p class="price">122 566 ₽<span class="percent">-15%</span></p>

            <div class="checkbox-container">
              <label for="checkbox" class="checkbox-label">
                <span class="quantity">12 шт в уп.</span>
                <input type="checkbox" id="checkbox" class="custom-checkbox" v-model="isChecked" />
                <span class="description">Заказ упаковкой</span>
              </label>
            </div>
            <table class="table">
              <tr class="tr">
                <td class="td">Завтра</td>
                <td class="td">7 шт.</td>
                <td class="td">7 шт.</td>
              </tr>

              <tr class="tr">
                <td class="td">Доставка</td>
                <td class="td">Тарасовка</td>
                <td class="td">Тарасовка</td>
              </tr>
            </table>
            <div class="buttons">
              <a v-if="btn" @click="addToCart" class="link" href="#">
                <img src="../assets/shopping-cart.svg" alt="" />
                <span>В корзину</span>
              </a>
              <a v-else class="btns" href="#">
                <button @click="decreaseQuantity"><img src="../assets/minus.svg" alt="" /></button>
                <p>{{ quantity }} шт</p>

                <button @click="increaseQuantity"><img src="../assets/plus.svg" alt="" /></button>
              </a>
              <button class="heart">
                <img src="../assets/heart.svg" alt="" />
              </button>
            </div>
          </div>
          <div class="product-right">
            <h2>Характеристики</h2>
            <table>
              <tr>
                <td class="haracteris">ELC00696</td>
                <td class="haracteris">ELC0200000696</td>
              </tr>
              <tr>
                <td class="haracteris">Код поставщика</td>
                <td class="haracteris">Артикул</td>
              </tr>
              <tr>
                <td class="haracteris">ELC00696</td>
                <td class="haracteris">ELC00696</td>
              </tr>
              <tr>
                <td class="haracteris">Код РАЭК</td>
                <td class="haracteris">Код ЕТМ</td>
              </tr>
              <tr>
                <td class="haracteris">Electric used</td>
                <td class="haracteris">ELC00696</td>
              </tr>
              <tr>
                <td class="haracteris">Бренд</td>
                <td class="haracteris">Серия</td>
              </tr>
              <tr>
                <td class="haracteris">ELC0200000696</td>
                <td class="haracteris"></td>
              </tr>
              <tr>
                <td class="haracteris">Код производителя</td>
                <table></table>
              </tr>
            </table>
          </div>
        </div>
        <div class="description">
          <h2>Описание товара</h2>
          <p>
            Создание приверженного покупателя специфицирует неопровержимый комплексный анализ
            ситуации. CTR существенно индуцирует из ряда вон выходящий SWOT-анализ. Воздействие на
            потребителя определяет возрастающий интеграл по поверхности, что известно даже
            школьникам. Отсюда естественно следует, что коммуникация уравновешивает косвенный фактор
            коммуникации. Поле направлений естественно допускает экспериментальный скачок функции,
            таким образом сбылась мечта идиота - утверждение полностью доказано. Арифметическая
            прогрессия притягивает линейно зависимый пул лояльных изданий.
          </p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      btn: true,
      quantity: 0,
      price: 122566,
      isChecked: true
    }
  },
  methods: {
    addToCart() {
      event.preventDefault()
      this.btn = false
    },
    increaseQuantity() {
      event.preventDefault()
      this.quantity += 12
      this.$emit('change-count', this.price) // Эмитим событие с ценой в качестве значения
    },
    decreaseQuantity() {
      event.preventDefault()
      if (this.quantity > 0) {
        this.quantity -= 12
        this.$emit('change-count', -this.price) // Эмитим событие с отрицательной ценой, чтобы уменьшить общую сумму
      }
    }
  }
}
</script>

<style scoped>
.percent {
  padding: 2px 8px;
  background: #ff3d71;
  border-radius: 4px;
  color: white;
  font-size: 16px;
  font-family: Gotham;
  font-weight: 700;
  line-height: 20px;
}
.btns {
  display: flex;
  align-items: center;
  padding: 8px 16px;
  border: solid 1px blue;
  text-decoration: none;
}
.btns p {
  width: 184px;
  text-align: center;
  max-width: 184px;
  color: #071435;
  font-size: 16px;
  font-family: Gotham;
  font-weight: 500;
  line-height: 24px;
}
.btns button {
  background: none;
  border: none;
  width: 24px;
}
.sneakers {
  display: flex;
  gap: 48px;
}
tr:nth-child(odd) td {
  color: #071435;
  font-size: 14px;
  font-family: 'Gotham', sans-serif;
  font-weight: 700;
  line-height: 16px;
  padding-bottom: 8px;
}
tr:nth-child(even) td {
  color: #828ead;
  font-size: 12px;
  font-family: 'Gotham', sans-serif;
  font-weight: 400;
  line-height: 16px;
  padding-bottom: 24px;
}
.haracteris {
  max-width: 302px;
  width: 302px;
  padding-right: 16px;
  padding-left: 0;
  padding-top: 4px;
  padding-bottom: 0;
  vertical-align: top;
  box-sizing: border-box;
}

tr td:last-child {
  padding-right: 0;
}
table {
  width: 100%;
  border-collapse: separate;
  border-spacing: 0;
}
tr:last-child td {
  padding-bottom: 0;
}
.product-left {
  padding-bottom: 48px;
  padding-right: 48px;
  border-right: 1px #e2e4f0 solid;
  width: 372px;
  max-width: 372px;
}
.product-right {
  padding-left: 48px;
}
h2 {
  color: #071435;
  font-size: 20px;
  font-family: Gotham;
  font-weight: 500;
  line-height: 20px;
  margin-bottom: 32px;
}
.link {
  padding: 16px 24px;
  background: #1551e5;
  color: #fff;
  border-radius: 8px;
  display: flex;
  align-items: center;
  gap: 0 12px;
  text-decoration: none;
  font-size: 14px;
  font-family: Gotham;
  font-weight: 500;
  line-height: 16px;
  width: 100%;
  justify-content: center;
}
.buttons {
  display: flex;
  gap: 0 16px;
}
.heart {
  padding: 16px 24px;
  border: none;
  background: #f2f6ff;
}
.table {
  width: 100%;
  border-collapse: collapse;
  padding: 32px 0px;
  display: inline-block;
}

.td {
  text-align: center;
  padding: 5px 50px 5px 0;
}

.td:last-child {
  padding-right: 0;
}

.tr:first-child .td {
  color: #071435;
  font-size: 14px;
  font-family: 'Gotham', sans-serif;
  font-weight: 700;
  line-height: 16px;
}

.tr:last-child .td {
  color: #828ead;
  font-size: 12px;
  font-family: 'Gotham', sans-serif;
  font-weight: 400;
  line-height: 16px;
  border-bottom: none;
}
.action {
  color: #ff3d71;
  font-size: 14px;
  font-family: Gotham;
  font-weight: 500;
  line-height: 16px;
  margin-bottom: 24px;
}
.price {
  display: flex;
  align-items: center;
  gap: 16px;
  color: #071435;
  font-size: 32px;
  font-family: Gotham;
  font-weight: 700;
  line-height: 48px;
  letter-spacing: 0.32px;
  margin-bottom: 33px;
}
.product {
  display: flex;
}
.checkbox-container {
  display: flex;
  align-items: center;
  font-family: 'Gotham', sans-serif;
  font-size: 14px;
  padding-bottom: 37px;
  border-bottom: 1px #e2e4f0 solid;
}

.custom-checkbox[data-v-fe6f7832] {
  -webkit-appearance: none;
  -moz-appearance: none;
  appearance: none;
  width: 36px;
  height: 20px;
  background: #1551e5;
  border: 2px solid #1551e5;
  border-radius: 32px;
  outline: none;
  cursor: pointer;
  position: relative;
  margin-right: 8px;
  flex-shrink: 0;
}

.custom-checkbox[data-v-fe6f7832]:checked::after {
  content: '';
  position: absolute;
  width: 12px;
  height: 12px;
  background: white;
  border-radius: 50%;
  left: 17px;
  top: 3px;
  box-shadow: 0 0 0 2px white;
}

.checkbox-label {
  display: flex;
  align-items: center;
  gap: 16px;
}
.description {
  display: inline-block;
  color: #071435;
  font-size: 14px;
  font-family: Gotham;
  font-weight: 500;
  line-height: 16px;
}
.quantity {
  color: #828ead;
  font-weight: 700;
  line-height: 16px;
  word-wrap: break-word;
  background: #f2f5f9;
  padding: 8px;
}

.descr {
  color: #071435;
  font-weight: 500;
}
h1 {
  color: #071435;
  font-size: 32px;
  font-family: Gotham Pro;
  font-weight: 400;
  text-transform: uppercase;
  line-height: 32px;
  padding-top: 24px;
  padding-bottom: 32px;
}
.main-item {
  color: #828ead;
  font-size: 12px;
  font-family: Gotham;
  font-weight: 400;
  line-height: 16px;
  word-wrap: break-word;
}
.main-list {
  width: 100%;
  height: 100%;
  justify-content: flex-start;
  align-items: center;
  gap: 4px;
  display: inline-flex;
}
</style>
