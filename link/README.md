# 管线

管线指的是两个资产对象之间的连线

	id：唯一标示符，类型为string	dataTypeId：管线的资产模型，资产模型表中的ID，用于控制管线的显示效果	name：管线名称	fromId：管线起始资产的ID，资产表中的ID，例如设备A连接到设备B，fromId是A的id	fromPortId：如果管线是从设备上端口上开始，例如设备A的端口a1连接到设备B的端口	b1.fromPortId指a1的资产id	fromOffset：指管线的起始端离起始资产直接的偏移量，如果为0，两者连接在一起	toId：管线结束资产的ID，资产表中的ID，例如设备A连接到设备B，toId是的id	toPortId：如果管线是从设备上端口上开始，例如设备A的端口a1连接到设备B的端口b1.toPortId指b1的资产id	toOffset：指管线的结束端离结束资产直接的偏移量，如果为0，两者连接在一起	type:当type为“link”时就创建mono.Link,否则创建mono.PathLink	path：管线的路径	description：描述