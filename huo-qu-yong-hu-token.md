### 获取自由职业者签约userToken

---

**简要描述：**

* 自由职业者进行电签时, 需要跳转至 职乐企服 平台进行电签, 该接口获取用户临时访问token

**请求头参数：**

```
Authorization: Bearer [accessToken]
```

**请求URL：**

* /contracts/employees/userToken/{employeeId}

**请求方式：**

* GET 

**参数：**

请求**参数说明**

| 参数 | 类型 | 是否必须 | 说明 |
| :--- | :--- | :--- | :--- |
| employeeId | string | 是 | 用户Id, 添加自由职业者接口返回 |

**返回结果示例**

```
成功示例
{
    "userToken":"[userToken]",
    "expiresIn":7200
}

失败示例
{
    "error": "BadRequest",
    "message": "accessToken无效"
}
```

**响应参数说明**

| 参数 | 类型 | 说明 |
| :--- | :--- | :--- |
| userToken | string | 企业自由职业者，进行页面签署时，需要携带的授权userToken |
| expiresIn | string | token有效时间 |



