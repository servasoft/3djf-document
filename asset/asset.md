# 资产
>资产对象管理的是资产实例，与实际资产对应，每个资产对象依据资产模型确定资产的外形，并在资产对象管理中设置资产的位置信息，从属关系。
资产对象中包含的字段：

字段 | 描述 | 数据类型 | 必填
----|-----| ------- | ----
id|资产对象编号| string | truename|资产对象名称| string | true
description | 数据描述 | string |
location | 参考附录一：location、position、空间规划 | json字符串 |
position2d | 2D中的物理坐标描述 | json字符串 |
rotation | 表示资产对象的旋转值，{x:0,y:0,z:0}，x、y、z分别表示三个方向上的旋转角度 | json字符串 |
position | 参考附录一：location、position、空间规划 | json字符串 |
parentId | 父对象，例如设备的的父对象为机柜| string | 
dataTypeId | 资产模型编号 | string |
weight | 资产重量 | int | true
businessTypeId | 业务类型编号 | string |