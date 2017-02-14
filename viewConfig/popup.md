# 弹出面板

弹出面板是3D机房系统中当选择一个3D对象时，显示的html tab组件，弹出面板包含多个tab，其中这里配置的URL所指向的页面会作为一个tab显示，系统会将选中的3D对象ID传递给URL指向的页面弹出面板包含字段
	id：3D对象的分类编号，即category ID	props: 拓展属性，暂未使用	url：指向的页面路径, 例如：id为rack, url为https://www.baidu.com/, 那么当选中机柜的时候百度的首页会作为一个	
	tab, 在弹出的面板中