* [1. 获取某类文章列表](#getList)


<h4 id='getList'>1. 获取某类文章列表</h4>

- method: GET
- url: index.php?controller=article&action=lists
- parameters:  
    - key(菜单的key,用于区分那类型的文章), 
    - type=all(查看全部文章列表), 
    - page(页码,从0开始),
    - limit=10(请求数据数量, 默认是10)
- retrun: 
        {
            error: 0,
            msg: ''
            data: {
                key: '',   //文章类型
                banner: '',    //横幅图片
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
