API
===
### 1. 添加第一个联系地址,设为默认

#### URL : /buyer/action

#### Method : POST

    {
        'action': 'ADDFIRSTDEFAULTCONTACTINFO',
        'streetId': '街道ID',
        'detail': '详细地址',
        'postalcode': '邮编',
        'phone': '座机号',
        'mobile': '手机号',
	
    }

### Result:

#### Success
	{
		'response': 'success'
	}

#### Error
	{
		'response': '非法参数'
	}

### 2. 添加联系地址

#### URL : /buyer/action

#### Method : POST

    {
        'action': 'ADDCONTACTINFO',
        'streetId': '街道ID',
        'detail': '详细地址',
        'postalcode': '邮编',
        'phone': '座机号',
        'mobile': '手机号',
	
    }

### Result:

#### Success
	{
		'response': 'success'
	}

#### Error
	{
		'response': '非法参数'
	}
	
### 3. 编辑联系地址

#### URL : /buyer/action

#### Method : POST

    {
        'action': 'EDITCONTACTINFO',
        'contactInfoId':'联系地址ID',
        'streetId': '街道ID',
        'detail': '详细地址',
        'postalcode': '邮编',
        'phone': '座机号',
        'mobile': '手机号',
	
    }

### Result:

#### Success
	{
		'response': 'success'
	}

#### Error
	{
		'response': '非法参数'
	}
	

### 4. 获得最合适的商店

#### URL : /buyer/action

#### Method : POST

    {
        'action': 'GETBESTSTORE',
       
        'streetId': '街道ID',
        
	
    }

### Result:

#### Success
	{
		'storeid': '商店ID'，
		'name': '商店名字'，
		'street': '所属街道'，
		'inventory': {'商店库存'}，
		'orders': {'商店订单'}，
		'supplierOrders': {'商店进货单'}，
		'suppliers': '商店供货商'，
		'isonline': '是否营业'，
		'deliverFee': '配送收取的费用'，
		'freeAmount': '满多少总价免运费'，
		'orderDate': '当天的时间'，
		'serialNumber': '当天的流水号'，
		'score': '评分'，
	}

#### Error
	{
		'response': '非法参数'
	}
	
### 5. 根据用户名获取默认的Homepage

#### URL : /buyer/homepage

#### Method : POST

    {
        
        'storeId': '商店ID',
        
	
    }

### Result:

#### Success
	{
		'storeid': '商店ID'，
		'items': {'typeid':'类型ID'，
			'typename':'类型名称'，
			'productid':'商品ID'，
			'productname':'商品名称'，
			'productprice':'商品价格'，
			'url':'商品的图片路径',
			'types':{'typeid':'类型ID'，'typename':'类型名称'}
		
		}，
	
	}

#### Error
	{
		'response': '非法参数'
	}
	


### 6. 获取某个商店的首页
#### URL : /buyer/action

#### Method : POST

    {
        'action': 'GETHOMEPAGE',
       
        'storeId': '商店ID',
        
	
    }

### Result:

#### Success
	{
		'storeid': '商店ID'，
		'items': {'typeid':'类型ID'，
			'typename':'类型名称'，
			'productid':'商品ID'，
			'productname':'商品名称'，
			'productprice':'商品价格'，
			'originalprice':'进货价格'，
			'types':{'typeid':'类型ID'，'typename':'类型名称'}
		
		}，
	
	}

#### Error
	{
		'response': '非法参数'
	}
	

### 7. 通过用户的购物车生成Order

#### URL : /buyer/action

#### Method : POST

    {
        'action': 'CREATEORDER',
        'storeId': '商店ID',
        'contactId': '联系人Id',
       
	
    }

### Result:

#### Success
	{
		'orderId': '订单ID号'
	}

#### Error
	{
		'response': '非法参数'
	}

### 8. 获取用户的订单数据
#### URL : /buyer/action

#### Method : POST

    {
        'action': 'GETFORMEDBUYERORDERS',
       	'state':'订单状态'，
        'pageindex': '分页第几页',
        'pagesize': '分页页面大小',
	
    }

### Result:

#### Success
	{
		'orderid': '订单ID'，
		'date':'日期'，
		'totalprice':'总价'，
		'items': {
		
			'barcode':'商品ID'，
			'name':'商品名称'，
			'price':'商品价格'，
			'count':'商品数量'，
			'url':'商品图片URL'
		
		}，
	
	}

#### Error
	{
		'response': '非法参数'
	}
	


### 9. 获取用户的order具体信息
#### URL : /buyer/action

#### Method : POST

    {
        'action': 'GETFORMEDBUYERORDERDETAIL',
       	'orderId':'订单ID'，
       
	
    }

### Result:

#### Success
	{
		'orderid': '订单ID'，
		'createDate':'创建日期'，
		'payDate':'付款日期'，
		'prepareDate': '处理日期'，
		'deliverDate':'配送日期'，
		'finishDate':'完成日期'，
		'totalprice': '总价'，
		'username':'用户名'，
		'address':'地址'，
		'tel': '电话'，
		'payType':{'ONLINE'：'网上支付'，'DESTINATION':'货到付款'}
	
		
		
		
		'items': {
		
			'barcode':'商品ID'，
			'name':'商品名称'，
			'price':'商品价格'，
			'count':'商品数量'，
			'url':'商品图片URL'
		
		}，
	
	}

