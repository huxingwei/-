
**express RESTful API**


**简介**：<p>此API提供接口调用</p>


**HOST**:127.0.0.1:8090


**联系人**:


**Version**:2.0

**接口路径**：/v2/api-docs?group=business-api


# Home管理相关接口

## 登录


**接口描述**:


**接口地址**:`/api/v1/home/login.do`


**请求方式**：`POST`


**consumes**:`["application/json"]`


**produces**:`["application/json"]`



**请求参数**：

| 参数名称         | 参数说明     |     in |  是否必须      |  数据类型  |  schema  |
| ------------ | -------------------------------- |-----------|--------|----|--- |
|account| 手机号或者邮箱  | query | true |string  |    |
|password| 登录密码，必传  | query | true |string  |    |
|source| 来源: 来源 1PC  2PC后台  3安卓  4苹果 5微信  | query | true |string  |    |

**响应示例**:

```json
{
	"code": "",
	"data": {
		"dateRegister": "",
		"email": "",
		"googleAuthCode": "",
		"inviterId": "",
		"ipRegister": "",
		"loginFailTimes": "",
		"macRegister": "",
		"mobile": "",
		"monthSendExpressNum": 0,
		"monthSignExpressNum": 0,
		"nationCode": "",
		"nickName": "",
		"realName": "",
		"sendExpressNum": 0,
		"sex": "",
		"signExpressNum": 0,
		"siteId": 0,
		"source": "",
		"token": "",
		"userCode": "",
		"userId": "",
		"userStatus": ""
	},
	"description": ""
}
```

**响应参数**:


| 参数名称         | 参数说明                             |    类型 |  schema |
| ------------ | -------------------|-------|----------- |
|code| 响应代码  |string  |    |
|data| 响应数据  |用户信息  | 用户信息   |
|description| 响应描述  |string  |    |



**schema属性说明**




**用户信息**

| 参数名称         | 参数说明                             |    类型 |  schema |
| ------------ | ------------------|--------|----------- |
|dateRegister | 注册时间   |string  |    |
|email | 邮箱   |string  |    |
|googleAuthCode | 谷歌验证码   |string  |    |
|inviterId | 邀请人ID   |string  |    |
|ipRegister | 注册IP   |string  |    |
|loginFailTimes | 当日登录失败次数   |string  |    |
|macRegister | 注册物理地址   |string  |    |
|mobile | 手机号码   |string  |    |
|monthSendExpressNum | 本月入库快递件数   |integer(int32)  |    |
|monthSignExpressNum | 本月签收快递件数   |integer(int32)  |    |
|nationCode | 国籍区号   |string  |    |
|nickName | 昵称   |string  |    |
|realName | 姓名   |string  |    |
|sendExpressNum | 今日入库快递件数   |integer(int32)  |    |
|sex | 性别 1男 2女   |string  |    |
|signExpressNum | 今日签收快递件数   |integer(int32)  |    |
|siteId | 所属站点id   |integer(int32)  |    |
|source | 注册来源 1PC 2PC后台 3安卓 4苹果 5微信   |string  |    |
|token | 用户Token   |string  |    |
|userCode | UID用户编号（自己的推广码）   |string  |    |
|userId | 用户ID   |string  |    |
|userStatus | 1正常 2锁定   |string  |    |

**响应状态**:


| 状态码         | 说明                            |    schema                         |
| ------------ | -------------------------------- |---------------------- |
| 200 | OK  |响应结果«用户信息»|
| 201 | Created  ||
| 401 | Unauthorized  ||
| 403 | Forbidden  ||
| 404 | Not Found  ||
## 注册


**接口描述**:


**接口地址**:`/api/v1/home/register.do`


**请求方式**：`POST`


**consumes**:`["application/json"]`


**produces**:`["application/json"]`



**请求参数**：

| 参数名称         | 参数说明     |     in |  是否必须      |  数据类型  |  schema  |
| ------------ | -------------------------------- |-----------|--------|----|--- |
|email| 邮箱  | query | false |string  |    |
|inviterCode| 邀请码  | query | false |string  |    |
|macRegister| 注册物理地址  | query | false |string  |    |
|mobile| 手机号  | query | false |string  |    |
|nationCode| 国家电话区号  | query | false |string  |    |
|password| 登录密码  | query | true |string  |    |
|source| 来源: 来源 1PC  2PC后台  3安卓  4苹果 5微信  | query | true |string  |    |
|userSource|   | query | false |string  |    |
|valiCode| 验证码  | query | true |string  |    |

**响应示例**:

```json
{
	"code": "",
	"data": {
		"dateRegister": "",
		"email": "",
		"googleAuthCode": "",
		"inviterId": "",
		"ipRegister": "",
		"loginFailTimes": "",
		"macRegister": "",
		"mobile": "",
		"monthSendExpressNum": 0,
		"monthSignExpressNum": 0,
		"nationCode": "",
		"nickName": "",
		"realName": "",
		"sendExpressNum": 0,
		"sex": "",
		"signExpressNum": 0,
		"siteId": 0,
		"source": "",
		"token": "",
		"userCode": "",
		"userId": "",
		"userStatus": ""
	},
	"description": ""
}
```

**响应参数**:


| 参数名称         | 参数说明                             |    类型 |  schema |
| ------------ | -------------------|-------|----------- |
|code| 响应代码  |string  |    |
|data| 响应数据  |用户信息  | 用户信息   |
|description| 响应描述  |string  |    |



**schema属性说明**




**用户信息**

| 参数名称         | 参数说明                             |    类型 |  schema |
| ------------ | ------------------|--------|----------- |
|dateRegister | 注册时间   |string  |    |
|email | 邮箱   |string  |    |
|googleAuthCode | 谷歌验证码   |string  |    |
|inviterId | 邀请人ID   |string  |    |
|ipRegister | 注册IP   |string  |    |
|loginFailTimes | 当日登录失败次数   |string  |    |
|macRegister | 注册物理地址   |string  |    |
|mobile | 手机号码   |string  |    |
|monthSendExpressNum | 本月入库快递件数   |integer(int32)  |    |
|monthSignExpressNum | 本月签收快递件数   |integer(int32)  |    |
|nationCode | 国籍区号   |string  |    |
|nickName | 昵称   |string  |    |
|realName | 姓名   |string  |    |
|sendExpressNum | 今日入库快递件数   |integer(int32)  |    |
|sex | 性别 1男 2女   |string  |    |
|signExpressNum | 今日签收快递件数   |integer(int32)  |    |
|siteId | 所属站点id   |integer(int32)  |    |
|source | 注册来源 1PC 2PC后台 3安卓 4苹果 5微信   |string  |    |
|token | 用户Token   |string  |    |
|userCode | UID用户编号（自己的推广码）   |string  |    |
|userId | 用户ID   |string  |    |
|userStatus | 1正常 2锁定   |string  |    |

