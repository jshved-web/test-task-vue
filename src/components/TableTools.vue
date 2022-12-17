<template>
  <div class="table">
    <div class="table__cell" v-for="i in 25" :key="i-1">
      <div @click="() => clickOnTool(i)" class="table__tool">
        <img class="table__image" :src="getPath()[i-1]" alt="">
      </div>
    </div>
  </div>
</template>
<script>
export default {
  props: {
    tools: {
      required: true,
      type: Array
    },
    toggle: {}
  },
  methods: {
    clickOnTool (i) {
      this.toggle()
      this.$emit('show', this.tools[i - 1])
    },
    getPath () {
      return this.tools.map(tool => tool.imgUrl)
    }
  }
}
</script>
<style scoped lang="scss">
.table {
  display: flex;
  flex-wrap: wrap;
  width: 527px;
  min-height: 500px;
  background: #262626;
  border: 1px solid #4D4D4D;
  border-radius: 12px;

  &__cell {
    padding: 5px;
    border: 1px solid #4D4D4D;
    width: 105px;
    min-height: 100px;
    display: flex;
    justify-content: center;
    align-items: center;
  }

  &__tool {
    cursor: pointer;
  }

  &__image {
    object-fit: cover;
    max-width: 54px;
    max-height: 54px;
  }

  &__cell:first-child {
    border-radius: 12px 0 0 0;
  }

  &__cell:last-child {
    border-radius: 0 0 12px 0;
  }

  &__cell:nth-child(5) {
    border-radius: 0 12px 0 0;
  }

  &__cell:nth-child(21) {
    border-radius: 0 0 0 12px;
  }
}
</style>
