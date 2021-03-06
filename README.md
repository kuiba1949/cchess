# cchess-edit
中国象棋 PGN 棋谱生成器 (cchess-edit). 在命令行(或者终端)输入中国象棋的走法. 可用来记录对局, 或者编写棋谱

cchess-edit 

ChangeLog 版本变更说明
coding: utf-8


2017-2-03, version 0.3-1, by Careone <emacslocale@126.com>

	* 主程序名称由 cchess 变更为 cchess-edit;

	* 增加：[摆子模式]。能动态显示各种棋子的位置和数量汇总，能自动过滤无效的
	  棋子位置，或者无效的棋子数量（超过1/2/5个）。[摆子模式]结束后，能保存当前
	  棋局的 FEN 数据到 PGN 对局文件，接着开始走棋，或者进入 [评论模式]；

	* 移除：选项 --default-pos (显示默认开局的棋子布局示意图, 用彩色的中文
	  或英文字母表示);

	* 部分变量，数组名称调整和优化；


2017-2-1, version 0.2-1, by Careone <emacslocale@126.com>

	文件/目录结构变更/优化：

	* 调整并优化了部分文件的命名和目录结构，更符合 Debian 标准；

	* 打包 DEB 包时，添加了 postinst 和 postrm 文件；

	* 添加了各种常见象棋棋谱格式的 MIME 文件类型图标：
	  /usr/share/icons/hicolor/48x48/mimetypes/*.png
	
	* 部分变量，数组名称调整和优化；

	* 修复了部分图片文件权限错误（不可读，0600修正为0644）；
	
	* 使用 help2man 命令制作了简单的 man 手册文件 cchess.6.man.gz (简体中文);


	功能变更/优化：

	* 增加了选项 --default-pos (显示默认开局的棋子布局示意图, 用彩色的中文
	  或英文字母表示);

        * 增加了让子模式的走法（让子代码是以01或00开头的4位数字），并且能自动生成
	  让子后的开局 FEN 数据；
    
	* 优化了从 [评论模式] 返回 [走棋模式] 的显示效果：用彩色高亮显示
	  两种模式的状态切换；


2017-1-23, version 0.1-1, by Careone <emacslocale@126.com>
	
	* 已完成基本功能：走棋，输入评论，保存走棋记录到 PGN 对局文件;

	* 保存 PGN 对局文件时按日期（年月日）和序号自动编号，在考虑到排序和查找的
	  同时，也能有效避免文件名; 

	* 对在终端和虚拟控制台的不同使用环境，采取了适应性代码方案；
