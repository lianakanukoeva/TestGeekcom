<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <FormBuild />
    <div class="cards">
      <Card v-for="(item, k) in card" 
        :key="k"
        :sale="item.sale"
        :img="item.img"
        :flat="item.flat"
        :area="item.area"
        :price="item.price"
        :address="item.address"  />
    </div>
  </div>
</template>

<script>
import FormBuild from '@/components/FormBuild'
import Card from '@/components/Card'

export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  components: {
    FormBuild,
    Card
  },
  data() {
    return {
      card: [
          {
              sale: "Скидка 6%",
              img: "yaroslavskiy-mytishci-jk-1471684959-7.jpg",
              flat: "1-комню квартира 26.3 m2",
              area: "ЖК Белые Росы",
              price: "1 118 000 ₽",
              address: "ул. Карамзина Семеновская"
          },
          {
              sale: "Скидка 6%",
              img: "yaroslavskiy-mytishci-jk-1471684959-7.jpg",
              flat: "1-комню квартира 26.3 m2",
              area: "ЖК Белые Росы",
              price: "1 118 000 ₽",
              address: "ул. Карамзина Семеновская"
          },
          {
              sale: "Скидка 6%",
              img: "yaroslavskiy-mytishci-jk-1471684959-7.jpg",
              flat: "1-комню квартира 26.3 m2",
              area: "ЖК Белые Росы",
              price: "1 118 000 ₽",
              address: "ул. Карамзина Семеновская"
          },
          {
              sale: "Скидка 6%",
              img: "yaroslavskiy-mytishci-jk-1471684959-7.jpg",
              flat: "1-комню квартира 26.3 m2",
              area: "ЖК Белые Росы",
              price: "1 118 000 ₽",
              address: "ул. Карамзина Семеновская"
          },
          {
              sale: "Скидка 6%",
              img: "yaroslavskiy-mytishci-jk-1471684959-7.jpg",
              flat: "1-комню квартира 26.3 m2",
              area: "ЖК Белые Росы",
              price: "1 118 000 ₽",
              address: "ул. Карамзина Семеновская"
          },
          {
              sale: "Скидка 6%",
              img: "yaroslavskiy-mytishci-jk-1471684959-7.jpg",
              flat: "1-комню квартира 26.3 m2",
              area: "ЖК Белые Росы",
              price: "1 118 000 ₽",
              address: "ул. Карамзина Семеновская"
          },
      ],
    }
  }
}
</script>
<style scoped lang="scss">
.cards {
  display: flex;
  justify-content: space-around;
  flex-wrap: wrap;
}
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
