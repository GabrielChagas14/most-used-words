<template>
  <div class="pill">
    <span class="name">{{ name }}</span>
    <span class="amount">{{ amount }}</span>
  </div>
</template>

<script>
export default {
  props: ["name", "amount"],
};
</script>

<style scoped>
.pill {
  background-color: rgb(230, 112, 180);
  color: #fff;
  margin: 10px;
  height: 55px;
  border-radius: 30px;
  font-size: 1.3em;
  font-weight: bold;
  display: flex;
  align-items: center;
}
.pill .name {
  margin-left: 15px;
}
.pill .amount {
  background: white;
  margin: 10px;
  padding: 5px;
  height: 35px;
  widows: 35px;
  border-radius: 18px;
  color: rgb(230, 112, 180);
  font-size: 14px;
  display: flex;
  justify-content: center;
  align-items: center;
}
</style>