**响应状态**:


| 状态码         | 说明                            |    schema                         |
| ------------ | -------------------------------- |---------------------- |
| 200 | OK  |响应结果«用户信息»|
| 201 | Created  ||
| 401 | Unauthorized  ||
| 403 | Forbidden  ||
| 404 | Not Found  ||
## 修改密码


**接口描述**:


**接口地址**:`/api/v1/home/updatePassword.do`


**请求方式**：`POST`


**consumes**:`["application/json"]`


**produces**:`["application/json"]`



**请求参数**：

| 参数名称         | 参数说明     |     in |  是否必须      |  数据类型  |  schema  |
| ------------ | -------------------------------- |-----------|--------|----|--- |
|locale| 语言 zh_cn：中文   en_us：英文  | query | false |string  |    |
|mobile| 手机号，非必传  | query | false |string  |    |
|newPassword| 新密码，必传  | query | true |string  |    |
|oldPassword| 旧密码，非必传  | query | false |string  |    |
|source| 来源: 来源 1PC  2PC后台  3安卓  4苹果 5微信  | query | false |string  |    |
|token| Token  | query | false |string  |    |
|userId| 用户ID  | query | false |string  |    |
|valiCode| 验证码，非必传  | query | false |string  |    |
|validType| 验证类型：1 旧密码设置新密码 （必须登录）    2：手机号设置新密码   | query | true |string  |    |

**响应示例**:

```json
{
	"code": "",
	"data": "",
	"description": ""
}
```

**响应参数**:


| 参数名称         | 参数说明                             |    类型 |  schema |
| ------------ | -------------------|-------|----------- |
|code| 响应代码  |string  |    |
|data| 响应数据  |string  |    |
|description| 响应描述  |string  |    |





**响应状态**:


| 状态码         | 说明                            |    schema                         |
| ------------ | -------------------------------- |---------------------- |
| 200 | OK  |响应结果«string»|
| 201 | Created  ||
| 401 | Unauthorized  ||
| 403 | Forbidden  ||
| 404 | Not Found  ||
# 发送短信相关接口

## 校验手机/邮件验证码


**接口描述**:


**接口地址**:`/api/v1/message/commonVerifyCode`


**请求方式**：`GET`


**consumes**:``


**produces**:`["application/json"]`



**请求参数**：

| 参数名称         | 参数说明     |     in |  是否必须      |  数据类型  |  schema  |
| ------------ | -------------------------------- |-----------|--------|----|--- |
|ct| 防重复提交随机数  | query | false |string  |    |
|geetest_challenge| 极验验证二次验证表单数据 chllenge  | query | false |string  |    |
|geetest_seccode| 极验验证二次验证表单数据 seccode  | query | false |string  |    |
|geetest_validate| 极验验证二次验证表单数据 validate  | query | false |string  |    |
|locale| 语言种类  | query | false |string  |    |
|nationCode| 国籍区号(发送类型: 2/41[非必填], 其他必填)  | query | false |string  |    |
|platformSource| 平台来源  | query | false |string  |    |
|source| 来源: 来源 1PC  2PC后台  3安卓  4苹果 5微信  | query | true |string  |    |
|type| 发送类型: 0.手机注册; 1.邮箱注册; 2.手机修改登录密码; 3.邮箱修改登录密码; 4.绑定邮箱; 5.绑定手机; 6.修改邮箱，手机发送验证码来验证; 7.修改邮箱，邮箱发送验证验证验证旧; 8.修改邮箱，邮箱发送验证验证验证新; 9.修改手机，手机发送验证码验证旧手机; 10.修改手机，邮箱发送验证码验证旧手机; 11.修改手机，手机发送验证码验证新手机; 12.邮箱验证 修改资金密码; 13.手机验证 修改资金密码; 14.关闭邮箱验证; 15.关闭短信验证; 16.开启邮箱验证; 17.开启手机验证; 18.广告被自动撤销，发送手机短信通知; 19.广告被自动撤销，发送邮件通知; 20.提币发送短信验证; 21.提币发送邮箱验证; 22.提币已汇出，短信提醒; 23.提币已汇出，邮件提醒; 24.充币已收币，短信提醒; 25.充币已收币，邮件提醒; 26.OTC放币，短信提醒; 27.OTC放币，邮件提醒; 28.OTC付款，短信提醒; 29.OTC付款，邮件提醒; 30.被申诉，短信提醒; 31.被申诉，邮件提醒; 32.用户充值告知管理员，短信提醒; 33.用户提币申请告知管理员，短信提醒; 34.策略订单未关闭更新状态，短信提醒;35.提现异常，短信提醒; 36.提现审核通知，短信提醒; 37.用户资金对账，数据异常; 38.比特宝定期投资成功，短信提醒; 39.结算比特宝定期投资利息成功，短信提醒;40.比特宝定期产品结算异常通知管理员，短信提醒; 41.登录发送短信验证码; 42.登录发送邮件验证码; 43.开启谷歌验证，发送短信验证码;44.开启谷歌验证，发送邮件验证码; 45.关闭谷歌验证，发送短信验证码; 46.关闭谷歌验证，发送邮件验证码; 47.生成APIKEY，发送短信验证码;48.生成APIKEY，发送邮件验证码; 49.设置资金密码, 邮箱验证; 50.设置资金密码, 手机验证;  | query | true |string  |    |
|valiSign| 非法校验  | query | false |string  |    |
|verifyMethod| 手机号或者邮箱，必传  | query | true |string  |    |

**响应示例**:

```json
{
	"code": "",
	"data": "",
	"description": ""
}
```

**响应参数**:


| 参数名称         | 参数说明                             |    类型 |  schema |
| ------------ | -------------------|-------|----------- |
|code| 响应代码  |string  |    |
|data| 响应数据  |string  |    |
|description| 响应描述  |string  |    |





**响应状态**:


| 状态码         | 说明                            |    schema                         |
| ------------ | -------------------------------- |---------------------- |
| 200 | OK  |响应结果«string»|
| 401 | Unauthorized  ||
| 403 | Forbidden  ||
| 404 | Not Found  ||
## 获取手机/邮件验证码


**接口描述**:


**接口地址**:`/api/v1/message/verifyCode.do`


**请求方式**：`GET`


**consumes**:``


**produces**:`["application/json"]`



**请求参数**：

