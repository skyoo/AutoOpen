#### 思路
* 请求钉钉API 获取审批结果 落地成文件
* 每10分钟比对一次审批ID，比上一次多出来的审批ID 就是新提交的审批ID
* 通过落地的审批结果查看审批ID的状态 如果同意 则放入循环中 执行开通操作
* 开通操作调用另外一个脚本，给另外一个脚本传递用户名密码变量

#### 关于自助开通 
* svn_auto_open 有注释 其余的脚本类似，所以没有注释
* \*_approve.sh 是主脚本，负责请求接口 另外一个是负责开通操作的
* 脚本脱敏，IP和邮箱还有各种密码请求token都是乱写的，请求的URL是真的 详钉钉开放平台

 https://open.dingtalk.com/ 钉钉开放平台

