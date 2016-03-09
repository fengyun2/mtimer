### 移动端 - 时间面板选择器(基于zepto)
用法:
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
		interval : 2,			// 时间间隔(单位秒)
	};
	$('#picktime').mtimer(opts);
});
```