| 参数名称         | 参数说明     |     in |  是否必须      |  数据类型  |  schema  |
| ------------ | -------------------------------- |-----------|--------|----|--- |
|ct| 防重复提交随机数  | query | false |string  |    |
|geetest_challenge| 极验验证二次验证表单数据 chllenge  | query | false |string  |    |
|geetest_seccode| 极验验证二次验证表单数据 seccode  | query | false |string  |    |
|geetest_validate| 极验验证二次验证表单数据 validate  | query | false |string  |    |
|locale| 语言种类  | query | false |string  |    |
|nationCode| 国籍区号(发送类型: 2/41[非必填], 其他必填)  | query | false |string  |    |
|platformSource| 平台来源  | query | false |string  |    |
|source| 来源: 来源 1PC  2PC后台  3安卓  4苹果 5微信  | query | true |string  |    |
|type| 发送类型: 0.手机注册; 1.邮箱注册; 2.手机修改登录密码; 3.邮箱修改登录密码; 4.绑定邮箱; 5.绑定手机; 6.修改邮箱，手机发送验证码来验证; 7.修改邮箱，邮箱发送验证验证验证旧; 8.修改邮箱，邮箱发送验证验证验证新; 9.修改手机，手机发送验证码验证旧手机; 10.修改手机，邮箱发送验证码验证旧手机; 11.修改手机，手机发送验证码验证新手机; 12.邮箱验证 修改资金密码; 13.手机验证 修改资金密码; 14.关闭邮箱验证; 15.关闭短信验证; 16.开启邮箱验证; 17.开启手机验证; 18.广告被自动撤销，发送手机短信通知; 19.广告被自动撤销，发送邮件通知; 20.提币发送短信验证; 21.提币发送邮箱验证; 22.提币已汇出，短信提醒; 23.提币已汇出，邮件提醒; 24.充币已收币，短信提醒; 25.充币已收币，邮件提醒; 26.OTC放币，短信提醒; 27.OTC放币，邮件提醒; 28.OTC付款，短信提醒; 29.OTC付款，邮件提醒; 30.被申诉，短信提醒; 31.被申诉，邮件提醒; 32.用户充值告知管理员，短信提醒; 33.用户提币申请告知管理员，短信提醒; 34.策略订单未关闭更新状态，短信提醒;35.提现异常，短信提醒; 36.提现审核通知，短信提醒; 37.用户资金对账，数据异常; 38.比特宝定期投资成功，短信提醒; 39.结算比特宝定期投资利息成功，短信提醒;40.比特宝定期产品结算异常通知管理员，短信提醒; 41.登录发送短信验证码; 42.登录发送邮件验证码; 43.开启谷歌验证，发送短信验证码;44.开启谷歌验证，发送邮件验证码; 45.关闭谷歌验证，发送短信验证码; 46.关闭谷歌验证，发送邮件验证码; 47.生成APIKEY，发送短信验证码;48.生成APIKEY，发送邮件验证码; 49.设置资金密码, 邮箱验证; 50.设置资金密码, 手机验证;  | query | true |string  |    |
|valiSign| 非法校验  | query | false |string  |    |
|verifyMethod| 手机号或者邮箱，必传  | query | true |string  |    |

**响应示例**:

```json
{
	"code": "",
	"data": {},
	"description": ""
}
```

**响应参数**:


| 参数名称         | 参数说明                             |    类型 |  schema |
| ------------ | -------------------|-------|----------- |
|code| 响应代码  |string  |    |
|data| 响应数据  |object  |    |
|description| 响应描述  |string  |    |





**响应状态**:


| 状态码         | 说明                            |    schema                         |
| ------------ | -------------------------------- |---------------------- |
| 200 | OK  |响应结果|
| 401 | Unauthorized  ||
| 403 | Forbidden  ||
| 404 | Not Found  ||
# 小程序-快递用户相关接口

## 小程序-查询快递订单详情


**接口描述**:


**接口地址**:`/api/v1/express/user/findExperssUserOrderDetail.do`


**请求方式**：`POST`


**consumes**:`["application/json"]`


**produces**:`["application/json"]`



**请求参数**：

| 参数名称         | 参数说明     |     in |  是否必须      |  数据类型  |  schema  |
| ------------ | -------------------------------- |-----------|--------|----|--- |
|id| 订单id  | query | false |string  |    |
|mobile| 手机号  | query | false |string  |    |

**响应示例**:

```json
{
	"code": "",
	"data": {
		"arriveTermTime": "",
		"arriveTransTime": "",
		"expressNo": "",
		"id": "",
		"inStorageTime": "",
		"initAddr": "",
		"isSendMsg": "",
		"logistics": [
			{
				"address": "",
				"createTime": "",
				"nextAddress": "",
				"opraterMobile": "",
				"opraterName": "",
				"status": ""
			}
		],
		"mobile": "",
		"nextAddr": "",
		"price": "",
		"receiptPicUrl": "",
		"remark": "",
		"shipAddr": "",
		"signForTime": "",
		"status": "",
		"takeCode": "",
		"termAddr": ""
	},
	"description": ""
}
```

**响应参数**:


| 参数名称         | 参数说明                             |    类型 |  schema |
| ------------ | -------------------|-------|----------- |
|code| 响应代码  |string  |    |
|data| 响应数据  |FindExpressOrderDetailResp  | FindExpressOrderDetailResp   |
|description| 响应描述  |string  |    |



**schema属性说明**




**FindExpressOrderDetailResp**

| 参数名称         | 参数说明                             |    类型 |  schema |
| ------------ | ------------------|--------|----------- |
|arriveTermTime | 到达目的地时间   |string  |    |
|arriveTransTime | 到达中转站时间   |string  |    |
|expressNo | 运单号   |string  |    |
|id | id   |string  |    |
|inStorageTime | 入库时间   |string  |    |
|initAddr | 始发站（入库）   |string  |    |
|isSendMsg | 是否发送短信 1：是 2：否   |string  |    |
|logistics | 物流信息   |array  | FindExpressOrderLogisticsResp   |
|mobile | 手机号   |string  |    |
|nextAddr | 下级区域（中转）   |string  |    |
|price | 价格   |string  |    |
|receiptPicUrl | 签收图片url   |string  |    |
|remark | 备注   |string  |    |
|shipAddr | 发货区域（入库）   |string  |    |
|signForTime | 签收时间   |string  |    |
|status | 状态 1：入库待确认 2：已入库 3：到达中转站待确认 4：到达中转站 5：到达目的地 6：已签收   |string  |    |
|takeCode | 取件码   |string  |    |
|termAddr | 目的地   |string  |    |

**FindExpressOrderLogisticsResp**

| 参数名称         | 参数说明                             |    类型 |  schema |
| ------------ | ------------------|--------|----------- |
|address | 地址   |string  |    |
|createTime | 操作时间   |string  |    |
|nextAddress | 下一站地址   |string  |    |
|opraterMobile | 操作人手机号   |string  |    |
|opraterName | 操作人姓名   |string  |    |
|status | 状态 1：已入库 2：运输中 3：已达到   |string  |    |

**响应状态**:


| 状态码         | 说明                            |    schema                         |
| ------------ | -------------------------------- |---------------------- |
| 200 | OK  |响应结果«FindExpressOrderDetailResp»|
| 201 | Created  ||
| 401 | Unauthorized  ||
| 403 | Forbidden  ||
| 404 | Not Found  ||
## 小程序-根据手机号查询快递订单


