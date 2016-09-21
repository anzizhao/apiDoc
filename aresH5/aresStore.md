* [1. 获取需要帮助的商家](#getStore)
* [2. 获取已经帮助的商家](#getStore2)

<h4 id='getStore'>1. 获取需要帮助的商家</h4>

* method: GET
* url: index.php?controller=employee&action=myStores
* parameters: 
    - partner_id, 
    - employee_sn, 
    - type=last, 
    - limit=10\(请求数据数量, 默认是10\)
* retrun: 
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


<h4 id='getStore2'>2. 获取已经帮助的商家</h4>

* method: GET
* url: index.php?controller=employee&action=myStores
* parameters: partner\_id, employee\_sn, type=top, limit=10\(请求数据数量, 默认是10\)
* retrun: 
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


