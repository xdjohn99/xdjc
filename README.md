# xdjc
删除【fenliu1.ini】之后的 【&emoji=true&list=false&tfo=false&scv=true&fdn=false&sort=false&new_name=true】
单独分流暴雪战网、plex

# 以下代码是CFW默认自带的，不用特意再写，结合上图，按需设置策略组的选项
→ DIRECT: 直连 
→ REJECT: 该规则下不走网络活动，常用于广告拦截
→ .*: 表示加入你订阅中所有节点 
→ url-test: 表示有该代码下的节点会自动测速 ，自动选取最低延迟的节点，不可更改

# 自动归类节点 - 以图片中香港节点策略组为例
→ (港|HK|Hong Kong)
代表具有"港"，"HK"，"HongKong"关键词的节点会归类到香港节点这个策略组中，
测速以 http://www.gstatic.com/generate_204`300,,50为准。

#举例 - 正则包含并排除的写法 - 香港节点不筛选5倍节点
custom_proxy_group=🇭🇰 香港节点`url-test`(?=.*(港|HK|Hong Kong|🇭🇰|HongKong))^((?!(5.0|5倍|5x)).)*$`http://www.gstatic.com/generate_204`300,,50
