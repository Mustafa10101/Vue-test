<template>
  <Header :count="formattedTotalCount" />
  <Main @change-count="updateTotalCount" />
  <Footer />
  <RouterView />
</template>

<script>
import Header from '../src/components/header.vue'
import Footer from '../src/components/footer.vue'
import Main from '../src/components/main.vue'

export default {
  components: { Header, Footer, Main },
  data() {
    return {
      totalCount: 144235
    }
  },
  methods: {
    updateTotalCount(value) {
      if (this.totalCount + value >= 0) {
        this.totalCount += value
      }
    }
  },
  computed: {
    formattedTotalCount() {
      return this.totalCount.toLocaleString('ru-RU')
    }
  }
}
</script>

<style scoped></style>
