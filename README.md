### 移动端 - 时间面板选择器(基于zepto)
使用说明:
1. 在页面上引入 css 和 js (可以参考index.html)
```
<link rel="stylesheet" type="text/css" href="css/mtimer.css">
<script type="text/javascript" src="js/zepto.js"></script>
<script type="text/javascript" src="js/mtimer.js"></script>
```

2. 在页面上使用 `input[type="text"]` 作为输入框,此外为了防止手机上弹出软件盘,添加 `readonly` 属性
```
<input type="text" id="picktime" value="03-27 15:00" readonly></input>
```

3. 日期组件初始化
```
$(function(){
	var opts = {
		dateStart : new Date(), // 开始时间
		dateNum : 10,			// 天数
		timeStart : 9,			// 开始时刻
		timeNum : 2,			// 小时数(从开始到结束的总时长)
		onOk : function() {		// 点击确定的回调函数
			console.log('你选择了时间...');
		},
		onCancel : function() {	// 点击取消的回调函数
			console.log('你取消了选择...');
		},
		interval : 2,			// 时间间隔(单位秒)[能被60整除的数都可以]
	};
	$('#picktime').mtimer(opts);
});
```