#### Error
	{
		'response': '非法参数'
	}
	
	
### 10. 添加收藏

#### URL : /buyer/action

#### Method : POST

    {
        'action': 'ADDTOFAVORATE',
        'barcode': '商品ID',
       
	
    }

### Result:

#### Success
	{
		'response': 'success'
	}

#### Error
	{
		'response': '非法参数'
	}
	
### 11. 添加商品到购物车

#### URL : /buyCart/action

#### Method : POST

    {
        'action': 'ADD',
        'barcode': '商品ID',
        'amount': '商品数量',
	
    }

### Result:

#### Success
	{
		'response': 'success'
	}

#### Error
	{
		'response': '非法参数'
	}
	
	
	
### 11. 添加商品到购物车

#### URL : /buyCart/action

#### Method : POST

    {
        'action': 'ADD',
        'barcode': '商品ID',
        'amount': '商品数量',
	
    }

### Result:

#### Success
	{
		'response': 'success'
	}

#### Error
	{
		'response': '非法参数'
	}
	
### 11. 购物车删除商品

#### URL : /buyCart/action

#### Method : POST

    {
        'action': 'DELETE',
        'barcode': '商品ID',
     
	
    }

### Result:

#### Success
	{
		'response': 'success'
	}

#### Error
	{
		'response': '非法参数'
	}
	
	
### 12. 购物车修改商品数量

#### URL : /buyCart/action

#### Method : POST

    {
        'action': 'DELETE',
        'barcode': '商品ID',
     	 'amount': '商品数量',
	
    }

### Result:

#### Success
	{
		'response': 'success'
	}

#### Error
	{
		'response': '非法参数'
	}
	
### 13. 获取用户的购物车
#### URL : /buyCart/action

#### Method : POST

    {
        'action': 'GET',
      
    }

### Result:

#### Success
	{
		'cartid': '购物车ID'，
	
		'cartitem': {
			'itemid':'购物车项ID'，
			'product':{
				'barcode':'商品ID'，
				'name':'商品名称'，
				'sellprice':'销售价格'，
				'type':{'商品类型'}，
				'clickcount':'人气指数'
			},
		
			'count':'商品数量'，
			'buyCart':'所属购物车'
		
		}，
	
	}

#### Error
	{
		'response': '非法参数'
	}
	
	
### 14. 配送订单
#### URL : /store/order/do

#### Method : POST

    {
        'action': 'DISPATCH',
        'orderid': '订单ID'，
	
      
    }

### Result:

#### Success
	{
		'response': 'success'
	
	}

#### Error
	{
		'response': '非法参数'
	}


### 15. 取消订单
#### URL : /store/order/do

#### Method : POST

    {
        'action': 'CANCEL',
        'orderid': '订单ID'，
	
      
    }

### Result:

#### Success
	{
		'response': 'success'
	
	}

#### Error
	{
		'response': '非法参数'
	}

### 16. 获取商品详情
#### URL : /product/info

#### Method : POST

    {
        'action': 'PRODUCTDETAIL',
        'storeId': '商店ID'，
        'barcode': '商品条码',
	
      
    }

### Result:

#### Success
	{
		"product":{
			"barcode":"6920459907429",
			"name":"CAN310每日C水晶24入",
			"url":"/a",
			"life":0,
			"price":0.0,
			"amount":100
		},
		"response":"productdetail"
}

#### Error
	{
		'response': '非法参数'
	}


### 16. 根据类型获取该类型的所有商品
#### URL : /product/info

#### Method : POST

    {
        'action': 'GETBYTYPE',
        'typeId': '类型Id'，
	
      
    }

### Result:

#### Success
	{
		"formProductDetails":[
					{
					"name":"酸辣牛肉面",
					"life":80,
					"price":0.0,
					"amount":100
					},
					{
					"name":"香菇炖鸡面",
					"life":80,
					"price":0.0,
					"amount":100
					},

				]
}

#### Error
	{
		'response': '非法参数'
	}
### 17. 获取所有的省份
#### URL : /buyer/address

#### Method : POST

    {
        'action': 'PROVINCE',
	
      
    }

### Result:

#### Success
	{
		"fpList":[
			{
				"provinceid":1,
				"name":"江苏省"
			}
		]
	}
#### Error
	{
		'response': '非法参数'
	}
	
	
	
### 18. 获取省份所有的市
#### URL : /buyer/address

#### Method : POST

    {
        'action': 'CITY',
	'provinceId':'省份ID'
      
    }

### Result:

#### Success
	{
	"fcList":[
			{
				"cityid":1,
				"name":"苏州市"
			}
		]
	}
#### Error
	{
		'response': '非法参数'
	}
### 19. 获得市下的所有区
#### URL : /buyer/address

#### Method : POST

    {
        'action': 'DISTRICT',
	'cityId':'城市ID'
      
    }

### Result:

#### Success
	{
	"fdList":[
			{
			"districtid":1,
			"name":"吴中区"
			}
		]
	}
#### Error
	{
		'response': '非法参数'
	}


### 20. 获得区下所有的街道
#### URL : /buyer/address

#### Method : POST

    {
        'action': 'STREET',
	'districtId':'区ID'
      
    }

### Result:

#### Success
	{
	"fsList":[
			{
			"streetid":1,
			"name":"浦庄大道"
			}
		]
	}
#### Error
	{
		'response': '非法参数'
	}

