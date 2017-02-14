# 巡检

巡检是运维产品必不可少的功能，是一个想对告警来说，检查频率想对较低，涉及到指标想对较少，有固定轨迹，固定时间轮训检查硬件状态的功能。
巡检报告相关字段
	inpectionId：巡检路径的编号  string	startTime：开始巡检时刻yyyy-MM-ddHH:mm:ss	endTime：结束巡检时刻yyyy-MM-ddHH:mm:ss	remark：本次巡检的备注信息 string巡检结果相关字段	dateTime：巡检时刻yyyy-MM-ddHH:mm:ss	target：巡检资产对象的编号 string	type：巡检结果类型，目前只支持text，后续可能会增加url等方式，可以在系统播放时，显示对应的url界面。	content：巡检结果，查看巡检报告时，会弹出对话框，显示该字段里面的内容，type的只为url时，这里传入对应的url地址。