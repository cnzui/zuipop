zuipop 1.0  2014/12/08
====
简介：  
一个纯CSS打造、兼容各个浏览器的网页泡泡组件   

使用说明：   
1.该泡泡组件支持的浏览器有IE6+，Chrome，Firefox, Safari, 360等。   
2.标题和尾巴可以根据需要自由去留   
3.IE6浏览器，三角不能空心（因为不支持透明边框的CSS）   
4.IE6,IE7浏览器不支持圆角（因为border-radius属性不支持）   
5.泡泡高度支持自适应   
6.当需要设置泡泡的最小高度时，IE6中要通过修改panel-content的高度来实现   
7.当需要修改皮肤时，请用附加样式的方式实现，最好不要在组件的CSS中直接修改。   
8.修改颜色时，注意三角的样式要同步修改。   
9.组件自带的zuipop前缀，可以防止CSS冲突   


附例：   
一个完整的泡泡使用示例：pop.html

```html
<div class="zuipop-container">
    	<div class="zuipopgroup">
            <div class="zuipop">
              <div class="zuipop-panel">
      		<div class="zuipop-panel-heading"><p>标题</p></div>
      		<div class="zuipop-panel-content">这是泡泡内容<br /><h1>我可以无限增高的哦！！</h1>
                    <h2>我可以无限增高的哦！！</h2>
                    <h3>我可以无限增高的哦！！</h3>
                    <h4>我可以无限增高的哦！！</h4></div>
      		<div class="zuipop-panel-footering"><p>尾巴</p></div>
              </div>
              <div class="zuipop-arrowleft"></div>
              <div class="zuipop-arrowleft zuipop-arrowleft-hacker"></div>
            </div>
        </div>
</div>
```

修改皮肤颜色：skinsample.html

```html
<style>
.blueborder{
	border-color:blue !important;
}
.blueborder-leftarrow{
	border-right-color:blue !important;	/* 三角边框的颜色 */
	top:50px !important;
}
.blueborder-leftarrow::after{
	border-right-color:white !important;	/* 三角空心里的颜色 */
}
.blueheader{
	background:blue !important;
	color:white;
}
</style>
<div class="zuipop-container">
	<div class="zuipopgroup">
		<div class="zuipop">
		  <div class="zuipop-panel blueborder">
        <div class="zuipop-panel-heading blueheader"><p>标题</p></div>
        <div class="zuipop-panel-content">这是泡泡内容<br />
            <h1>我可以无限增高的哦！！</h1>
            <h2>我可以无限增高的哦！！</h2>
            <h3>我可以无限增高的哦！！</h3>
            <h4>我可以无限增高的哦！！</h4>
        </div>
        <div class="zuipop-panel-footering"><p>尾巴</p></div>
		  </div>
		  <div class="zuipop-arrowleft blueborder-leftarrow"></div>
		  <div class="zuipop-arrowleft zuipop-arrowleft-hacker"></div>
		</div>
	</div>
</div>
```


效果图
=====
![image](https://github.com/cnzui/zuipop/raw/master/screenshots/sample.jpg)

官方主页
=====
http://www.cnzui.com/