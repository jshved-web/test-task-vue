<template>
  <div class="sidebar">
    <div class="sidebar__content">
      <img :src="require('@/assets/Img Blur.png')" alt="">
      <p class="p"/>
      <p class="p"/>
      <p class="p"/>
      <p class="p"/>
    </div>
  </div>
</template>
<script>
export default {}
</script>
<style scoped lang="scss">
.sidebar {
  max-width: 236px;
  background: #262626;
  border: 1px solid #4D4D4D;
  border-radius: 12px;
  margin-right: 24px;
  padding: 15px;
  display: flex;
  justify-content: center;
  &__content{

  }
  .p{
    padding: 10px;
    border-radius: 4px;
    background: linear-gradient(90deg, #3C3C3C 0%, #444444 51.04%, #333333 100%);
  }
}
</style>