**接口描述**:


**接口地址**:`/api/v1/express/user/findExpressUserOrderList.do`


**请求方式**：`POST`


**consumes**:`["application/json"]`


**produces**:`["application/json"]`



**请求参数**：

| 参数名称         | 参数说明     |     in |  是否必须      |  数据类型  |  schema  |
| ------------ | -------------------------------- |-----------|--------|----|--- |
|expressNo| 运单号  | query | false |string  |    |
|locale| 语言 zh_cn：中文   en_us：英文  | query | false |string  |    |
|mobile| 手机号  | query | false |string  |    |
|pageNo| 当前页数  | query | false |integer  |    |
|pageSize| 每页显示条数  | query | false |integer  |    |
|source| 来源: 来源 1PC  2PC后台  3安卓  4苹果 5微信  | query | false |string  |    |
|token| Token  | query | false |string  |    |
|userId| 用户ID  | query | false |string  |    |

**响应示例**:

```json
{
	"code": "",
	"data": {
		"endRow": 0,
		"hasNextPage": true,
		"hasPreviousPage": true,
		"isFirstPage": true,
		"isLastPage": true,
		"list": [
			{
				"arriveTermTime": "",
				"arriveTransTime": "",
				"expressNo": "",
				"id": "",
				"inStorageTime": "",
				"initAddr": "",
				"isSendMsg": "",
				"mobile": "",
				"nextAddr": "",
				"price": "",
				"receiptPicUrl": "",
				"remark": "",
				"shipAddr": "",
				"signForTime": "",
				"status": "",
				"takeCode": "",
				"termAddr": ""
			}
		],
		"navigateFirstPage": 0,
		"navigateLastPage": 0,
		"navigatePages": 0,
		"navigatepageNums": [],
		"nextPage": 0,
		"pageNum": 0,
		"pageSize": 0,
		"pages": 0,
		"prePage": 0,
		"size": 0,
		"startRow": 0,
		"total": 0
	},
	"description": ""
}
```

**响应参数**:


| 参数名称         | 参数说明                             |    类型 |  schema |
| ------------ | -------------------|-------|----------- |
|code| 响应代码  |string  |    |
|data| 响应数据  |PageInfo«FindExpressOrderResp»  | PageInfo«FindExpressOrderResp»   |
|description| 响应描述  |string  |    |



**schema属性说明**




**PageInfo«FindExpressOrderResp»**

| 参数名称         | 参数说明                             |    类型 |  schema |
| ------------ | ------------------|--------|----------- |
|endRow |    |integer(int32)  |    |
|hasNextPage |    |boolean  |    |
|hasPreviousPage |    |boolean  |    |
|isFirstPage |    |boolean  |    |
|isLastPage |    |boolean  |    |
|list |    |array  | FindExpressOrderResp   |
|navigateFirstPage |    |integer(int32)  |    |
|navigateLastPage |    |integer(int32)  |    |
|navigatePages |    |integer(int32)  |    |
|navigatepageNums |    |array  |    |
|nextPage |    |integer(int32)  |    |
|pageNum |    |integer(int32)  |    |
|pageSize |    |integer(int32)  |    |
|pages |    |integer(int32)  |    |
|prePage |    |integer(int32)  |    |
|size |    |integer(int32)  |    |
|startRow |    |integer(int32)  |    |
|total |    |integer(int64)  |    |

**FindExpressOrderResp**

| 参数名称         | 参数说明                             |    类型 |  schema |
| ------------ | ------------------|--------|----------- |
|arriveTermTime | 到达目的地时间   |string  |    |
|arriveTransTime | 到达中转站时间   |string  |    |
|expressNo | 运单号   |string  |    |
|id | id   |string  |    |
|inStorageTime | 入库时间   |string  |    |
|initAddr | 始发站（入库）   |string  |    |
|isSendMsg | 是否发送短信 1：是 2：否   |string  |    |
|mobile | 手机号   |string  |    |
|nextAddr | 下级区域（中转）   |string  |    |
|price | 价格   |string  |    |
|receiptPicUrl | 签收图片url   |string  |    |
|remark | 备注   |string  |    |
|shipAddr | 发货区域（入库）   |string  |    |
|signForTime | 签收时间   |string  |    |
|status | 状态 1：入库待确认 2：已入库 3：到达中转站待确认 4：到达中转站 5：到达目的地 6：已签收   |string  |    |
|takeCode | 取件码   |string  |    |
|termAddr | 目的地   |string  |    |

**响应状态**:


| 状态码         | 说明                            |    schema                         |
| ------------ | -------------------------------- |---------------------- |
| 200 | OK  |响应结果«PageInfo«FindExpressOrderResp»»|
| 201 | Created  ||
| 401 | Unauthorized  ||
| 403 | Forbidden  ||
| 404 | Not Found  ||
## 小程序-增加快递用户信息


**接口描述**:


**接口地址**:`/api/v1/express/user/insertExpressUser.do`


**请求方式**：`POST`


**consumes**:`["application/json"]`


**produces**:`["application/json"]`



**请求参数**：

| 参数名称         | 参数说明     |     in |  是否必须      |  数据类型  |  schema  |
| ------------ | -------------------------------- |-----------|--------|----|--- |
|mobile| 手机号  | query | false |string  |    |
|name| 名称  | query | false |string  |    |
|sex| 性别 1男 2女  | query | false |string  |    |

**响应示例**:

```json
{
	"code": "",
	"data": {},
	"description": ""
}
```

**响应参数**:


| 参数名称         | 参数说明                             |    类型 |  schema |
| ------------ | -------------------|-------|----------- |
|code| 响应代码  |string  |    |
|data| 响应数据  |object  |    |
|description| 响应描述  |string  |    |





**响应状态**:


| 状态码         | 说明                            |    schema                         |
| ------------ | -------------------------------- |---------------------- |
| 200 | OK  |响应结果«object»|
| 201 | Created  ||
| 401 | Unauthorized  ||
| 403 | Forbidden  ||
| 404 | Not Found  ||
# 快递订单相关接口

## 查询快递订单详情


**接口描述**:


**接口地址**:`/api/v1/express/findExpressOrderDetail.do`


**请求方式**：`POST`


**consumes**:`["application/json"]`


**produces**:`["application/json"]`



**请求参数**：

| 参数名称         | 参数说明     |     in |  是否必须      |  数据类型  |  schema  |
| ------------ | -------------------------------- |-----------|--------|----|--- |
|expressNo| 运单号  | query | false |string  |    |
|id| 订单id  | query | false |string  |    |
|locale| 语言 zh_cn：中文   en_us：英文  | query | false |string  |    |
|source| 来源: 来源 1PC  2PC后台  3安卓  4苹果 5微信  | query | false |string  |    |
|token| Token  | query | false |string  |    |
|userId| 用户ID  | query | false |string  |    |

