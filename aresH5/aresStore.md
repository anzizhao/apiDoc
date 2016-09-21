#### 1. 获取需要帮助的商家

* method: GET
* url: index.php?controller=employee&action=myStores
* parameters: partner\_id, employee\_sn, type=last, limit=10\(请求数据数量, 默认是10\)
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


#### 2.获取已经帮助的商家

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


