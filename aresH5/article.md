* [1. 获取文章下详情](#getDetail)
* [2. 获取推荐文章信息](#getPush)


<h4 id='getDetail'>1. 获取文章下详情</h4>

- method: GET
- url: index.php?controller=article&action=view
- parameters: 
    - article_id (文章id)
- retrun: 
        {
            error: 0,
            msg: ''
            data: {
                    article_id: '', // 文章ID
                    title: '',  // 文章标题
                    content: '', // 文章正文
                    post_date: '', // 文章发布时间
                    tags:  [
                        {
                           id: '',
                           name: '',
                        }
                    ]
                 } 
        }  


<h4 id='getPush'>2. 获取推荐文章信息</h4>
- method: GET
- url: index.php?controller=article&action=listsByTags
- parameters: 
    - tags[] (tagId, ) or  tag_ids: ‘1,2,3,4,5’
    - limit=3(请求数据数量)
- retrun: 
        {
            error: 0,
            msg: ''
            data: {
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
