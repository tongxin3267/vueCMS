<template>
  <div>
    <div class="mint-header" v-show="node.other.isFixed==1"></div>
    <mt-header :fixed="node.other.isFixed==1" :title="node.other.title" :style="node.styl" :component-name="node.name">
      <mt-button icon="back" slot="left">返回</mt-button>
      <div slot="right">
        <mt-button v-if="node.other.title_menu==1">
          <div class="icon iconfont icon-search" slot="icon"></div>
        </mt-button>
        <mt-button v-else-if="node.other.title_menu==2" >
          <div class="icon iconfont icon-gouwuche" slot="icon"></div>
        </mt-button>
        <mt-button icon="more" slot="right" v-if="node.other.isMore==1"></mt-button>
      </div>
    </mt-header>
  </div>

</template>

<script>
  import { Header, Button,Search } from 'mint-ui';
  export default {
    name: 'header-component',
    props: ['node', 'themeColor'],
    data(){
      return {
        search:""
      }
    },
    methods:{
    },
    components:{
      'mtHeader': Header,
      'mtButton': Button,
    }
  }
</script>

<style scoped>
.mint-header{
  background-color:#fff;color:#000;
}
</style>

