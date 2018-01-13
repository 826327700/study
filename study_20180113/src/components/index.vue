<template>
  <div class="hello">
     <p>请输入id,获取中文名</p>
     <p>可选id:2,3,382,383,384,396,397,398</p>
     <el-input v-model="input" placeholder="请输入id" style="width:200px"></el-input><el-button @click="getName" type="primary">获取名称</el-button>
    <p>中文名：{{name}}</p>
  </div>
</template>

<script>
/**
 * 要求：在输入框中输入任意层级下的id，获取到id对应的中文名称
 */
import data from '@/data.js'
export default {
  name: "index",
  data() {
    return {
      data:data,//id数据源
      id:'',
      name:''
    };
  },
  methods: {
    getName(){

    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1,
h2 {
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
