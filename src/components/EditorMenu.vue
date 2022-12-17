<template>
<div  class="menu" v-bind:class="{ active: isActive }">
  <div class="menu__content">
    <div class="menu__header">
      <img :src="tool?.imgUrl" alt="" class="menu__img">
    </div>
    <div class="menu__body">

    </div>
  </div>
</div>
</template>
<script>
export default {
  props: {
    tool: {
      required: true
    },
    isActive: {
      required: true
    }
  }
}
</script>
<style scoped lang="scss">
.menu{
  transform: translateX(+100%);
  position: fixed;
  width: 100vw;
  height: 100vh;
  top: 0;
  right: 0;
  border-left: 1px solid #4D4D4D;
  transition: all 0.2s;
  &__img{
    object-fit: cover;
    width: 130px;
    height: 130px;
  }
  &__content {
    width: 30%;
    height: 100%;
    background: rgba(38, 38, 38, 0.5);
    display: flex;
    flex-direction: column;
    align-items: center;
  }
}
.menu.active {
  transform: translateX(72%);
}
</style>