**响应示例**:

```json
{
	"code": "",
	"data": {
		"arriveTermTime": "",
		"arriveTransTime": "",
		"expressNo": "",
		"id": "",
		"inStorageTime": "",
		"initAddr": "",
		"isSendMsg": "",
		"logistics": [
			{
				"address": "",
				"createTime": "",
				"nextAddress": "",
				"opraterMobile": "",
				"opraterName": "",
				"status": ""
			}
		],
		"mobile": "",
		"nextAddr": "",
		"price": "",
		"receiptPicUrl": "",
		"remark": "",
		"shipAddr": "",
		"signForTime": "",
		"status": "",
		"takeCode": "",
		"termAddr": ""
	},
	"description": ""
}
```

**响应参数**:


| 参数名称         | 参数说明                             |    类型 |  schema |
| ------------ | -------------------|-------|----------- |
|code| 响应代码  |string  |    |
|data| 响应数据  |FindExpressOrderDetailResp  | FindExpressOrderDetailResp   |
|description| 响应描述  |string  |    |



**schema属性说明**




**FindExpressOrderDetailResp**

| 参数名称         | 参数说明                             |    类型 |  schema |
| ------------ | ------------------|--------|----------- |
|arriveTermTime | 到达目的地时间   |string  |    |
|arriveTransTime | 到达中转站时间   |string  |    |
|expressNo | 运单号   |string  |    |
|id | id   |string  |    |
|inStorageTime | 入库时间   |string  |    |
|initAddr | 始发站（入库）   |string  |    |
|isSendMsg | 是否发送短信 1：是 2：否   |string  |    |
|logistics | 物流信息   |array  | FindExpressOrderLogisticsResp   |
|mobile | 手机号   |string  |    |
|nextAddr | 下级区域（中转）   |string  |    |
|price | 价格   |string  |    |
|receiptPicUrl | 签收图片url   |string  |    |
|remark | 备注   |string  |    |
|shipAddr | 发货区域（入库）   |string  |    |
|signForTime | 签收时间   |string  |    |
|status | 状态 1：入库待确认 2：已入库 3：到达中转站待确认 4：到达中转站 5：到达目的地 6：已签收   |string  |    |
|takeCode | 取件码   |string  |    |
|termAddr | 目的地   |string  |    |

**FindExpressOrderLogisticsResp**

| 参数名称         | 参数说明                             |    类型 |  schema |
| ------------ | ------------------|--------|----------- |
|address | 地址   |string  |    |
|createTime | 操作时间   |string  |    |
|nextAddress | 下一站地址   |string  |    |
|opraterMobile | 操作人手机号   |string  |    |
|opraterName | 操作人姓名   |string  |    |
|status | 状态 1：已入库 2：运输中 3：已达到   |string  |    |

**响应状态**:


| 状态码         | 说明                            |    schema                         |
| ------------ | -------------------------------- |---------------------- |
| 200 | OK  |响应结果«FindExpressOrderDetailResp»|
| 401 | Unauthorized  ||
| 403 | Forbidden  ||
| 404 | Not Found  ||
## 查询快递订单列表


**接口描述**:


**接口地址**:`/api/v1/express/findExpressOrderList.do`


**请求方式**：`POST`


**consumes**:`["application/json"]`


**produces**:`["application/json"]`



**请求参数**：

| 参数名称         | 参数说明     |     in |  是否必须      |  数据类型  |  schema  |
| ------------ | -------------------------------- |-----------|--------|----|--- |
|expressNo| 运单号  | query | false |string  |    |
|locale| 语言 zh_cn：中文   en_us：英文  | query | false |string  |    |
|mobile| 手机号  | query | false |string  |    |
|pageNo| 当前页数  | query | false |integer  |    |
|pageSize| 每页显示条数  | query | false |integer  |    |
|source| 来源: 来源 1PC  2PC后台  3安卓  4苹果 5微信  | query | false |string  |    |
|takeCode| 取件码  | query | false |string  |    |
|token| Token  | query | false |string  |    |
|userId| 用户ID  | query | false |string  |    |

**响应示例**:

```json
{
	"code": "",
	"data": {
		"endRow": 0,
		"hasNextPage": true,
		"hasPreviousPage": true,
		"isFirstPage": true,
		"isLastPage": true,
		"list": [
			{
				"arriveTermTime": "",
				"arriveTransTime": "",
				"expressNo": "",
				"id": "",
				"inStorageTime": "",
				"initAddr": "",
				"isSendMsg": "",
				"mobile": "",
				"nextAddr": "",
				"price": "",
				"receiptPicUrl": "",
				"remark": "",
				"shipAddr": "",
				"signForTime": "",
				"status": "",
				"takeCode": "",
				"termAddr": ""
			}
		],
		"navigateFirstPage": 0,
		"navigateLastPage": 0,
		"navigatePages": 0,
		"navigatepageNums": [],
		"nextPage": 0,
		"pageNum": 0,
		"pageSize": 0,
		"pages": 0,
		"prePage": 0,
		"size": 0,
		"startRow": 0,
		"total": 0
	},
	"description": ""
}
```

**响应参数**:


| 参数名称         | 参数说明                             |    类型 |  schema |
| ------------ | -------------------|-------|----------- |
|code| 响应代码  |string  |    |
|data| 响应数据  |PageInfo«FindExpressOrderResp»  | PageInfo«FindExpressOrderResp»   |
|description| 响应描述  |string  |    |



**schema属性说明**




**PageInfo«FindExpressOrderResp»**

| 参数名称         | 参数说明                             |    类型 |  schema |
| ------------ | ------------------|--------|----------- |
|endRow |    |integer(int32)  |    |
|hasNextPage |    |boolean  |    |
|hasPreviousPage |    |boolean  |    |
|isFirstPage |    |boolean  |    |
|isLastPage |    |boolean  |    |
|list |    |array  | FindExpressOrderResp   |
|navigateFirstPage |    |integer(int32)  |    |
|navigateLastPage |    |integer(int32)  |    |
|navigatePages |    |integer(int32)  |    |
|navigatepageNums |    |array  |    |
|nextPage |    |integer(int32)  |    |
|pageNum |    |integer(int32)  |    |
|pageSize |    |integer(int32)  |    |
|pages |    |integer(int32)  |    |
|prePage |    |integer(int32)  |    |
|size |    |integer(int32)  |    |
|startRow |    |integer(int32)  |    |
|total |    |integer(int64)  |    |

**FindExpressOrderResp**

