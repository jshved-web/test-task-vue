<template>
  <div class="app">
    <main class="app__content">
      <table-tools :tools="tools"/>
    </main>
  </div>
</template>

<script>
import TableTools from '@/components/TableTools'

export default {
  components: {
    TableTools
  },
  data () {
    return {
      tools: [
        {
          id: 1,
          imgUrl: 'https://w7.pngwing.com/pngs/21/707/png-transparent-computer-icons-tool-others.png',
          description: 'Молоток и ключ'
        },
        {
          id: 2,
          imgUrl: 'bbbbb',
          description: 'Молоток и ключ'
        },
        {
          id: 3,
          imgUrl: 'zzzzzz',
          description: 'Молоток ключ'
        }
      ]
    }
  }
}
</script>
<style lang="scss">
body {
  background: #1E1E1E;
}

.app {
  max-width: 998px;
  padding: 5px;
  margin: 0 auto;

  &__content {
    display: flex;
    justify-content: center;
  }
}
</style>
