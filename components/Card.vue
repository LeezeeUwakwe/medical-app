<template>
  <div>
    <div class="card-wrapper">
      <div
        v-for="(card, index) in cards"
        :key="index"
        class="main-card"
      >
        <img :src="card.icon" class="main-icon" alt="" />
        <div class="top-wrapper">
          <p class="card-title">{{ card.title }}</p>
          <p class="number">{{ card.numbers }}</p>
          <div class="mini-wrapper">
            <img :src="card.subIcon"  alt="" />
            <p :class="card.subColor === 'warning' ? 'warning' : 'success'">
              {{ card.subText }}
            </p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    cards: {
      type: Array,
      default: () => [],
    },
  },

  data: () => ({ }),
}
</script>

<style scoped>
.warning {
  color: #CC0000;
  font-size: 10px;
  font-weight: 600;
}
.success {
  color: #03A300;
  font-size: 10px;
  font-weight: 600;
}
.main-card {
  display: flex;
  align-items: center;
  background-color: #fff;
  width: 205px;
  height: 5.9rem;
  padding: 16px 15px;
  border-radius: 6px;
  border: 1px solid #e0e0e0;
}
.card-wrapper {
  display: flex;
  margin-top: 25px;
  align-items: center;
  justify-content: space-between;
  width: 100%;
  justify-content: space-between;
}
.main-icon {
  width: 40px;
  height: 40px;
}
.card-title {
  font-size: 12px;
  color: #8f8f8f;
  font-weight: 600;
}
.top-wrapper {
  margin-left: 20px;
}
.mini-wrapper {
  display: flex;
  align-items: center;
}
.number {
  color: #292929;
  font-size: 17px;
  font-weight: 400;
}
.v-application p {
  margin-bottom: 0;
}

.v-application .success,
.v-application .warning  {
  background-color: #fff !important;
}
</style>
