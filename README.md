# VariableCilpImageView
可变裁剪区及缩放裁剪图片
大多图片裁剪大多两种操作：改变裁剪区图片不能缩放、裁剪区固定图片缩放，两种方法都可以裁剪到不同图片，本次介绍的是可变裁剪区同时能缩放图片，同时记录自己的开发项目过程。
	
	裁剪视图一共三个view，最底层的缩放CilpImageView ，中间是可变裁剪区CilpBorderView，还有最顶层的CilpTouchView。监听CilpTouchView的OnTouch事件，通过判断down手势是否落在拉伸裁剪区的按钮内分发给CilpBorderView或者CilpImageView 。
	Options类是默认裁剪配置。