API
===
### 1. Create user

#### URL : /api/user/create/

#### Method : POST

    {
        'username': '用户名',
        'password': '密码',
        'repeatPwd': '密码',
        'mobile': '11位手机号码',
        'email': '电子邮箱',
		'community': '1', (小区的主键)
		'is_admin': '1', ('0':业主, '1':工作人员, '2':管理员)
		'floor': '楼栋号',
		'gate_card': '门牌号',
		'address': '详细地址'
    }

### Result:

#### Success
	{
		'info': 'create user successful'
	}

#### Error
	{
		'username_error': True, 
		'info': '用户名已存在'
	}

	{
		'password_error': True, 
		'info': '两次密码输入不相同'
	}

	{
		'password_error': True, 
		'info': '密码：字母、数字组成，6-15位'
	}

	{
		'mobile_error': True, 
		'info': '请输入正确的手机号码'
	}

	{
		'email_error': True, 
		'info': '请输入正确的邮箱地址
	}

