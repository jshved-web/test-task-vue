<template>
  <div class="app">
    <main class="app__content">
      <side-bar/>
      <table-tools
        :tools="tools"
        :toggle="toggle"
        @show="getToolInfo"
      />
      <editor-menu :isActive="isActive" :tool="tool"/>
    </main>
  </div>
</template>

<script>
import TableTools from '@/components/TableTools'
import SideBar from '@/components/SideBar'
import EditorMenu from '@/components/EditorMenu'
export default {
  components: {
    EditorMenu,
    SideBar,
    TableTools
  },
  data () {
    return {
      tool: null,
      isActive: false,
      tools: [
        {
          id: 1,
          imgUrl: 'https://w7.pngwing.com/pngs/21/707/png-transparent-computer-icons-tool-others.png',
          description: 'Молоток и ключ'
        },
        {
          id: 2,
          imgUrl: 'https://w7.pngwing.com/pngs/21/707/png-transparent-computer-icons-tool-others.png',
          description: 'Молоток и ключ'
        },
        {
          id: 3,
          imgUrl: 'https://w7.pngwing.com/pngs/21/707/png-transparent-computer-icons-tool-others.png',
          description: 'Молоток ключ'
        }
      ]
    }
  },
  methods: {
    toggle () {
      this.isActive = !this.isActive
    },
    getToolInfo (tool) {
      this.tool = tool
      console.log(this.tool)
    }
  }
}
</script>
<style lang="scss">
*{
  box-sizing: border-box;
}
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
