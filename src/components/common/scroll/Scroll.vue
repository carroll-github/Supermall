<template>
  <div class="wrapper" ref="wrapper">
    <div class="content">
      <slot></slot>
    </div>
  </div>
</template>

<script>
  import BScroll from 'better-scroll'
  export default {
    name: 'Scroll',
    props: {
      probeType: {
        type: Number,
        default: 0
      },
      pullUpLoad: {
        type: Boolean,
        default: false
      }
    },
    data(){
      return{
        scroll: null
      }
    },
    mounted(){
      //1.创建Scroll对象
      this.scroll = new BScroll(this.$refs.wrapper, {
        click: true,
        probeType: this.probeType,
        pullUpLoad: this.pullUpLoad
        // pullUpLoad: true,
        // scrollbar: true,
        // pullDownRefresh: true
      }),

      //2.监听滚动的位置
      this.scroll.on('scroll', (position)=>{
        this.$emit('scroll', position)
      }),

      //3.上拉加载更多
      this.scroll.on('pullingUp', ()=>{
        this.$emit('pullingUp')
      })
    },
    methods: {
      //对scroll对象进行进一步封装
      scrollTo(x,y,time=300){
        this.scroll.scrollTo(x,y,time)
      },
      finishPullUp(){
        this.scroll.finishPullUp()
      }
    }
  }
</script>

<style>

</style>