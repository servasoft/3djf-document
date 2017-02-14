# 资产分类

在系统中可能某些功能针对某类资产进行处理，所以有了资产分类管理。例如在资产模型中的位置表达式中，如下：

```
{"z": "(data.parentCategory&&data.parentCategory.getId()&&data.parentCategory.getId().toLowerCase().indexOf('channel') >=0)?(z%2?-3:-5):z"
}

```
其中就用到了分类为channel的资产。通道可能存在多种样子，在资产类型中添加多个，这里要指定多个类型就不合理，最佳方案是根据分类来处理

资产分类包含字段：
	id：分类编号	description：分类描述
	stopAlarmPropagationable：阻止告警传播，Boolean	visible: 此分类的资产对象是否可见	system：分类标识，如果为true标识为系统内置分类，添加分类时忽略此属性，Boolean，内置分类有地球、数据中心、楼、楼层、机房、通道、机柜、列头柜、空调、发电机、设备、板卡、端口、指示灯、连线、部件、门禁、环境系统、消防、办公用品、电视机、普通柜子（配电柜、开关柜等）	