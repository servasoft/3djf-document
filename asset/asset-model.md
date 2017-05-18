# 资产模型
>资产模型是根据资产的外观来进行区分的，例如机柜，不同的厂家的机柜外观不同，这些就需要添加多个资产模型

资产模型包含字段：
	id：required, 资产模型编号	categoryId：required, 资产分类编号，来自于资产分类模块的编号	description：资产模型描述	size：参考附录一：location、position、空间规划	childrenSize：；参考附录一：location、position、空间规划	model：required, 在3D场景中，资产模型对应的3D模型，模型ID注册在TWaver Make中，在3D场景中使用，必须有值	modelParameters：3D模型参数	simpleModel：简单模型，资产模型在延迟加载时使用的模型对象，注册在TWaver Make中	simpleModelParameters：简单模型参数	model2d：在2D场景中，资产模型对应的2D模型，模型ID注册在TWaver Make中，在2D场景中使用，必须有值	model2dParameters：2D模型参数	batchable： 默认值：false，保留字段，暂未使用	lazyable：默认值：false，是否延迟加载	stopAlarmPropagationable：默认值：false，阻止告警传播	rotationExp：高级用法，旋转表达式	positionExp：；高级用法，位置表达式{"z": "(data.parentCategory&&data.parentCategory.getId()&&data.parentCategory.getId().toLowerCase().indexOf('channel') >=0)?(z%2?-3:-5):z"}	system：默认值：false，类型标识，如果为true标识为系统内置分类，添加分类时忽略此属性，Boolean，内置的资产模型有设备、机柜、板卡、空调、端口、指示灯、电力系统、显示部件、各种柜子、通道、环境检测、办公、建筑、数据中心、列头柜、电视机、灭火器、灭火器组、门禁、地球	powerRating：默认值：0，用电额定功率	weightRating：默认值：0，承重	subtype: 子类型, 例如:设备分为服务器(server)和网络设备(network)	noPrefab: 是否使用clonePrefab方法复制相同的的对象,可以提高渲染效率	noVirtualOther: 当lookAt此类型模型时，不虚化其他模型
	searchFilter: 默认值：true，在下拉列表中，是否被过滤，如果值为true，显示，false，不显示### 添加资产模型

<font face="Droid Sans Mono,monospace" size="5">
<font color="#003bed"><b>POST</b></font> <font color="#888">http://{serverhost:serverport}</font>/api/datatype/add
</font>

#### Body

Accept: application/json

```
{
	id: '',
	categoryId: '',
	//... ... 资产模型其他不是必须字段
}
```

#### Returns
返回添加时传递过去的属性值，及其它默认值不为null的属性

Content-Type: application/json

```
//成功
{
	value: {
		"id": "",
		"categoryId": "",
		//... ... 其他添加时传递过去的属性值，及其它默认值不为null的属性
    },
	error: null
}
//失败
{error: 'error message' 或 {message:""} }
```

### 更新资产模型

<font face="Droid Sans Mono,monospace" size="5">
<font color="#003bed"><b>POST</b></font> <font color="#888">http://{serverhost:serverport}</font>/api/datatype/update
</font>

#### Body

Accept: application/json

```
{
	//需要更新的值
	value: {
		categoryId: '',
	},
	// 所有的更新条件
	options: {
		id: '',
	}
}
```
#### Returns
返回被更新资产模型的所有字段

Content-Type: application/json

```
//成功
{
	value: {
		//资产模型的所有字段
    },
	error: null
}
//失败
{error: 'error message' 或 {message:""} }
```

### 删除资产模型

<font face="Droid Sans Mono,monospace" size="5">
<font color="#003bed"><b>POST</b></font> <font color="#888">http://{serverhost:serverport}</font>/api/datatype/remove
</font>

#### Body

Accept: application/json

```
{
	// 所有的删除条件
	id: '',
}
```
#### Returns
被删除资产模型的所有字段

Content-Type: application/json

```
//成功
{
	value: {
		//被删除资产模型的所有字段
    },
	error: null
}
//失败
{error: 'error message' 或 {message:""} }
```

### 查看资产模型

<font face="Droid Sans Mono,monospace" size="5">
<font color="#003bed"><b>POST</b></font> <font color="#888">http://{serverhost:serverport}</font>/api/datatype/get
</font>

#### Body

Accept: application/json

```
{
	// 所有的查询条件
	id: '',
}
```
#### Returns
返回符合查询条件的第一个资产模型的所有字段

Content-Type: application/json

```
//成功
{
	value: {
		//符合查询条件的第一个资产模型的所有字段
    },
	error: null
}
//失败
{error: 'error message' 或 {message:""} }
```
### 搜索资产模型

<font face="Droid Sans Mono,monospace" size="5">
<font color="#003bed"><b>POST</b></font> <font color="#888">http://{serverhost:serverport}</font>/api/datatype/search
</font>

#### Body

Accept: application/json

```
{
	// 所有的搜索条件
	id: '',
}
```
#### Returns
返回符合搜索条件的所有资产模型的所有属性

Content-Type: application/json

```
//成功
{
	//符合搜索条件的所有资产模型
	value: [{
		//资产模型的所有属性
	}],
	error: null
}
//失败
{error: 'error message' 或 {message:""} }
```

