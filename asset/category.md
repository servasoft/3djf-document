# 资产分类

在系统中可能某些功能针对某类资产进行处理，所以有了资产分类管理。例如在资产模型中的位置表达式中，如下：

```
{"z": "(data.parentCategory&&data.parentCategory.getId()&&data.parentCategory.getId().toLowerCase().indexOf('channel') >=0)?(z%2?-3:-5):z"
}

```
其中就用到了分类为channel的资产。通道可能存在多种样子，在资产类型中添加多个，这里要指定多个类型就不合理，最佳方案是根据分类来处理

资产分类包含字段：

	stopAlarmPropagationable：阻止告警传播，Boolean