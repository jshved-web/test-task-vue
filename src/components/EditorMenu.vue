<template>
<div  class="menu" v-bind:class="{ active: isActive }">
  <div class="menu__content">
    <div class="menu__header">
      <img :src="tool?.imgUrl" alt="" class="menu__img">
    </div>
    <div class="menu__body">
      <div class="menu__text">
        <p>{{ tool?.description }}</p>
        <p/>
        <p/>
        <p/>
        <p/>
      </div>
      <div class="menu__footer">
        <button @click="onDelete" class="menu__button">Удалить предмет</button>
      </div>
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
  },
  methods: {
    onDelete () {
      this.$emit('delete', this.tool)
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
  &__header{
    border-bottom: 3px solid #4D4D4D;
  }
  &__img{
    margin: 60px;
    object-fit: cover;
    width: 150px;
    height: 150px;
  }
  &__content {
    width: 30%;
    height: 100%;
    background: rgba(38, 38, 38, 0.5);
    display: flex;
    flex-direction: column;
    align-items: center;
  }
  &__text p{
    text-align: center;
    width: 211px;
    margin-top: 16px;
    background: linear-gradient(90deg, #3C3C3C 0%, #444444 51.04%, #333333 100%);
    border-radius: 8px;
    padding: 10px;
    font-size: 17px;
    color: white;
  }
  &__footer{
    margin-top: 24px;
    border-top: 3px solid #4D4D4D;
  }
  &__button {
    color: #FFFFFF;
    margin-top: 24px;
    cursor: pointer;
    width: 220px;
    height: 39px;
    background: #FA7272;
    border-radius: 8px;
  }
}
.menu.active {
  transform: translateX(72%);
}
</style>
