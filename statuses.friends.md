#GET: /statuses/friends

返回用户的前100个好友

##路径

    http://api.fanfou.com/statuses/friends.[json|xml|rss]

##调用方法

    GET

##限制条件

    用户登录, 目标用户为当前用户关注者或未设置隐私

##参数:

###id

- 作用: 目标用户的id，未设置则为当前登录用户

- 格式: `id=user_id`

- 字段说明: 可选

###page

- 作用: 此api每次返回100个好友, page用于指定返回结果的页码

- 格式: `page=page_id`

- 字段说明: 可选

###callback

- 格式: callback=javascript函数名

- 作用: 当使用json格式时,生成的json对象将作为参数传给指定的javascript函数

- 字段说明: 可选

###mode

- 作用: 当`mode=default`(默认)时,返回消息中用户信息包含用户自定义profile

- 格式: `mode=mode_str`

- 字段说明: 可选

##返回结果

###成功

- HTTP Status Code

    `200 OK HTTP/1.1`

- 返回值

    * json格式

        返回一个由用户的详细信息组成的数组，用户的详细信息格式参见[[user show]](/user/show)

            {
                user_0,
                user_1,
                ...
            }