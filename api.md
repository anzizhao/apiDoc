September 20, 2016 9:52 AM

一. 开始首页(名片)
1. 获取战神信息
- method: GET
- url: index.php?controller=employee&action=card
- parameters: partner_id, employee_sn
- retrun: 
{
		error: 0,
		msg: 'success',
		data: {
            partner_id: 12345, // 战队编号
            employee_sn: 012, // 战神编号
            partner_name: '', // 战队名称
            employee_name: '',  // 战神姓名
            employee_avatar: '', // 战神头像url
            rank: 1,  // 战神排名
            development: 0, // 开拓力
            leadership: 0, // 领导力
            influence: 0, // 影响力
            star_num:  0, // 星星个数
    	}
}


二.  我是谁



三. 秘笈
1. 菜单
- method: GET
- url: index.php?controller=article&action=menus
- parameters: 
- retrun: 
{
        error: 0,
        msg: '',
        data: {
        button: [
          {
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
                },
                ]
           }]
        }   
}

2. 推送文章信息
- method: GET
- url: index.php?controller=article&action=lists
- parameters: key(菜单的key,用于区分那类型的文章), type=recommended(首页推送列表), page(页码,从0开始)
- retrun: 
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

四. 查看全部文章页面
1. 获取某类文章列表
- method: GET
- url: index.php?controller=article&action=lists
- parameters:  key(菜单的key,用于区分那类型的文章), type=all(查看全部文章列表), page(页码,从0开始)
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

五. 文章详情
1. 获取文章下详情
- method: GET
- url: index.php?controller=article&action=view
- parameters: article_id (文章id)
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
                    tag_ids: ‘1,2,3,4,5’
             } 
}  
2. 获取推荐文章信息
- method: GET
- url: index.php?controller=article&action=listsByTags
- parameters: tags[] (tagId, ), limit=3
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

六. 战神成绩
1. 获取战神成绩
- method: GET
- url: index.php?controller=employee&action=myScores
- parameters: partner_id, employee_sn
- retrun: 
{
        error: 0,
        msg: '',
        data: {
            partner_id: 12345, // 战队id
            employee_sn: 012, // 战神编号
            new_stores_num: 0, // 拓展店数
            heat: 0, //热度
            proportion: 0, //占比
            beat_num: 0, //击败全国战神数
            one_heat: {
                rank: 0, // 热度对内排名
                number: 0, // 热度数量
                ratio: 50.55, // 热度百分比
            },   // 1热度情况
            two_heat: {
                rank: 0, // 热度对内排名
                number: 0, // 热度数量
                ratio: 50.55, // 热度百分比
            },   // 2热度情况
            three_heat: {
                rank: 0, // 热度对内排名
                number: 0, // 热度数量
                ratio: 50.55, // 热度百分比
            },   // 3热度情况
}  
   
   
七. 战神的商家
1. 获取需要帮助的商家
- method: GET
- url: index.php?controller=employee&action=myStores
- parameters: partner_id, employee_sn, type=last, limit=10
- retrun: 
{
        error: 0,
        msg: '',
        data: {
            stores:[
                {
                    store_name: '', // 店铺名称
                    proportion: '',  // 环比
                    up_or_down: '',  // 升或降, up为升 down为降
                }
            ] 
}
2. 获取已经帮助的商家
- method: GET
- url: index.php?controller=employee&action=myStores
- parameters: partner_id, employee_sn, type=top, limit=10
- retrun: 
{
        error: 0,
        msg: '',
        data: {
            stores:[
                {
                    store_name: '',  // 店铺名称
                    proportion: '',  // 环比
                    up_or_down: '',  // 升或降, up为升 down为降
                }
            ] 
}  