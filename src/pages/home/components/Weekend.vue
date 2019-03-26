<template>
	<div>
	  <div class="title">火爆推荐</div>
	  <ul>
	  	<li 
	  	class="item border-bottom" 
	  	v-for="item of recommendList"
        :key="item.id"
	  	>
        <div class="item-img-wrapper">
	  		  <img class="item-img" src="item.imgUrl">
	  		</div>
        <div class="item-info">
	  		  <p class="item-title">{{item.title}}</p>
	  		  <p class="item-desc">{{item.desc}}</p>
	  		  <button class="item-button">详情</button>
	  	    </div>
	  	</li>
	  </ul>
    </div>
</template>

<script>
export default{
	name: 'HomeWeekend',
	data () {
		return {
			recommendList: [{
			id: '0001',
			imgUrl: '/data:image/gif;base64,iVBORw0KGgoAAAANSUhEUgAAAAEAAAABCAYAAAAfFcSJAAAADUlEQVQImWNgYGBgAAAABQABh6FO1AAAAABJRU5ErkJggg==',
			title: '大连',
			desc: '浪漫',
		},{
			id: '0002',
			imgUrl: '//gw.alicdn.com/tfs/TB1pN01wsUrBKNjSZPxXXX00pXa-210-126.png_450x10000.jpg_.webp',
			title: '大连',
			desc: '浪漫',
		}]
		}
       }
}
</script>

<style lang="stylus" scoped>
  @import '../../../assets/styles/mixins.styl'
  .title
    margin-top: .2rem
    line-height: .8rem
    background: #eee
    text-indent: .2rem
    .item-img-wrapper
      overflow: hidden
      height: 0
      padding-bottom: 33.9%
    .item-img
      width: 100%
    .item-info
      flex: 1
      padding: .1rem
      min-width: 0
      .item-title
        line-height: .54rem
        font-size: .32rem
        ellipsis ()
      .item-desc
        line-height: .4rem
        color: #ccc
        ellipsis ()
      .item-button
        line-height: .45rem
        margin-top: .15rem
        background: #ff9300
        padding: 0 .1rem
        border-radius: .06rem
</style>