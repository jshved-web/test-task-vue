<template>
  <div class="table">
    <div class="table__cell" v-for="i in 25" :key="i">
      <div class="table__tool">
        {{ getPath()[i - 1] }}
      </div>
    </div>
  </div>
</template>
<script>
export default {
  props: {
    tools: {
      type: Array,
      required: true
    }
  },
  methods: {
    getPath () {
      return this.tools.map(tool => tool.description)
    }
  }
}
</script>
<style scoped lang="scss">
.table {
  display: flex;
  flex-wrap: wrap;
  width: 585px;
  min-height: 500px;
  background: #262626;
  border: 1px solid #4D4D4D;
  border-radius: 12px;

  &__cell {
    padding: 5px;
    border: 1px solid #4D4D4D;
    width: 105px;
    min-height: 100px;
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
