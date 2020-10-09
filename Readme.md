# 功能模块
**运行程序后，显示相关信息，输入序号指令。类似下图**
![学校运动会管理系统C课程设计](http://pic2.fanwen118.com/wk-img/img17/22033889_1.jpg)
**显示默认参赛单位名称，运动员参赛项目限制，输入数字选择功能。**
* 1. 参赛项目发布
	* 显示已有项目信息
	* 输入项目信息 //空格分隔
		* 项目名称
		* 项目场地
		* 比赛时间 //输入时检测格式，大小
		* 成绩单位  //秒，米等
		* 项目名次与得分 //不知道怎么搞，现在想法是输入名次和对应得分
		* 参赛人数阈值
		* 参数人数下限（人数不足项目将被取消）
		* 参数人数上限
* 2. 运动员报名登记
	* 显示已有运动员信息
	* 输入运动员信息 //空格分隔
		* 运动员名称
		* 运动员参赛单位
		* 运动员性别
		* 参赛项目
* 3.  秩序册生成 //显示秩序册，也就是什么时候举行什么比赛，运动员是谁
* 4. 成绩录入
	* 显示所有项目，输入数字选择项目
		* 按顺序显示项目所有运动员，分别输入运动员成绩，//空格分隔，none表示弃赛，成绩为0
* 5. 运动会成绩册
* 6. 系统设置
	* 单位名称
	* 运动员参赛项目限制
* 7. 数据备份
* 8. 退出系统

# 总体布局
1. 实际使用应该是1参赛项目发布，到2运动员报名登记，一步一步按。
2. 项目用结构体变量存储，结构体包含
	    * 项目名称
		* 项目场地
		* 比赛时间
		* 成绩单位  //秒，米等
		* 项目名次与得分 //不知道怎么搞
		* 参赛人数阈值
		* 参数人数下限（人数不足项目将被取消）
		* 参数人数上限
		* 运动员名字数组
3. 用指针数组存储每一个项目的地址。
4. 运动员用结构体变量存储，结构体包含
	    * 运动员名称
		* 运动员参赛单位
		* 运动员性别
		* 参赛项目数组 //指针数组
		* 比赛成绩数组
5. 秩序册生成：通过遍历项目的比赛时间，将项目排好顺序，再同过查询项目结构体变量的运动员名字数组来生成
6. 