| 参数名称         | 参数说明                             |    类型 |  schema |
| ------------ | ------------------|--------|----------- |
|arriveTermTime | 到达目的地时间   |string  |    |
|arriveTransTime | 到达中转站时间   |string  |    |
|expressNo | 运单号   |string  |    |
|id | id   |string  |    |
|inStorageTime | 入库时间   |string  |    |
|initAddr | 始发站（入库）   |string  |    |
|isSendMsg | 是否发送短信 1：是 2：否   |string  |    |
|mobile | 手机号   |string  |    |
|nextAddr | 下级区域（中转）   |string  |    |
|price | 价格   |string  |    |
|receiptPicUrl | 签收图片url   |string  |    |
|remark | 备注   |string  |    |
|shipAddr | 发货区域（入库）   |string  |    |
|signForTime | 签收时间   |string  |    |
|status | 状态 1：入库待确认 2：已入库 3：到达中转站待确认 4：到达中转站 5：到达目的地 6：已签收   |string  |    |
|takeCode | 取件码   |string  |    |
|termAddr | 目的地   |string  |    |

**响应状态**:


| 状态码         | 说明                            |    schema                         |
| ------------ | -------------------------------- |---------------------- |
| 200 | OK  |响应结果«PageInfo«FindExpressOrderResp»»|
| 401 | Unauthorized  ||
| 403 | Forbidden  ||
| 404 | Not Found  ||
## 查询快递预订单列表


**接口描述**:


**接口地址**:`/api/v1/express/findPreExpressOrderList.do`


**请求方式**：`POST`


**consumes**:`["application/json"]`


**produces**:`["application/json"]`



**请求参数**：

| 参数名称         | 参数说明     |     in |  是否必须      |  数据类型  |  schema  |
| ------------ | -------------------------------- |-----------|--------|----|--- |
|locale| 语言 zh_cn：中文   en_us：英文  | query | false |string  |    |
|source| 来源: 来源 1PC  2PC后台  3安卓  4苹果 5微信  | query | false |string  |    |
|token| Token  | query | false |string  |    |
|type| 类型， 1：入库预订单  2：中转预订单  | query | false |string  |    |
|userId| 用户ID  | query | false |string  |    |

**响应示例**:

```json
{
	"code": "",
	"data": [
		{
			"arriveTermTime": "",
			"arriveTransTime": "",
			"expressNo": "",
			"id": "",
			"inStorageTime": "",
			"initAddr": "",
			"isSendMsg": "",
			"mobile": "",
			"nextAddr": "",
			"price": "",
			"receiptPicUrl": "",
			"remark": "",
			"shipAddr": "",
			"signForTime": "",
			"status": "",
			"takeCode": "",
			"termAddr": ""
		}
	],
	"description": ""
}
```

**响应参数**:


| 参数名称         | 参数说明                             |    类型 |  schema |
| ------------ | -------------------|-------|----------- |
|code| 响应代码  |string  |    |
|data| 响应数据  |array  | FindExpressOrderResp   |
|description| 响应描述  |string  |    |



**schema属性说明**




**FindExpressOrderResp**

| 参数名称         | 参数说明                             |    类型 |  schema |
| ------------ | ------------------|--------|----------- |
|arriveTermTime | 到达目的地时间   |string  |    |
|arriveTransTime | 到达中转站时间   |string  |    |
|expressNo | 运单号   |string  |    |
|id | id   |string  |    |
|inStorageTime | 入库时间   |string  |    |
|initAddr | 始发站（入库）   |string  |    |
|isSendMsg | 是否发送短信 1：是 2：否   |string  |    |
|mobile | 手机号   |string  |    |
|nextAddr | 下级区域（中转）   |string  |    |
|price | 价格   |string  |    |
|receiptPicUrl | 签收图片url   |string  |    |
|remark | 备注   |string  |    |
|shipAddr | 发货区域（入库）   |string  |    |
|signForTime | 签收时间   |string  |    |
|status | 状态 1：入库待确认 2：已入库 3：到达中转站待确认 4：到达中转站 5：到达目的地 6：已签收   |string  |    |
|takeCode | 取件码   |string  |    |
|termAddr | 目的地   |string  |    |

**响应状态**:


| 状态码         | 说明                            |    schema                         |
| ------------ | -------------------------------- |---------------------- |
| 200 | OK  |响应结果«List«FindExpressOrderResp»»|
| 401 | Unauthorized  ||
| 403 | Forbidden  ||
| 404 | Not Found  ||
## 根据手机号查询最近一次快递站点信息


**接口描述**:


**接口地址**:`/api/v1/express/findRecentlySiteByMobile.do`


**请求方式**：`POST`


**consumes**:`["application/json"]`


**produces**:`["application/json"]`



**请求参数**：

| 参数名称         | 参数说明     |     in |  是否必须      |  数据类型  |  schema  |
| ------------ | -------------------------------- |-----------|--------|----|--- |
|locale| 语言 zh_cn：中文   en_us：英文  | query | false |string  |    |
|mobile| 手机号  | query | false |string  |    |
|source| 来源: 来源 1PC  2PC后台  3安卓  4苹果 5微信  | query | false |string  |    |
|token| Token  | query | false |string  |    |
|userId| 用户ID  | query | false |string  |    |

**响应示例**:

```json
{
	"code": "",
	"data": {
		"mobile": "",
		"shipAddr": "",
		"shipAddrId": 0
	},
	"description": ""
}
```

**响应参数**:


| 参数名称         | 参数说明                             |    类型 |  schema |
| ------------ | -------------------|-------|----------- |
|code| 响应代码  |string  |    |
|data| 响应数据  |FindRecentlySiteInfoResp  | FindRecentlySiteInfoResp   |
|description| 响应描述  |string  |    |



**schema属性说明**




**FindRecentlySiteInfoResp**

| 参数名称         | 参数说明                             |    类型 |  schema |
| ------------ | ------------------|--------|----------- |
|mobile | 手机号   |string  |    |
|shipAddr | 发货区域   |string  |    |
|shipAddrId | 发货区域站点id   |integer(int32)  |    |

**响应状态**:


| 状态码         | 说明                            |    schema                         |
| ------------ | -------------------------------- |---------------------- |
| 200 | OK  |响应结果«FindRecentlySiteInfoResp»|
| 401 | Unauthorized  ||
| 403 | Forbidden  ||
| 404 | Not Found  ||
## 获取下级站点信息列表及初始化价格


**接口描述**:


**接口地址**:`/api/v1/express/getExpressInitInfo.do`


**请求方式**：`POST`


**consumes**:`["application/json"]`


**produces**:`["application/json"]`



**请求参数**：

| 参数名称         | 参数说明     |     in |  是否必须      |  数据类型  |  schema  |
| ------------ | -------------------------------- |-----------|--------|----|--- |
|locale| 语言 zh_cn：中文   en_us：英文  | query | false |string  |    |
|source| 来源: 来源 1PC  2PC后台  3安卓  4苹果 5微信  | query | false |string  |    |
|token| Token  | query | false |string  |    |
|userId| 用户ID  | query | false |string  |    |

**响应示例**:

