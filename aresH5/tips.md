* [1. 获取菜单](#getmenu)
* [2. 推送文章信息](#getInfo)
* [附1. 菜单对应的Key](#key)

#### [1. 获取菜单](id:getmenu)

* method: GET
* url: index.php?controller=article&action=menus
* parameters: 
* retrun: 
  ```
    {
        error: 0,
        msg: '',
        data: {
            button: [{
                        "name":"考拉动态",
                        "sub_button":[
                            {    
                                "type":"click",  // type 为click, 前端做的一些操作
                                "name":"公司动态",
                                "key": "companyState",
                            },
                            {
                                "type":"view",    //type为view, 直接点击url跳转
                                "name":"XXXXX",
                                "url":"http://v.qq.com/"
                            }
                        ]
                    }]
               }   
        }
  ```


#### [2. 推送文章信息](id:getInfo)

* method: GET
* url: index.php?controller=article&action=lists
* parameters: key\(菜单的key,用于区分获取文章类型\), type=recommended\(首页推送列表\)
* retrun: 
  ```
    {
        error: 0,
        msg: '',
        data: {
            key: '',   // 信息类型
            link: '',   // 如果为商品信息, link返回链接, 用于查看全部的跳转, 如果为文章类型, 不返回
            articles: [
            {
                article_id: '', //文章ID
                type: 'article',  //类型, 'article'文章信息
                title: '',  //文章标题
                picture: '', // 文章图片
                link: '', // 外链, 这里不需要
                post_date: '', // 文章发布时间
            },
            {
                article_id: '', //文章ID
                type: 'link',  //类型, 'link'跳转链接
                title: '',  //文章标题
                picture: '', // 文章图片
                link: '', // 外链, 这里需要
                post_date: '', // 文章发布时间
            },
            {
                article_id: '', //文章ID
                type: 'goodsInfo',  //类型, 'goodsInfo'商品信息
                name: '',   // 商品名称 
                price: 0.00,  // 商品价格
                title: '',  //文章标题
                picture: '', // 文章图片
                link: '', //商品跳转链接
                post_date: '', // 文章发布时间
            },
            ]
        }   
    }
  ```


#### [附1. 菜单对应的Key](id:key)

```
{

 "name":"考拉动态",
 "sub_button":[
     {
        "type":"click", // type 为click, 前端做的一些操作
        "name":"公司动态",
        "key": "companyState",
     },
     {
         "type":"click", 
         "name":"产品动态",
         "key": "productState",
     },
```

{

"type":"view", \/\/type为view, 直接点击url跳转

"name":"XXXXX",

"url":"[http:\/\/v.qq.com\/](http://v.qq.com/)"

}

\]

}

