### 页面签约跳转

---

**简要描述：**

* 自由职业者进行电签时, 是跳转至职乐企服的签约页面，跳转的url需要调用方根据参数自己构建,其中包含企业信息、自由职业者信息、自由职业者临时授权token等信息。在签署完成后,我们将在企业回跳url,以GET方式传入自由职业者信息,完成前端签约数据回调。

**跳转URL：**

* [https://webapp.gzlle.com/contract-open/spa.html](https://webapp.gzlle.com/contract-open/spa.html)

**请求方式：**

* GET 

**完整跳转URL示例：**

* [https://webapp.gzlle.com/contract-open/spa.html?employeeId=111&corpId=222&userToken=333&callbackUrl=http%3A%2F%2Fwww.baidu.com](https://webapp.gzlle.com/contract-open/spa.html?employeeId=111&corpId=222&userToken=333&callbackUrl=http%3A%2F%2Fwww.baidu.com)

**请求参数说明：**

| 参数 | 类型 | 是否必须 | 说明 |
| :--- | :--- | :--- | :--- |
| employeeId | string | 是 | 用户Id, 添加自由职业者接口返回 |
| corpId | string | 是 | 企业Id,在获取appKey的邮件里有提供. |
| userToken | string | 是 | 自由职业者电签临时授权token, 由 [1.3获取用户token](/huo-qu-yong-hu-token.md) 接口获取. |
| callbackUrl | string | 否 | 需要对callbackUrl进行url\_encode转码.当自由职业者签署完成后,前端会回跳至该链接. |
|  |  |  |  |

**回调方式：**

* GET 

**完整回跳URL示例：**

* [https://www.贵公司网址.com/?v=1&name=龙武军&employeeId=123456☎=18888888888&papersType=0&papersNo=430221198810108888&bankCardNo=6222222222222222](https://www.贵公司网址.com/?v=1&name=龙武军&employeeId=123456&phone=18888888888&papersType=0&papersNo=430221198810108888&bankCardNo=6222222222222222)

**回传参数说明：**

| 参数 | 类型 | 是否必须 | 说明 |
| :--- | :--- | :--- | :--- |
| employeeId | string | 是 | 用户Id, 添加自由职业者接口返回 |
| name | string | 否 | 姓名 |
| phone | string | 否 | 手机号码 |
| papersType | string | 否 | 证件类型,0身份证 |
| papersNo | string | 否 | 证件号码 |
| bankCardNo | string | 否 | 银行卡号 |
| employeeNo | string | 否 | 编号,企业添加时传入的值 |



