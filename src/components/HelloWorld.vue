<template>
  <div class="hello">
      <vue-tree-list :model="data" default-tree-node-name="新建组织" default-leaf-node-name="新建员工"></vue-tree-list>
  </div>
</template>

<script>

// import {VueTreeList,Tree, TreeNode} from './tree/index'
  import { VueTreeList, Tree, TreeNode } from 'vue-tree-list'


export default {
  name: 'HelloWorld',
  components: {
      VueTreeList:VueTreeList
  },
  data () {
    return {
        newTree: {},
        data: new Tree([
          {
            name: 'Node 1',
            id: 1,
            pid: 0,
            children: [
              {
                name: 'Node 1-2',
                id: 2,
                isLeaf: true,
                pid: 1
              }
            ]
          },
          {
            name: 'Node 2',
            id: 3,
            pid: 0
          },
          {
            name: 'Node 3',
            id: 4,
            pid: 0
          }
        ])
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
