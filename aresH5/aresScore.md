#### 1. 获取战神成绩
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
                    : 50.55, // 热度百分比
                },   // 2热度情况
                three_heat: {
                    rank: 0, // 热度对内排名
                    number: 0, // 热度数量
                    ratio: 50.55, // 热度百分比
                },   // 3热度情况
        }  
   
