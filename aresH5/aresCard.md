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
