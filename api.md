September 20, 2016 9:52 AM

一. 开始首页(名片)
1. 获取战神信息
- method: GET
- url: 
- parameters: ares_id 
- retrun: 
{
		error: 0,
		msg: '',
		data: {
			id: '', // 战神id
            No: '', //序号
            name: '',  //战神姓名
            rank: 0,  //战神排名
            group: '', // 战队
            avatar: '', //战神头像  url
            marketExploration: 0, // 开拓力
            leadership: 0, // 领导力
            influence: 0, // 影响力
            star:  0, //星星个数
    	}
}


二.  我是谁



三. 秘笈
1. 菜单
- method: GET
- url: 
- parameters: 
- retrun: 
{
        error: 0,
        msg: '',
        data: {
        "button":[
          {
               "name":"考拉动态",
               "sub_button":[
               {    
                   "type":"click",  // type 为click, 前端做的一些操作
                   "name":"公司动态",
                   "key": "companyState",
                },
                {
                   "type":"view",    //type为view,直接点击url跳转
                   "name":"XXXXX",
                   "url":"http://v.qq.com/"
                },
                ]
           }]
        }   
}
2. 推送文章信息
- method: GET
- url: 
- parameters: key(菜单的key,用于区分那类型的文章)
- retrun: 
{
        error: 0,
        msg: '',
        data: {
            classify: '',   //信息类型
            link: '',   // 如果为商品信息, link返回链接,用于查看全部的跳转,如果为文章类型, 不返回
            articles: [
                {
                    id: '', //文章ID
                    type: 'article',  //类型, 有'article'文章信息, 'goodsInfo'商品信息
                    title: '',  //文章标题
                    picture: '', // 文章图片
                },
                {
                    id: '', //文章ID
                    type: 'goodsInfo',  //类型, 有'article'文章信息, 'goodsInfo'商品信息
                    name: '',   // 商品名称 
                    price: '0.00,  // 商品价格
                    title: '',  //文章标题
                    picture: '', // 文章图片
                    link: '', //商品跳转链接
                },

            ]
        }   
}

四. 查看全部文章页面
1. 获取某类文章列表
- method: GET
- url: 
- parameters:  key(菜单的key,用于区分那类型的文章)
- retrun: 
{
        error: 0,
        msg: ''
        data: {
            classify: '',   //文章类型
            banner: '',    //横幅图片
            articles: [
                {
                    id: '', //文章ID
                    title: '',  //文章标题
                    picture: '', // 文章图片
                    postDate: '', //文章发布时间

                }
            ]
        }   
}

五. 文章详情
1. 获取文章下详情
- method: GET
- url: 
- parameters: id (文章id)
- retrun: 
{
        error: 0,
        msg: ''
        data: {
                    id: '', //文章ID
                    title: '',  //文章标题
                    postDate: '', //文章发布时间
                    tags:  [
                        {
                           id: '',
                           name: '',
                        }
                    ]
             } 
}  
2. 获取推荐文章信息
- method: GET
- url: 
- parameters: tags[] (tagId, )
- retrun: 
{
        error: 0,
        msg: ''
        data: {
                    id: '', //文章ID
                    title: '',  //文章标题
                    picture: '', // 文章图片  
             } 
}

六. 战神成绩
1. 获取战神成绩
- method: GET
- url: 
- parameters: ares_id (战神id)
- retrun: 
{
        error: 0,
        msg: '',
        data: {
            id: '', // 战神id
            marketExplorationNum: 0, // 拓展店数
            heat: 0, //热度
            proportion: 0, //占比
            beatAresNumber: 0, //击败全国战神数
            oneHeat: {
                rank: 0, // 热度对内排名
                number: 0, // 热度数量
            },   // 1热度情况
            twoHeat: {
                rank: 0, // 热度对内排名
                number: 0, // 热度数量
            },   // 2热度情况
            threeHeat: {
                rank: 0, // 热度对内排名
                number: 0, // 热度数量
            },   // 热度情况
}  
   
   
七. 战神的商家
1. 获取需要帮助的商家
- method: GET
- url: 
- parameters: ares_id (战神id)
- retrun: 
{
        error: 0,
        msg: '',
        data: {
            businessmen:[
                {
                    shopName: '', //店面
                    proportion: '',  //环比
                    isUp: true,  // 是否升, true为升 false为降
                }
            ] 
}
2. 获取已经帮助的商家
- method: GET
- url: 
- parameters: ares_id (战神id)
- retrun: 
{
        error: 0,
        msg: '',
        data: {
            businessmen:[
                {
                    shopName: '', //店面
                    proportion: '',  //环比
                    isUp: true,  // 是否升, true为升 false为降
                }
            ] 
}  


