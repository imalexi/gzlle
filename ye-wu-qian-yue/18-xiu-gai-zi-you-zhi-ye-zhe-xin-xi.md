### 修改自由职业者信息

---

**简要描述：**

* 在业务签约未开始的情况下，企业可以修改自由职业者基本信息

**请求头参数：**

```
Authorization: Bearer [accessToken]
```

**请求URL：**

* /contracts/employees/edit

**请求方式：**

* POST 

**请求参数说明**

| 字段名称 | 类型 | 是否必须 | 说明 |
| :--- | :--- | :--- | :--- |
| id | string | 是 | employeeId,自由职业者id和手机号码必须填一个 |
| name | string | 是 | 姓名 |
| phone | string | 是 | 登记手机号,自由职业者id和手机号码必须填一个 |
| papersType | int | 否 | 证件类型 0:身份证 |
| papersNo | string | 否 | 证件号码 |
| bankCardNo | string | 否 | 银行卡号 |
| bankPhone | string | 否 | 银行预留手机号 |
| employeeNo | string | 否 | 自由职业者在企业编号 |
| extra | string | 否 | 扩展参数 |

**返回示例**

```
成功示例:

{
    "extra": "string",
    "employeeId": "12345678"
}

失败示例:
{
    "error": "BadRequest",
    "message": "accessToken无效"
}
```

**备注**

* 更多返回错误代码请看首页的异常码描述