```json
{
	"code": "",
	"data": {
		"defaultPrice": "",
		"subSites": [
			{
				"id": "",
				"siteAddr": "",
				"siteName": ""
			}
		]
	},
	"description": ""
}
```

**响应参数**:


| 参数名称         | 参数说明                             |    类型 |  schema |
| ------------ | -------------------|-------|----------- |
|code| 响应代码  |string  |    |
|data| 响应数据  |FindExpressInitInfoResp  | FindExpressInitInfoResp   |
|description| 响应描述  |string  |    |



**schema属性说明**




**FindExpressInitInfoResp**

| 参数名称         | 参数说明                             |    类型 |  schema |
| ------------ | ------------------|--------|----------- |
|defaultPrice | 默认价格   |string  |    |
|subSites | 下级站点信息列表   |array  | FindSubSiteResp   |

**FindSubSiteResp**

| 参数名称         | 参数说明                             |    类型 |  schema |
| ------------ | ------------------|--------|----------- |
|id | id   |string  |    |
|siteAddr | 站点地址   |string  |    |
|siteName | 站点名   |string  |    |

**响应状态**:


| 状态码         | 说明                            |    schema                         |
| ------------ | -------------------------------- |---------------------- |
| 200 | OK  |响应结果«FindExpressInitInfoResp»|
| 401 | Unauthorized  ||
| 403 | Forbidden  ||
| 404 | Not Found  ||
## 入库-扫描


**接口描述**:


**接口地址**:`/api/v1/express/inStoragePrepare.do`


**请求方式**：`POST`


**consumes**:`["application/json"]`


**produces**:`["application/json"]`



**请求参数**：

| 参数名称         | 参数说明     |     in |  是否必须      |  数据类型  |  schema  |
| ------------ | -------------------------------- |-----------|--------|----|--- |
|expressNo| 运单号  | query | false |string  |    |
|id| 快递订单id，重新扫描时传  | query | false |string  |    |
|locale| 语言 zh_cn：中文   en_us：英文  | query | false |string  |    |
|mobile| 手机号  | query | false |string  |    |
|price| 价格  | query | false |string  |    |
|siteId| 发货区域站点id  | query | false |integer  |    |
|source| 来源: 来源 1PC  2PC后台  3安卓  4苹果 5微信  | query | false |string  |    |
|token| Token  | query | false |string  |    |
|userId| 用户ID  | query | false |string  |    |

**响应示例**:

```json
{
	"code": "",
	"data": {},
	"description": ""
}
```

**响应参数**:


| 参数名称         | 参数说明                             |    类型 |  schema |
| ------------ | -------------------|-------|----------- |
|code| 响应代码  |string  |    |
|data| 响应数据  |object  |    |
|description| 响应描述  |string  |    |





**响应状态**:


| 状态码         | 说明                            |    schema                         |
| ------------ | -------------------------------- |---------------------- |
| 200 | OK  |响应结果|
| 201 | Created  ||
| 401 | Unauthorized  ||
| 403 | Forbidden  ||
| 404 | Not Found  ||
## 入库-确认


**接口描述**:


**接口地址**:`/api/v1/express/inStorageSubmit.do`


**请求方式**：`POST`


**consumes**:`["application/json"]`


**produces**:`["application/json"]`



**请求参数**：

| 参数名称         | 参数说明     |     in |  是否必须      |  数据类型  |  schema  |
| ------------ | -------------------------------- |-----------|--------|----|--- |
|expressIds| 入库订单id列表  | query | false |array  | string   |
|locale| 语言 zh_cn：中文   en_us：英文  | query | false |string  |    |
|source| 来源: 来源 1PC  2PC后台  3安卓  4苹果 5微信  | query | false |string  |    |
|token| Token  | query | false |string  |    |
|userId| 用户ID  | query | false |string  |    |

**响应示例**:

```json
{
	"code": "",
	"data": {},
	"description": ""
}
```

**响应参数**:


| 参数名称         | 参数说明                             |    类型 |  schema |
| ------------ | -------------------|-------|----------- |
|code| 响应代码  |string  |    |
|data| 响应数据  |object  |    |
|description| 响应描述  |string  |    |





**响应状态**:


| 状态码         | 说明                            |    schema                         |
| ------------ | -------------------------------- |---------------------- |
| 200 | OK  |响应结果|
| 201 | Created  ||
| 401 | Unauthorized  ||
| 403 | Forbidden  ||
| 404 | Not Found  ||
## 签收


**接口描述**:


**接口地址**:`/api/v1/express/signForExpress.do`


**请求方式**：`POST`


**consumes**:`["multipart/form-data"]`


**produces**:`["application/json"]`



**请求参数**：

| 参数名称         | 参数说明     |     in |  是否必须      |  数据类型  |  schema  |
| ------------ | -------------------------------- |-----------|--------|----|--- |
|id| 订单id  | query | false |string  |    |
|locale| 语言 zh_cn：中文   en_us：英文  | query | false |string  |    |
|signPic| 签收图片  | formData | false |string  |    |
|source| 来源: 来源 1PC  2PC后台  3安卓  4苹果 5微信  | query | false |string  |    |
|token| Token  | query | false |string  |    |
|userId| 用户ID  | query | false |string  |    |

**响应示例**:

```json
{
	"code": "",
	"data": {},
	"description": ""
}
```

**响应参数**:


| 参数名称         | 参数说明                             |    类型 |  schema |
| ------------ | -------------------|-------|----------- |
|code| 响应代码  |string  |    |
|data| 响应数据  |object  |    |
|description| 响应描述  |string  |    |





**响应状态**:


| 状态码         | 说明                            |    schema                         |
| ------------ | -------------------------------- |---------------------- |
| 200 | OK  |响应结果|
| 201 | Created  ||
| 401 | Unauthorized  ||
| 403 | Forbidden  ||
| 404 | Not Found  ||
## 中转站-扫描


**接口描述**:


**接口地址**:`/api/v1/express/transStationPrepare.do`


**请求方式**：`POST`


**consumes**:`["application/json"]`


**produces**:`["application/json"]`



**请求参数**：

| 参数名称         | 参数说明     |     in |  是否必须      |  数据类型  |  schema  |
| ------------ | -------------------------------- |-----------|--------|----|--- |
|expressNo| 运单号  | query | false |string  |    |
|id| 快递订单id  | query | false |string  |    |
|isSendMsg| 是否发送短信  | query | false |boolean  |    |
|isToDestination| 是否到达目的地  | query | false |boolean  |    |
|locale| 语言 zh_cn：中文   en_us：英文  | query | false |string  |    |
|mobile| 手机号  | query | false |string  |    |
|remark| 备注  | query | false |string  |    |
|siteId| 下级城市站点id  | query | false |integer  |    |
|source| 来源: 来源 1PC  2PC后台  3安卓  4苹果 5微信  | query | false |string  |    |
|token| Token  | query | false |string  |    |
|userId| 用户ID  | query | false |string  |    |

