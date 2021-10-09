# masters_work
# 主人的任务<br>
学长学姐好，欢迎来看我完成的任务，因为我第一志愿是后端，所以前端页面做的不是很漂亮，请见谅(需要我做的话我也能做的漂亮(doge))<br><br>
    完成的任务：
    
            1.破冰小游戏
      介绍：输入名字的个数（暂定1-6个之间），点击生成题目，后台会随机返回一张图片的地址和题目
      会随机让你判断明星的性别或者名字（名字个数以刚刚输入的个数为准），点击提交后返回后台校验。
      如果正确则提示判断正确、自动跳到下一题，如果错误则提示错误。
      （这边我设计的是登陆注册的一张用户表，破冰小游戏又是另一张表，因为我设置了有默认头像，如果设计成一张表，
      人们注册后不上传的话会导致认脸系统体验较差，就。。强行解释下我这么设计的原因）

            2.登录注册
      采用了邮箱验证码的方式，验证码有效时长10分钟，通过加密后传到前端进行验证,
      登录鉴权系统也算比较完整的做完了，通过PHP的Session设置Cookie实现，Cookie时长三小时。
            
            3.头像上传
      简单的头像图片上传功能，支持jpeg，png，bmp，jpg，gif的图片格式，采用前后端双重验证。
      用户还可以通过设置自己头像是否在首页以及破冰小游戏中显示。
            
    
技术栈：使用了前端：html+css+js，后端php+mysql，（我知道php比较垃圾，现在正在自学别的语言）<br>
前端还使用了Vue3、Bootstrap响应式设计、jQurey等

自认为添加的细节：<br>
  前后端数据传输进行了简单的加密处理；<br>
  我的网站已经配置了SSL证书，现在访问的协议强制为HTTPS，会更加方便；<br>
  绝大部分都进行了前后端双重验证；<br>
  在做登录鉴权时，Cookie里仅保存用户的邮箱和密码，每次涉及用户账户信息修改时会把Cookie拿去验证以防止有人恶意修改Cookie去修改别人的信息；<br>
  前后端都有做一些简单的SQL过滤处理和XSS防护；<br>
  在保存头像图片时，选择保存图片名为："@用户邮箱.[图片格式]"，因为用户邮箱是主键所以既保证了不会和其他用户重名又保证了每个用户只能上传有限张图片;<br>
  <br>
  <br>
还存在的不足：<br>
  前后端数据传输中，加密采用的是base64加密，（虽然我知道这没什么用，别人一分析代码就能破解出来），之后再做网站时会将其改为更牛13一点的比如非对称加密算法，足以保证安全；<br>
  在SQL查询中，因为要查询的数据数量不多又需要防止SQL注入时，可以先将所有信息查询后放在一个数组中然后再到另一个循环里去判断它，但如果数量增多会导致查询速度变慢；<br>
  现在我的防止SQL注入还只是简单的过滤函数，有些时候会出问题，之后学到框架后可能会有更精确、过滤效果更好的框架可以使用；<br>
  发送邮箱验证码时虽然进行了加密，但是最好还是后端通过redis进行校验，最好还可以给域名加一个SSL证书让HTTP后面加个S，更安全；<br>
<br>
我已经把这个部署到我的阿里云服务器上，可以试用这个URL访问它：http://rzclould.top/masters_work/index.html ，感谢学长学姐的观看。


