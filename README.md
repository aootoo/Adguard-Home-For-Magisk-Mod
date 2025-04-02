# Adguard Home For Magisk Mod
- 一个通过重定向并过滤 DNS 请求来屏蔽广告的 Magisk/KernelSU 模块
- 在官方的基础上增加了IFW规则、删除/占用广告文件夹等方法禁用广告
- 内置了8680的拦截规则并在此基础上增加了自定义规则
- 重构了模块几乎所有的底层脚本，带来更低的延迟更好的性能以及功耗优化
# 模块相比于其他的方案有哪些优点？
- 相比于私人DNS有哪些优点？
1. 私人dns需要不断的向服务器进行访问，一旦服务器超负荷或过载以及服务器连不上的话就会导致断网
2. 由于私人dns需要向服务器进行访问，所以存在很大的网络延迟问题（因为需要向服务器请求过滤以后再返回到你的设备上）
3. 私人DNS由于数据都交由服务器处理，存在的数据泄露的隐患（因为私人DNS的置信度不高）
4. 数据都在本地处理，隐私保障性更高
- 相比于Hosts有哪些优点？
1. 数据都是加密传输，并且经过Doh
2. 防止DNS劫持，防止网页被劫持的风险
3. 不容易被检测，原因同第一点
- 相比于李跳跳等无障碍跳过软件有哪些优点？
1. 不用担心会掉后台，不用担心杀后台会导致无障碍失效等问题
2. 不会因为无障碍而导致手机掉帧卡顿，因为无障碍跳过软件是实时扫描页面元素
3. 轻量化运行不用担心耗电过快的问题
4. 模块不存在应用包名被检测的问题
- 相比于Lsposed模块去广告有哪些优点？
1. 不容易被检测到，因为Lsposed去广告插件需要Hook函数注入应用
2. 本模块虽屏蔽精度不高，相比于此类插件屏蔽的广啊（因为此类模块只能屏蔽一个或十几个应用）
# 教程
- 一定要关闭或卸载其他广告拦截模块、代理模块、无障碍跳过软件、VPN代理去广告、浏览器自带广告拦截、私人DNS等等
- 如果你使用的是Magisk框架，那么点击模块旁边的操作按钮就可以进入Web UI管理器
- 使用Chash Meta导致无法正常过滤的，可以去Chash Meta设置-应用中关闭系统代理（我测试依然可以正常代理，并且广告可以过滤了）
- 测速：https://test.ustc.edu.cn/
- 测试广告拦截率（达到96%或以上是正常）：https://paileactivist.github.io/toolz/adblock.html

# 鸣谢
- [AdguardHome_magisk](https://github.com/410154425/AdGuardHome_magisk)
- [akashaProxy](https://github.com/ModuleList/akashaProxy)
- [box_for_magisk](https://github.com/taamarin/box_for_magisk)
- [AdGuardHomeForMagisk](https://github.com/twoone-3/AdGuardHomeForMagisk)
