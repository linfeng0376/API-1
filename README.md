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
		'response': 'success'
	}

#### Error
	{
		'response': '非法参数'
	}
	