**响应示例**:

```json
{
	"code": "",
	"data": {},
	"description": ""
}
```

**响应参数**:


| 参数名称         | 参数说明                             |    类型 |  schema |
| ------------ | -------------------|-------|----------- |
|code| 响应代码  |string  |    |
|data| 响应数据  |object  |    |
|description| 响应描述  |string  |    |





**响应状态**:


| 状态码         | 说明                            |    schema                         |
| ------------ | -------------------------------- |---------------------- |
| 200 | OK  |响应结果|
| 201 | Created  ||
| 401 | Unauthorized  ||
| 403 | Forbidden  ||
| 404 | Not Found  ||
## 中转站-确认


**接口描述**:


**接口地址**:`/api/v1/express/transStationSubmit.do`


**请求方式**：`POST`


**consumes**:`["application/json"]`


**produces**:`["application/json"]`



**请求参数**：

| 参数名称         | 参数说明     |     in |  是否必须      |  数据类型  |  schema  |
| ------------ | -------------------------------- |-----------|--------|----|--- |
|expressIds| 订单id列表  | query | false |array  | string   |
|locale| 语言 zh_cn：中文   en_us：英文  | query | false |string  |    |
|source| 来源: 来源 1PC  2PC后台  3安卓  4苹果 5微信  | query | false |string  |    |
|token| Token  | query | false |string  |    |
|userId| 用户ID  | query | false |string  |    |

**响应示例**:

```json
{
	"code": "",
	"data": {},
	"description": ""
}
```

**响应参数**:


| 参数名称         | 参数说明                             |    类型 |  schema |
| ------------ | -------------------|-------|----------- |
|code| 响应代码  |string  |    |
|data| 响应数据  |object  |    |
|description| 响应描述  |string  |    |





**响应状态**:


| 状态码         | 说明                            |    schema                         |
| ------------ | -------------------------------- |---------------------- |
| 200 | OK  |响应结果|
| 201 | Created  ||
| 401 | Unauthorized  ||
| 403 | Forbidden  ||
| 404 | Not Found  ||
# 用户相关接口

## 获取用户信息


**接口描述**:


**接口地址**:`/api/v1/user/getUserInfo.do`


**请求方式**：`GET`


**consumes**:``


**produces**:`["application/json"]`



**请求参数**：

| 参数名称         | 参数说明     |     in |  是否必须      |  数据类型  |  schema  |
| ------------ | -------------------------------- |-----------|--------|----|--- |
|locale| 语言 zh_cn：中文   en_us：英文  | query | false |string  |    |
|source| 来源: 来源 1PC  2PC后台  3安卓  4苹果 5微信  | query | false |string  |    |
|token| Token  | query | false |string  |    |
|userId| 用户ID  | query | false |string  |    |

**响应示例**:

```json
{
	"code": "",
	"data": {
		"dateRegister": "",
		"email": "",
		"googleAuthCode": "",
		"inviterId": "",
		"ipRegister": "",
		"loginFailTimes": "",
		"macRegister": "",
		"mobile": "",
		"monthSendExpressNum": 0,
		"monthSignExpressNum": 0,
		"nationCode": "",
		"nickName": "",
		"realName": "",
		"sendExpressNum": 0,
		"sex": "",
		"signExpressNum": 0,
		"siteId": 0,
		"source": "",
		"token": "",
		"userCode": "",
		"userId": "",
		"userStatus": ""
	},
	"description": ""
}
```

**响应参数**:


| 参数名称         | 参数说明                             |    类型 |  schema |
| ------------ | -------------------|-------|----------- |
|code| 响应代码  |string  |    |
|data| 响应数据  |用户信息  | 用户信息   |
|description| 响应描述  |string  |    |



**schema属性说明**




**用户信息**

| 参数名称         | 参数说明                             |    类型 |  schema |
| ------------ | ------------------|--------|----------- |
|dateRegister | 注册时间   |string  |    |
|email | 邮箱   |string  |    |
|googleAuthCode | 谷歌验证码   |string  |    |
|inviterId | 邀请人ID   |string  |    |
|ipRegister | 注册IP   |string  |    |
|loginFailTimes | 当日登录失败次数   |string  |    |
|macRegister | 注册物理地址   |string  |    |
|mobile | 手机号码   |string  |    |
|monthSendExpressNum | 本月入库快递件数   |integer(int32)  |    |
|monthSignExpressNum | 本月签收快递件数   |integer(int32)  |    |
|nationCode | 国籍区号   |string  |    |
|nickName | 昵称   |string  |    |
|realName | 姓名   |string  |    |
|sendExpressNum | 今日入库快递件数   |integer(int32)  |    |
|sex | 性别 1男 2女   |string  |    |
|signExpressNum | 今日签收快递件数   |integer(int32)  |    |
|siteId | 所属站点id   |integer(int32)  |    |
|source | 注册来源 1PC 2PC后台 3安卓 4苹果 5微信   |string  |    |
|token | 用户Token   |string  |    |
|userCode | UID用户编号（自己的推广码）   |string  |    |
|userId | 用户ID   |string  |    |
|userStatus | 1正常 2锁定   |string  |    |

**响应状态**:


| 状态码         | 说明                            |    schema                         |
| ------------ | -------------------------------- |---------------------- |
| 200 | OK  |响应结果«用户信息»|
| 401 | Unauthorized  ||
| 403 | Forbidden  ||
| 404 | Not Found  ||
## 修改用户信息


**接口描述**:


**接口地址**:`/api/v1/user/updateUser.do`


**请求方式**：`POST`


**consumes**:`["multipart/form-data"]`


**produces**:`["application/json"]`



**请求参数**：

| 参数名称         | 参数说明     |     in |  是否必须      |  数据类型  |  schema  |
| ------------ | -------------------------------- |-----------|--------|----|--- |
|headPic| 头像图片  | formData | false |string  |    |
|headPicUrl|   | query | false |string  |    |
|locale| 语言 zh_cn：中文   en_us：英文  | query | false |string  |    |
|source| 来源: 来源 1PC  2PC后台  3安卓  4苹果 5微信  | query | false |string  |    |
|token| Token  | query | false |string  |    |
|userId| 用户ID  | query | false |string  |    |

**响应示例**:

```json
{
	"code": "",
	"data": {},
	"description": ""
}
```

**响应参数**:


| 参数名称         | 参数说明                             |    类型 |  schema |
| ------------ | -------------------|-------|----------- |
|code| 响应代码  |string  |    |
|data| 响应数据  |object  |    |
|description| 响应描述  |string  |    |





**响应状态**:


| 状态码         | 说明                            |    schema                         |
| ------------ | -------------------------------- |---------------------- |
| 200 | OK  |响应结果|
| 201 | Created  ||
| 401 | Unauthorized  ||
| 403 | Forbidden  ||
| 404 | Not Found  ||
