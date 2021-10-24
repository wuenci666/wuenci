中文版选项

选项	默认	描述
id(编号)	require	歌曲ID /播放列表ID /专辑ID /搜索关键字
server(平台)	require	音乐平台：netease，tencent，kugou，xiami，baidu
type（类型）	require	song，playlist，album，search，artist
auto（支持类种 类）	options	音乐链接，支持：netease，tencent，xiami
fixed（固定模式）	false	启用固定模式，默认false
mini（迷你模式）	false	启用迷你模式,默认false
autoplay（自动播放）	false	音频自动播放，默认false
theme(主题颜色)	#2980b9	默认#2980b9
loop（循环）	all	播放器循环播放，值：“all”，one”，“none”
order(顺序)	list	播放器播放顺序，值：“list”，“random”
preload(加载)	auto	值：“none”，“metadata”，“'auto”
volume（声量）	0.7	默认音量，请注意播放器会记住用户设置，用户自己设置音量后默认音量将不起作用
mutex（限制）	true	防止同时播放多个玩家，在该玩家开始播放时暂停其他玩家
lrc-type（歌词）	0	歌词显示
list-folded（列表折叠）	false	指示列表是否应该首先折叠
list-max-height（最大高度）	340px	列出最大高度
storage-name（储存名称）	metingjs	存储播放器设置的localStorage键
英文版选项

option	default	description
id	require	song id / playlist id / album id / search keyword
server	require	music platform: netease, tencent, kugou, xiami, baidu
type	require	song, playlist, album, search, artist
auto	options	music link, support: netease, tencent, xiami
fixed	false	enable fixed mode
mini	false	enable mini mode
autoplay	false	audio autoplay
theme	#2980b9	main color
loop	all	player loop play, values: 'all', 'one', 'none'
order	list	player play order, values: 'list', 'random'
preload	auto	values: 'none', 'metadata', 'auto'
volume	0.7	default volume, notice that player will remember user setting, default volume will not work after user set volume themselves
mutex	true	prevent to play multiple player at the same time, pause other players when this player start play
lrc-type	0	lyric type
list-folded	false	indicate whether list should folded at first
list-max-height	340px	list max height
storage-name	metingjs	localStorage key that store player setting



直接调用：
迷你版背景音乐
根据以上参数，写好了迷你版背景音乐，默认在左下角显示，默认列表折叠，默认不显示歌词
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8" />
		<title></title>	
	<!-- require APlayer -->
	<link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/wuenci666/wuenci@master/music/APlayer.min.css">
	<script src="https://cdn.jsdelivr.net/gh/wuenci666/wuenci@master/music/APlayer.min.js"></script>
	<!-- require MetingJS -->
	<script src="https://cdn.jsdelivr.net/gh/wuenci666/wuenci@master/music/Meting.min.js"></script>
	</head>
	<body>

<meting-js 
	server="netease" 
	type="playlist" 
	id="60198"
	fixed="true" 
	autoplay="true"
	loop="all"
	order="random"
	preload="auto"
	list-folded="ture"
	list-max-height="500px"
	lrc-type="1">
</meting-js>

	</body>
</html>
简洁调用：
<!--css-->
<link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/wuenci666/wuenci@master/music/APlayer.min.css">
<!--js-->
	<script src="https://cdn.jsdelivr.net/gh/wuenci666/wuenci@master/music/APlayer.min.js"></script>
	<script src="https://cdn.jsdelivr.net/gh/wuenci666/wuenci@master/music/Meting.min.js"></script>
        <!--使用-->
	<meting-js 
	server="netease" 
	type="playlist" 
	id="60198"
	fixed="true" 
	autoplay="true"
	loop="all"
	order="random"
	preload="auto"
	list-folded="ture"
	list-max-height="500px"
	lrc-type="1">
	</meting-js>
页脚引用：
<link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/wuenci666/wuenci@master/music/APlayer.min.css">
<script src="https://cdn.jsdelivr.net/gh/wuenci666/wuenci@master/music/APlayer.min.js"></script>
<script src="https://cdn.jsdelivr.net/gh/wuenci666/wuenci@master/music/Meting.min.js"></script>
<div>
<meting-js 
	server="netease" 
	type="playlist" 
	id="60198"
	fixed="true" 
	autoplay="true"
	loop="all"
	order="random"
	preload="auto"
	list-folded="ture"
	list-max-height="500px"
	lrc-type="1">
</meting-js>	
</div>
简单直接调用：
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8" />
		<title></title>	
	<!-- require APlayer -->
	<link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/wuenci666/wuenci@master/music/APlayer.min.css">
	<script src="https://cdn.jsdelivr.net/gh/wuenci666/wuenci@master/music/APlayer.min.js"></script>
	<!-- require MetingJS -->
	<script src="https://cdn.jsdelivr.net/gh/wuenci666/wuenci@master/music/Meting.min.js"></script>
	</head>
	<body>
<meting-js server="netease" type="playlist" id="60198"></meting-js>
	</body>
</html>
注释：
 解析：server="netease" type="playlist" id="60198"

server指音乐平台，netease指网易云音乐， type类型，playlist列表，id指歌曲的i或者专辑或列表外链id
因此重点在于指定平台，指定外链id
武恩赐制作
