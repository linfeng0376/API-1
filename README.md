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
	
### 6. 获取某个商店的首页
#### URL : /buyer/action

#### Method : POST

    {
        'action': 'GETDEFAULTHOMEPAGE',
       
        'streetId': '街道ID',
        
	
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
	


### 5. 根据用户名获取默认的Homepage
#### URL : /buyer/action

#### Method : POST

    {
        'action': 'GETDEFAULTHOMEPAGE',
       
        'streetId': '街道ID',
        
	
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
	


