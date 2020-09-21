<template>
  <div class="wrapper" ref="CateScroll">
    <div>
      <!-- 1.无论是否设置click: false，button都可以点击 -->
      <button @click="btnClick">啦啦啦</button>

      <!-- 2.必须设置click: true，div才可以点击 -->
      <div @click="divClick">哈哈哈</div>

      <ul class="content">
        <li>liebiao1</li>
        <li>liebiao2</li>
        <li>liebiao3</li>
        <li>liebiao4</li>
        <li>liebiao5</li>
        <li>liebiao6</li>
        <li>liebiao7</li>
        <li>liebiao8</li>
        <li>liebiao9</li>
        <li>liebiao10</li>
        <li>liebiao11</li>
        <li>liebiao12</li>
        <li>liebiao13</li>
        <li>liebiao14</li>
        <li>liebiao15</li>
        <li>liebiao16</li>
        <li>liebiao17</li>
        <li>liebiao18</li>
        <li>liebiao19</li>
        <li>liebiao20</li>
        <li>liebiao21</li>
        <li>liebiao22</li>
        <li>liebiao23</li>
        <li>liebiao24</li>
        <li>liebiao25</li>
        <li>liebiao26</li>
        <li>liebiao27</li>
        <li>liebiao28</li>
        <li>liebiao29</li>
        <li>liebiao30</li>
        <li>liebiao31</li>
        <li>liebiao32</li>
        <li>liebiao33</li>
        <li>liebiao34</li>
        <li>liebiao35</li>
        <li>liebiao36</li>
        <li>liebiao37</li>
        <li>liebiao38</li>
        <li>liebiao39</li>
        <li>liebiao40</li>
        <li>liebiao41</li>
        <li>liebiao42</li>
        <li>liebiao43</li>
        <li>liebiao44</li>
        <li>liebiao45</li>
        <li>liebiao46</li>
        <li>liebiao47</li>
        <li>liebiao48</li>
        <li>liebiao49</li>
        <li>liebiao50</li>
        <li>liebiao51</li>
        <li>liebiao52</li>
        <li>liebiao53</li>
        <li>liebiao54</li>
        <li>liebiao55</li>
        <li>liebiao56</li>
        <li>liebiao57</li>
        <li>liebiao58</li>
        <li>liebiao59</li>
        <li>liebiao60</li>
        <li>liebiao61</li>
        <li>liebiao62</li>
        <li>liebiao63</li>
        <li>liebiao64</li>
        <li>liebiao65</li>
        <li>liebiao66</li>
        <li>liebiao67</li>
        <li>liebiao68</li>
        <li>liebiao69</li>
        <li>liebiao70</li>
        <li>liebiao71</li>
        <li>liebiao72</li>
        <li>liebiao73</li>
        <li>liebiao74</li>
        <li>liebiao75</li>
        <li>liebiao76</li>
        <li>liebiao77</li>
        <li>liebiao78</li>
        <li>liebiao79</li>
        <li>liebiao80</li>
        <li>liebiao81</li>
        <li>liebiao82</li>
        <li>liebiao83</li>
        <li>liebiao84</li>
        <li>liebiao85</li>
        <li>liebiao86</li>
        <li>liebiao87</li>
        <li>liebiao88</li>
        <li>liebiao89</li>
        <li>liebiao90</li>
        <li>liebiao91</li>
        <li>liebiao92</li>
        <li>liebiao93</li>
        <li>liebiao94</li>
        <li>liebiao95</li>
        <li>liebiao96</li>
        <li>liebiao97</li>
        <li>liebiao98</li>
        <li>liebiao99</li>
        <li>liebiao100</li>
      </ul>
    </div>
  </div>
</template>

<script>
  import BScroll from 'better-scroll'

  export default {
    name: "Category",
    data(){
      return{
        scroll:null
      }
    },
    mounted(){
      this.scroll = new BScroll(this.$refs.CateScroll,{
        // probeType: 2,
        click: true, //点击
        pullUpLoad: true //上拉加载更多
      })

      this.scroll.on('scroll', (position)=>{
        console.log(position);
      })

      this.scroll.on('pullingUp', () => {
        console.log('上啦加载更多');
      })
    },
    methods: {
      btnClick(){
        console.log('啦啦啦');
      },
      divClick(){
        console.log('哈哈哈');
      }
    }

  }
    
</script>

<style scoped>
  .wrapper {
    height: 150px;
    background-color: palevioletred;

    overflow: hidden;

    /* 原生滚动在移动端卡顿，一般不用 */
    /* overflow-y: scroll; */
  }
</style>
