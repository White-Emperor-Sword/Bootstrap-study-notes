1.栅格选择：
							超小屏	小屏>540px		中等 > 768px			大屏 > 992px			超大屏 >= 1200px
	.container最大宽度		none		540px			720px				960px				1140px
	类前缀					.col-		.col-sm-		.col-md				.col-lg-			.col-xl-
	.container-fluid		始终是100% 顶格

	整个宽度，bootstrap默认分为12块，你可以在后面跟上数字来决定它占多少 ：
		<div class="col-xl-3" style="background-color: red">1</div>   "col-xl-3" 表示它占3份
		并且你分多少份要和中间的字段结合一下，比如 col-xl-3 就是在xl宽度之上才能触发，如果不写中间字段，他就默认总是均分，自适应
		<div class="container">
			<div class="row">
				<div class="col-3" style="background-color: red">1</div>
				<div class="col-3" style="background-color: blue">2</div>
				<div class="col-3" style="background-color: yellow">3</div>
				<div class="col-3" style="background-color: pink">4</div>
			</div>
		</div>


	等宽布局：
		如果直接使用col，他就忽略自动分成的12格，更具的你需求自动划分区域
			<div class="container">
				<div class="row">
					<div class="col" style="background-color: red">1</div>
					<div class="col" style="background-color: blue">2</div>
					<div class="col" style="background-color: yellow">3</div>
					<div class="col" style="background-color: pink">4</div>
					<div class="col" style="background-color: pink">5</div>
					<div class="col" style="background-color: pink">6</div>
					<div class="col" style="background-color: pink">7</div>
					<div class="col" style="background-color: pink">8</div>
					<div class="col" style="background-color: pink">9</div>
					<div class="col" style="background-color: pink">10</div>
				</div>
			</div>

	可变宽度的弹性空间：
		根据栅格的大小自动适应边框
		<div class="col-auto" style="background-color: red">1</div>

	响应式混合布局：
		<div class="container">
			<div class="row">
				<div class="col-sm-3 col-lg-4" style="background-color: red">1</div>
				<div class="col-sm-3 col-lg-4" style="background-color: blue">2</div>
				<div class="col-sm-3 col-lg-4" style="background-color: yellow">3</div>
				<div class="col-sm-3 col-lg-4" style="background-color: pink">4</div>
			</div>
		</div>




	垂直对齐：
		1.在row上加 .align-item-start/center/end   分别是顶部对齐/居中对齐/底部对齐
			<div class="container">
				<div class="row align-item-center" style="border:3px solid #f00;height:100px;">
					<div class="col" style="background-color: red">1</div>
					<div class="col" style="background-color: blue">2</div>
					<div class="col" style="background-color: yellow">3</div>
					<div class="col" style="background-color: pink">4</div>
				</div>
			</div>



		2.在col上加 .align-self-start/center/end		分别是顶部对齐/居中对齐/底部对齐
			<div class="container">
				<div class="row align-self-center" style="border:3px solid #f00;height:100px;">
					<div class="col" style="background-color: red">1</div>
					<div class="col" style="background-color: blue">2</div>
					<div class="col" style="background-color: yellow">3</div>
					<div class="col" style="background-color: pink">4</div>
				</div>
			</div>
	


	水平对齐：
		在cow上 加  .jusity-content-start/center/end/around/between 分别是 左对齐，居中对齐，右对齐，等距对齐，两端对齐，

			<div class="container">
				<div class="row jusity-content-start" style="border:3px solid #f00;height:100px;">
					<div class="col-2" style="background-color: red">1</div>
					<div class="col-2" style="background-color: blue">2</div>
					<div class="col-2" style="background-color: yellow">3</div>
					<div class="col-2" style="background-color: pink">4</div>
				</div>
			</div>



	清除间距：
		在row上 加.no-gutters


	重排列：
		使用.order-* class选择符，可以对div空间进行 可视化排序，系统提供了 .order-1 到.order-12 12个级别的顺序

		数值越小，越排在前面，数值越大 越排在后面 order-frist默认总是在最前面


			<div class="container">
				<div class="row jusity-content-start" style="border:3px solid #f00;height:100px;">
					<div class="col-2 order-1" style="background-color: red">1</div>
					<div class="col-2 order-3" style="background-color: blue">2</div>
					<div class="col-2 order-0" style="background-color: yellow">3</div>
					<div class="col-2 order-2" style="background-color: pink">4</div>
				</div>
			</div>

	偏移：
		.offset-md-*    .offset-md-4 向右偏移4格


	margin：
		.ml-auto .mr-auto 强制隔离某两个栅格


	列嵌套：
		在已经分好的栅格内，在嵌一个 .row  在这个小的栅格内按同样的规则细分新的栅格


			<div class="container">
				<div class="row jusity-content-start" style="border:3px solid #f00;height:100px;">
					<div class="col-3" style="background-color: red">1</div>
					<div class="col-3" style="background-color: blue">2</div>
					<div class="col-3" style="background-color: yellow">3</div>
					<div class="col-3">
						<div class="row">
							<div class="col-xl-4" style="background-color:#235212">a</div>
							<div class="col-xl-8" style="background-color:#987666">b</div>
						</div>
					</div>
				</div>
			</div>


2.禁用响应式——响应式分界点：
	针对不同的设备会出现不同的显示效果，在sytle里面设置

	<style type="text/css">
		.container{
			width:1140px;
		}

		#ceb {
			font-size:16px
		}


		@media(min-width:786px) {
			#ceb {
			font-size:16px;
			color:red;
			}
		}

		@media(min-width:992px) {
			#ceb {
			font-size:16px;
			color:yellow;
			}
		}

		@media(min-width:1200px) {
			#ceb {
			font-size:16px;
			color:gray;
			}
		}
		//固定了宽度，缩小界面会出现滚动条
	</style>

	<div class="container">
		<div id="ceb">内容</div>
		<div class="row">
			<div class="col" style="background-color: red">1</div>
			<div class="col" style="background-color: blue">2</div>
			<div class="col" style="background-color: yellow">3</div>
			<div class="col" style="background-color: pink">4</div>
		</div>
	</div>



3.排版——代码：
	
	标题：html中有<h1></h1> 到 <h6></h6> 六种型号的标题，bootstrap也有六种class与H1一致，但是不会被浏览器视为元素

		<p class="h1"></p>
		<p class="h2"></p>
		<p class="h3"></p>
		<p class="h4"></p>
		<p class="h5"></p>
		<p class="h6"></p>



	副标题：<small class="text-muted">副标题，颜色变浅</small>
		<p class="h1">标题<small class="text-muted">副标题，颜色变浅</small></p>

	显式标题：比h1标题更大： <h1 class="display-1"></h1>
		<h1 class="display-1"></h1>
		<h1 class="display-2"></h1>
		<h1 class="display-3"></h1>
		<h1 class="display-4"></h1>

	中心文字高亮显示： <mark></mark>
		<p>You can use the mark tag to <mark>highlight</mark> text.</p>    



	删除线：<del></del>  <s></s>
		<p><del>This line of text is meant to be treated as deleted text.</del></p>
		<p><s>This line of text is meant to be treated as no longer accurate.</s></p>


	下划线：<ins></ins><u><u/>

		<p><ins>This line of text is meant to be treated as an addition to the document.</ins></p>
		<p><u>This line of text will render as underlined</u></p>


	加粗：<strong></strong>
		<p><strong>This line rendered as bold text.</strong></p>

	斜体：<em></em>	
		<p><em>This line rendered as italicized text.</em></p>


	分行或单行多列并排：
		<ul class="list-inline">  //去除前面的点
			<li>1</li>
			<li>2</li>
			<li>3</li>
			<li>4</li>
		</ul>

		<ul> 
			<li class="list-inline-item">1</li>  //同一行显示
			<li class="list-inline-item">2</li>
			<li class="list-inline-item">3</li>
			<li class="list-inline-item">4</li>
		</ul>

	内联代码：
		For example, <section> should be wrapped as inline.
	
		For example, <code>&lt;section&gt;</code> should be wrapped as inline.

		//页面上的文字排版布局会按这里面的排版出现


	示例标注：
		这是一个代码示例</br>
		<samp>这是一个代码实例</samp>


3.图片框：
	基本样式：

		<div class="container">
			<div class="row">
				<div class="col-md-3>
					<img src="" class="w-100%">  //撑满
				</div>

				<div class="col-md-3>
					<img src="" class="img-fluid">  //撑满
				</div>

				<div class="col-md-3>
					<img src="" class="img-thumbnail">  //缩略图样式 并且加一个圆角的、有空白的边框
				</div>
			</div>
		</div>


	图片对齐处理：


		<div class="container" style="border:1px solid #F00;" class="clearfix"> //浮动 布局  左右顶格对齐
			<img src="" class="img-thumbnail rounded">   //图片本身圆角处理
			<img src="" class="img-thumbnail">
			<img src="" class="img-thumbnail">
		</div>


		<div class="text-center">  //居中对齐
			<img src="" class="rounded d-block mx-auto">   //d-block 是display：block的简写，变为块级元素
		</div>


	图文框：  figuer 标签

		<div class="row">
			<div class="col-md-4">
				<figuer class="figuer">
					<img src="" class="img-fluid rounded">

					<figcaption class="figcaption text-center">图片下方的文字说明</figcaption>
				</figuer>
				<img src="" class="img-fluid">
			</div>
		</div>

5.表格
	


	<div class="container">
		<table class="table table-dark table-striped table-bordered">//在table标签后面加 class=“table”   就能显示行线 table-dark 设置背景颜色  table-striped 行内隔行改变颜色 table-bordered 给表格加上外边框
		table-borderless 去除所有边框 table-hover 鼠标悬停时高亮


		<caption> List of user </caption> //表格的标题，在下面显示
			<thead class="thead-light"> //class 中设置表头的颜色
				<tr>
				  <th scope="col">#</th>
				  <th scope="col">First</th>
				  <th scope="col">Last</th>
				  <th scope="col">Handle</th>
				</tr>
			</thead>
			<tbody>
				<tr>
					<th scope="row">1</th>
					<td>Mark</td>
					<td>Otto</td>
					<td>@mdo</td>
				</tr>
				<tr>
				  <th scope="row">2</th>
				  <td>Jacob</td>
				  <td>Thornton</td>
				  <td>@fat</td>
				</tr>
				<tr>
				  <th scope="row">3</th>
				  <td>Larry</td>
				  <td>the Bird</td>
				  <td>@twitter</td>
				</tr>
			</tbody>
		</table>
	</div>


	显示不同颜色：
		<tr class="table-active">...</tr>

		<tr class="table-primary">...</tr>
		<tr class="table-secondary">...</tr>
		<tr class="table-success">...</tr>
		<tr class="table-danger">...</tr>
		<tr class="table-warning">...</tr>
		<tr class="table-info">...</tr>
		<tr class="table-light">...</tr>
		<tr class="table-dark">...</tr>

		<!-- On cells (`td` or `th`) -->
		<tr>
		  <td class="table-active">...</td>
		  
		  <td class="table-primary">...</td>
		  <td class="table-secondary">...</td>
		  <td class="table-success">...</td>
		  <td class="table-danger">...</td>
		  <td class="table-warning">...</td>
		  <td class="table-info">...</td>
		  <td class="table-light">...</td>
		  <td class="table-dark">...</td>
		</tr>

		如果要改成深色的背景，把talbe 换成bg

	响应式的滚动条：
		如果框太长，在div内生成一个可以拉动的滚动条： 使用class="table-responsive"
		<div class="table-responsive">
		  <table class="table">
		    ...
		  </table>
		</div>


6.边框-浮动：
	添加一个边框：  class="border"
	设置不同边框颜色：calss="border border-primary/secondary/success/danger/warning/info/light/dark" 
	设置圆角：class="rounded"   其中 rounded-top/left/right/bottom 设置上下左右的角变圆角 rounded-circle整个就编一个圆了 rounded-pill 操场形状



7.颜色-display属性：

	文本颜色：<p class="text-primary">text-primary</p>
			<p class="text-secondary">text-secondary</p>
			<p class="text-success">text-success</p>
			<p class="text-danger">text-danger</p>
			<p class="text-warning">text-warning</p>
			<p class="text-info">text-info</p>
			<p class="text-light">text-light</p>
			<p class="text-light">text-dark</p>



	塞进链接中 一样可以添加
		<p><a href='#' calss="text-secondary">text-dark</a></p>



	背景颜色：
		<p class="bg-secondary text-primary">text-primary</p>
		<p class="bg-primary text-secondary">text-secondary</p>
		<p class="bg-secondary text-success">text-success</p>
		<p class="bg-success text-danger">text-danger</p>
		<p class="bg-danger text-warning">text-warning</p>
		<p class="bg-warning text-info">text-info</p>
		<p class="bg-info text-light">text-light</p>
		<p class="bg-light text-light">text-dark</p>


	Display显示属性：
		常用属性：none、隐藏属性
				inline、变为行内属性并共享一行，不能更改元素的height，width的值，大小由内容撑开
				block、使元素变成块级元素，独占一行，能够改变元素的height，width的值
				inline-block、不独占一行的块级元素
				table、元素会作为块级表格来显示，类似<table>，表格前后带有换行符
				table-cell、元素会作为一个表格单元格显示，类似<td>和<th>
				table-row、元素会作为一个表格行显示，类似<tr>
				flex、
				inline-flex 

				变为行内属性并共享一行




			<div class="container">
				<div>111</div>
				<div class="d-none">111</div>

			</div>


8.文本处理-垂直对齐规格与尺寸：
	class="text-center" 文本居中
	class="text-left"	文本左对齐
	class="text-right"	文本右对齐

	class="text-justify"  处理文本，不留空
	class="text-nowarp" 文本不换行
	class="d-inline-block text-truncate"  以省略号截断文本，要结合 d-inlineblock 或者 d-block使用


	class="text-lowercase" 集体小写
	class="text-uppercase"	集体大写
	class="text-capitalize" 首字母大写

	class="font-weight-bold" 字体加粗
	class="font-weight-light" 浅
	class="font-weight-normal" 
	class="font-italic" 斜体


	垂直对齐： class="align-baseline/top/middle/bottom/text-bottom/text-top"
		也可以再table里面用
		align-middle 比较常用 垂直居中


	规格与尺寸：
		宽度和高度可以用 w/h-25/50/75/100 来配置

9.间隔和阴影：
	间隔：
		class="p/pt/pb/pl/pr-1/2/3/4/5"
		class="m/mb/mt/ml/mr-1/2/3/4/5/6"

	阴影：
		style="boxshadow:10px 10px 5px #eee;" 前两个是从x、y轴延申的距离 第三个是模糊度 
		class="shadow "
		class="shadow-sm"
		class="shadow-lg" 控制阴影大小
		class="shadow-none"


10.定位-显示或隐藏-关闭图标

	header 标签  顶部导航栏 可以设置class="fixed-top/sticky-top"  永远出现在顶部 

	footer 标签  页脚导航栏


	class="invisible"隐藏
	class="visible"显示


	<button type="button" class="close">   关闭按钮
	<a href="" class="close"></a>


11.嵌入-图像替换-读凭器：
	嵌入：
		长宽比例处理：  class="embed-responsive-21by9/16by9/4by3/1by1"  长宽比 21：9/16：9/4：3/1：1


		<div class="embed-responsive-21by9">
			<iframe src="" class="embed-responsive-item></iframe>  //里面的对象可以有iframe embed video object
		</div>


	图像替换：
		<h1 class="text-hide" style="background-image.url('ip')"></h1> 
		//作用就是html会认为是一个h1标签 但实际上是显示的图片，这样可以优化搜索引擎的检索


12.flex 弹性布局：

	<div class="display:flex"></div>

	父级：
		启用：display：flex/inline-flex

		方向：flex-row 从左向右  flex-row-reverse 从右向左 flex-column 从上到下 flex-column-reverse 从下到上

		对齐：jusitify-content-start/center/end/between/around 左对齐 居中对齐 右对齐 两端对齐 等距对齐

		对齐项目：align-items-stretch/start/center/end/baseline 默认 顶部对齐 中部对齐 底部对齐 文本处于统一条线

		wrap包裹：flex-nowrap/warp/wrap-reverse 默认不会自动换行  自动换行 反向换行

		对齐内容：align-content-start/center/end/around 以文本为对齐标准


	子元素：在每一个item里面分别设置他的class
		自动对齐：align-self-stretch/start/center/end/baseline
		自相等：flex-fill  沾满剩余所有宽度
		等宽变换：flex-grow-0/1  沾满剩余宽度
		缩小能力：flex-shrink-1/0 然他保持原有的宽度 这个还蛮重要的，鼠标悬停的时候变大
		order排序：order-0~12 越小越靠前 等于设置权重



13.组件之警告提示框： class="alert alert-primary" role="alert"
	可以在里面添加其他标签和内容

	<div class="alert alert-primary" role="alert">
	  A simple primary alert—check it out!
	</div>

	<div class="alert alert-secondary" role="alert">
	  A simple secondary alert—check it out!
	</div>

	<div class="alert alert-success" role="alert">
	  A simple success alert—check it out!
	</div>

	<div class="alert alert-danger" role="alert">
	  A simple danger alert—check it out!
	</div>

	<div class="alert alert-warning" role="alert">
	  A simple warning alert—check it out!
	</div>

	<div class="alert alert-info" role="alert">
	  A simple info alert—check it out!
	</div>

	<div class="alert alert-light" role="alert">
	  A simple light alert—check it out!
	</div>

	<div class="alert alert-dark" role="alert">
	  A simple dark alert—check it out!
	</div>

	使用的时候可以与js事件绑定

	<button type="button" class="close" data-dismiss="alert" fade show>&time</button>
	//data-dismiss能移除整个alert 的DOM元素 
	//fade show 淡出效果

14.徽章——面包屑导航
	可作为链接或者按钮的一部分，以提供统计数字样式

	<span class="badge badge-secondary">New</span>
	<span class="badge badge-pill badge-secondary">New</span> 胶囊式

	也可以在连接上使用
	<a href="#" class="badge badge-pill badge-secondary">new</a>


	面包屑：
		<ul class="breadcrumb">  面包屑导航栏
			<li class="breadcrumb-item active"></li> 加入active 当前页变灰色
		</ul>

15.button按钮：

	<div class="btn-group" role="group" aria-label="Basic example">
		<button type="button" class="btn btn-secondary">Left</button>
		<button type="button" class="btn btn-secondary">Middle</button>
		<button type="button" class="btn btn-secondary">Right</button>

		//也可以加在submit reset a标签 上面
		<button type="submit" class="btn btn-secondary">Middle</button>
		<button type="reset" class="btn btn-secondary">Middle</button>
		<a href="#" class="btn btn-secondary"></a>
	</div>

	轮廓按钮：只是边框有颜色，悬停有颜色变化
		class="btn-outline-secondary"

	大小和尺寸：
		btn-block 撑满全屏  在移动端非常有用
		btn-sm btn-lg

	禁用与启用状态：
		disabled 和 active
		<button type="button" class="btn btn-secondary disabled">Middle</button>
		<button type="button" class="btn btn-secondary active">Middle</button>

	点击切换启用 状态：
		data-toggle="button"

		<button type="button" class="btn btn-secondary" data-toggle="button">Middle</button>

	复选和单选框：
		复选：
			<div class="btn-group" data-toggle="button">
				<label class="btn btn-secondary">
					<input type="checkbox" name="checkbox[]" id="">Java
				</label>
				<label class="btn btn-secondary">
					<input type="checkbox" name="checkbox[]" id="">JS
				</label>
				<label class="btn btn-secondary">
					<input type="checkbox" name="checkbox[]" id="">Python
				</label>

			</div>

		单选：
			<div class="btn-group" data-toggle="button">
				<label class="btn btn-secondary">
					<input type="radio" name="radio" id="">Java
				</label>
				<label class="btn btn-secondary">
					<input type="radio" name="radio" id="">JS
				</label>
				<label class="btn btn-secondary">
					<input type="radio" name="radio" id="">Python
				</label>

			</div>

		bs4 还提供了一种新样式，更加简洁：
			class="btn-group-toggle"

			<div class="btn-group btn-group-toggle" data-toggle="button">
				<label class="btn btn-secondary">
					<input type="radio" name="radio" id="">Java
				</label>
				<label class="btn btn-secondary">
					<input type="radio" name="radio" id="">JS
				</label>
				<label class="btn btn-secondary">
					<input type="radio" name="radio" id="">Python
				</label>

			</div>


16.下拉菜单： 下拉菜单组件、提示组件、冒泡组件等都依赖于popper.js
	class="dropdown-toggle"

	<div class="dropdown">
		<button class="btn btn-primary dropdown-toggle" data-toggle="dropdown">Dropdown</button>
		<div class="dropdown-menu">
			<a href="" class="dorpdown-item">aaa</a>
			<a href="" class="dorpdown-item">bbb</a>
			<a href="" class="dorpdown-item">ccc</a>
		</div>
	</div>



	role="group" 使整个菜单变成行内元素


	<div class="btn-group" role="group">
    <button id="btnGroupDrop1" type="button" class="btn btn-secondary dropdown-toggle" data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
      Dropdown
    </button>
    <div class="dropdown-menu" aria-labelledby="btnGroupDrop1">
      <a class="dropdown-item" href="#">Dropdown link</a>
      <a class="dropdown-item" href="#">Dropdown link</a>
    </div>
  	</div>


  	class="dropdown-toggle-split"  将菜单与箭头分开


  	尺寸大小：
  		btn-sm btn-lg


  	有效和不可用：
  		active disabled


  	响应式对齐：默认是左边对齐的
  		class="drop-menu-right"  右边对齐

  	分割线：
  		<div class="drop-divier"></div>

  	Javascript事件：
  		 $.('#id').on('show.bs.dropdown',function(){
  		 	调用show显示方法时触发事件
  		});

  		 $.('#id').on('show.bs.dropdown',function(){
  		 	当下拉菜单对用户可见时触发事件
  		});

  		 $.('#id').on('hide.bs.dropdown',function(){
  		 	调用隐藏实例方法时触发事件
  		});

  		 $.('#id').on('hidden.bs.dropdown',function(){
  		 	下拉菜单完全隐藏时触发事件
  		})


17.按钮组：
	
	此为连在一起的三个按钮组成的按钮组
	<div class="btn-group" role="group" aria-label="Basic example">
		<button type="button" class="btn btn-secondary">Left</button>
		<button type="button" class="btn btn-secondary">Middle</button>
		<button type="button" class="btn btn-secondary">Right</button>
	</div>

	按钮工具栏：

		<div class="btn-toolbar">
			<div class="btn-group">
				<button type="button" class="btn btn-secondary">1</button>
				<button type="button" class="btn btn-secondary">2</button>
				<button type="button" class="btn btn-secondary">3</button>
			</div>

			<div class="btn-group">
				<button type="button" class="btn btn-secondary">4</button>
				<button type="button" class="btn btn-secondary">5</button>
				<button type="button" class="btn btn-secondary">6</button>
			</div>

			<div clas="btn-group">
				<button type="button" class="btn btn-secondary">7</button>
			</div>
		</div>


	嵌套：可以正常按钮与group混用

	<div class="btn-group" role="group" aria-label="Button group with nested dropdown">
	  <button type="button" class="btn btn-secondary">1</button>
	  <button type="button" class="btn btn-secondary">2</button>

	  <div class="btn-group" role="group">
	    <button id="btnGroupDrop1" type="button" class="btn btn-secondary dropdown-toggle" data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
	      Dropdown
	    </button>
	    <div class="dropdown-menu" aria-labelledby="btnGroupDrop1">
	      <a class="dropdown-item" href="#">Dropdown link</a>
	      <a class="dropdown-item" href="#">Dropdown link</a>
	    </div>
	  </div>
	</div>



	改为垂直排列：
		<div class="btn-group-vertical">

18.input输入框及输入群组：

	input框前添加其他说明：  class="input-group mb-3" 所包裹的内容会在用一行显示
		<div class="input-group mb-3">
	  		<div class="input-group-prepend">
	    		<span class="input-group-text" id="basic-addon1">@</span>
	  		</div>
	  		<input type="text" class="form-control" placeholder="Username" aria-label="Username" aria-describedby="basic-addon1">
		</div>


	也可以在尾部添加：
		<div class="input-group mb-3">
  			<input type="text" class="form-control" placeholder="Recipient's username" aria-label="Recipient's username" aria-describedby="basic-addon2">
  			<div class="input-group-append">
    			<span class="input-group-text" id="basic-addon2">@example.com</span>
  			</div>
		</div>


	控制输入框的页脚：<textarea class="form-control" aria-label="With textarea"></textarea>
		<div class="input-group">
  			<div class="input-group-prepend">
    			<span class="input-group-text">With textarea</span>
  			</div>
		<textarea class="form-control" aria-label="With textarea"></textarea>
		</div>



	输入组插件：

		勾选或者单选框：
			多选：
			<div class="input-group mb-3">
  				<div class="input-group-prepend">
    				<div class="input-group-text">
      					<input type="checkbox" aria-label="Checkbox for following text input">
    				</div>
  				</div>
  				<input type="text" class="form-control" aria-label="Text input with checkbox">
			</div>


			单选：
			<div class="input-group">
				<div class="input-group-prepend">
    				<div class="input-group-text">
      					<input type="radio" aria-label="Radio button for following text input">
    				</div>
  				</div>
  				<input type="text" class="form-control" aria-label="Text input with radio button">
			</div>


		按扭组合：可以在里面放button按钮，也可以放入下拉菜单，其他设置与上面的一致：
			<div class="input-group mb-3">
  				<div class="input-group-prepend">
    				<button class="btn btn-outline-secondary" type="button" id="button-addon1">Button</button>
  				</div>
  				<input type="text" class="form-control" placeholder="" aria-label="Example text with button addon" aria-describedby="button-addon1">
			</div>

		下拉菜单：
			<div class="input-group mb-3">
  				<div class="input-group-prepend">
    				<button class="btn btn-outline-secondary dropdown-toggle" type="button" data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">Dropdown</button>
    					<div class="dropdown-menu">
					      <a class="dropdown-item" href="#">Action</a>
					      <a class="dropdown-item" href="#">Another action</a>
					      <a class="dropdown-item" href="#">Something else here</a>
      						<div role="separator" class="dropdown-divider"></div>
      						<a class="dropdown-item" href="#">Separated link</a>
    					</div>
  				</div>
  				<input type="text" class="form-control" aria-label="Text input with dropdown button">
			</div>


	放入自定义表单：
		<div class="input-group mb-3">
  			<div class="input-group-prepend">
    			<label class="input-group-text" for="inputGroupSelect01">Options</label>
  			</div>
  			<select class="custom-select" id="inputGroupSelect01">
			    <option selected>Choose...</option>
			    <option value="1">One</option>
			    <option value="2">Two</option>
			    <option value="3">Three</option>
  			</select>
		</div>

	选择文件上传：
		<div class="input-group mb-3">
			<div class="input-group-prepend">
				<span class="input-group-text" id="inputGroupFileAddon01">Upload</span>
  			</div>
  			<div class="custom-file">
    		<input type="file" class="custom-file-input" id="inputGroupFile01" aria-describedby="inputGroupFileAddon01">
    		<label class="custom-file-label" for="inputGroupFile01">Choose file</label>
  			</div>
		</div>


19.表单：
	基本使用：文本控件<input>,<select>,<textarea>，采用form-control优化处理
				所有文本都在form-group的div中


		<form>
  			<div class="form-group">  
			    <label for="exampleInputEmail1">Email address</label>
			    <input type="email" class="form-control" id="exampleInputEmail1" aria-describedby="emailHelp">
			    <small id="emailHelp" class="form-text text-muted">We'll never share your email with anyone else.</small>  //小号字体文本说明
 			</div>
  			<div class="form-group">
			    <label for="exampleInputPassword1">Password</label>
			    <input type="password" class="form-control" id="exampleInputPassword1">
  			</div>
			<div class="form-group form-check">
				<input type="checkbox" class="form-check-input" id="exampleCheck1">
				<label class="form-check-label" for="exampleCheck1">Check me out</label>
			</div>
  			<button type="submit" class="btn btn-primary">Submit</button>
		</form>


	结合按钮组 添加选择框：
		<form>
  			<div class="form-group">
			    <label for="exampleFormControlInput1">Email address</label>
			    <input type="email" class="form-control" id="exampleFormControlInput1" placeholder="name@example.com">
  			</div>

		  <div class="form-group">
		    <label for="exampleFormControlSelect1">Example select</label>
		    <select class="form-control" id="exampleFormControlSelect1">
		      <option>1</option>
		      <option>2</option>
		      <option>3</option>
		      <option>4</option>
		      <option>5</option>
		    </select>
		  </div>

		  <div class="form-group">
		    <label for="exampleFormControlSelect2">Example multiple select</label>
		    <select multiple class="form-control" id="exampleFormControlSelect2">
		      <option>1</option>
		      <option>2</option>
		      <option>3</option>
		      <option>4</option>
		      <option>5</option>
		    </select>
		  </div>
		  

		  <div class="form-group">
		    <label for="exampleFormControlTextarea1">Example textarea</label>
		    <textarea class="form-control" id="exampleFormControlTextarea1" rows="3"></textarea>
		  </div>
		</form>


	select菜单：自定义<select>菜单仅需要一个自定义类.custom-select即可触发自定义样式。自定义样式仅限于<select>的初始外观，由于浏览器的限制，无法修改<option>。
		<select class="custom-select">
		  <option selected>Open this select menu</option>
		  <option value="1">One</option>
		  <option value="2">Two</option>
		  <option value="3">Three</option>
		</select>

		添加multiple


	调整大小： sm lg 调整大小  placeholder 框内说明文字
		<input class="form-control form-control-lg" type="text" placeholder=".form-control-lg"> 
		<input class="form-control" type="text" placeholder="Default input">
		<input class="form-control form-control-sm" type="text" placeholder=".form-control-sm">


	select选择框：
		<select class="form-control form-control-lg">
		  <option>Large select</option>
		</select>
		<select class="form-control">
		  <option>Default select</option>
		</select>
		<select class="form-control form-control-sm">
		  <option>Small select</option>
		</select>

	只读：添加 readonly 属性
		<input class="form-control" type="text" placeholder="Readonly input here..." readonly>


	只读纯文本：如果要在表单中将<input readonly>元素设置为纯文本样式，请使用.form-control-plaintext类删除默认的表单字段样式，并保留正确的边距和填充。 

		<form class="form-inline">
		  <div class="form-group mb-2">
		    <label for="staticEmail2" class="sr-only">Email</label>
		    <input type="text" readonly class="form-control-plaintext" id="staticEmail2" value="email@example.com">
		  </div>
		  <div class="form-group mx-sm-3 mb-2">
		    <label for="inputPassword2" class="sr-only">Password</label>
		    <input type="password" class="form-control" id="inputPassword2" placeholder="Password">
		  </div>
		  <button type="submit" class="btn btn-primary mb-2">Confirm identity</button>
		</form>

	范围输入：水平滚动条，使用.form-control-range设置水平滚动范围输入。

		<form>
		  <div class="form-group">
		    <label for="formControlRange">Example Range input</label>
		    <input type="range" class="form-control-range" id="formControlRange">
		  </div>
		</form>



	复选和单选框：
		借助.form-check对默认复选框和单选框进行了改进，

		复选：checkbox
			<div class="form-check">
			  <input class="form-check-input" type="checkbox" value="" id="defaultCheck1">
			  <label class="form-check-label" for="defaultCheck1">
			    Default checkbox
			  </label>
			</div>
			<div class="form-check">
			  <input class="form-check-input" type="checkbox" value="" id="defaultCheck2" disabled>
			  <label class="form-check-label" for="defaultCheck2">
			    Disabled checkbox
			  </label>
			</div>


		单选：label
		<div class="form-check">
		  <input class="form-check-input" type="radio" name="exampleRadios" id="exampleRadios1" value="option1" checked>
		  <label class="form-check-label" for="exampleRadios1">
		    Default radio
		  </label>
		</div>
		<div class="form-check">
		  <input class="form-check-input" type="radio" name="exampleRadios" id="exampleRadios2" value="option2">
		  <label class="form-check-label" for="exampleRadios2">
		    Second default radio
		  </label>
		</div>
		<div class="form-check">
		  <input class="form-check-input" type="radio" name="exampleRadios" id="exampleRadios3" value="option3" disabled>
		  <label class="form-check-label" for="exampleRadios3">
		    Disabled radio
		  </label>
		</div>


	通过将.form-check-inline添加到任何.form-check中，将复选框或单选框分组在同一水平行上。

	表格网格：可以使用我们的网格类构建更复杂的表单。将它们用于需要多列，可变宽度和其他对齐选项的表单布局。

		<form>
		  <div class="row">
		    <div class="col">
		      <input type="text" class="form-control" placeholder="First name">
		    </div>
		    <div class="col">
		      <input type="text" class="form-control" placeholder="Last name">
		    </div>
		  </div>
		</form>


		表格行：您也可以将.row替换为.form-row，这是我们标准网格行的一种变体，它覆盖了默认的列装订线，以实现更紧凑，更紧凑的布局。
			<form>
			  <div class="form-row">
			    <div class="col">
			      <input type="text" class="form-control" placeholder="First name">
			    </div>
			    <div class="col">
			      <input type="text" class="form-control" placeholder="Last name">
			    </div>
			  </div>
			</form>


	提示成功和非法：添加验证手段，使用.is-invalid和.is-valid指示无效和有效的表单字段。这些类也支持.invalid-feedback
		<form>
			<div class="form-row">
				<div class="col-md-4 mb-3">
			      <label for="validationServer01">First name</label>
			      <input type="text" class="form-control is-valid" id="validationServer01" value="Mark" required>
			      <div class="valid-feedback">
			        Looks good!
			      </div>  //这一部分添加控制语句显示
			    </div>
			</div>


			<div class="col-md-6 mb-3">
		      <label for="validationServer03">City</label>
		      <input type="text" class="form-control is-invalid" id="validationServer03" required>
		      <div class="invalid-feedback">
		        Please provide a valid city.
		      </div>  //失败提示
		    </div>

		</form>


	Switches开关：自定义复选框的标记，但是使用.custom-switch类来呈现切换开关。开关还支持disabled属性。
		<div class="custom-control custom-switch">
		  <input type="checkbox" class="custom-control-input" id="customSwitch1">
		  <label class="custom-control-label" for="customSwitch1">Toggle this switch element</label>
		</div>
		<div class="custom-control custom-switch">
		  <input type="checkbox" class="custom-control-input" disabled id="customSwitch2">
		  <label class="custom-control-label" for="customSwitch2">Disabled switch element</label>
		</div>



20.轮播图（carousel）：class="carousel slide" data-ride="carousel"
	基本样式：只带有幻灯片的旋转木马。轮播图片上存在.d-block和.w-100，以防止浏览器默认图片对齐。

		data-ride="carousel" 默认5秒切换一次，但是效果很干 class="slide" 相对丝滑一点 data-interval="1000" 控制时间单位 ms

		<div id="carouselExampleSlidesOnly" class="carousel slide" data-ride="carousel">
		  <div class="carousel-inner">
		    <div class="carousel-item active">
		        <img src="..." class="d-block w-100" alt="...">
		    </div>
		    <div class="carousel-item">
		      <img src="..." class="d-block w-100" alt="...">
		    </div>
		    <div class="carousel-item">
		      <img src="..." class="d-block w-100" alt="...">
		    </div>
		  </div>
		</div>




	添加上一个和下一个控件：
		href="#carouselExampleControls" 需要和图片的id绑定

		<div id="carouselExampleControls" class="carousel slide" data-ride="carousel">
		  <div class="carousel-inner">
		    <div class="carousel-item active">
		      <img src="..." class="d-block w-100" alt="...">
		    </div>
		    <div class="carousel-item">
		      <img src="..." class="d-block w-100" alt="...">
		    </div>
		    <div class="carousel-item">
		      <img src="..." class="d-block w-100" alt="...">
		    </div>
		  </div>
		  <a class="carousel-control-prev" href="#carouselExampleControls" role="button" data-slide="prev">
		    <span class="carousel-control-prev-icon" aria-hidden="true"></span>
		    <span class="sr-only">Previous</span>
		  </a>
		  <a class="carousel-control-next" href="#carouselExampleControls" role="button" data-slide="next">
		    <span class="carousel-control-next-icon" aria-hidden="true"></span>
		    <span class="sr-only">Next</span>
		  </a>
		</div>



	再加选择框： 
		<div id="carouselExampleIndicators" class="carousel slide" data-ride="carousel">
		  <ol class="carousel-indicators">
		    <li data-target="#carouselExampleIndicators" data-slide-to="0" class="active"></li>
		    <li data-target="#carouselExampleIndicators" data-slide-to="1"></li>
		    <li data-target="#carouselExampleIndicators" data-slide-to="2"></li>
		  </ol>
		  <div class="carousel-inner">
		    <div class="carousel-item active">
		      <img src="..." class="d-block w-100" alt="...">
		    </div>
		    <div class="carousel-item">
		      <img src="..." class="d-block w-100" alt="...">
		    </div>
		    <div class="carousel-item">
		      <img src="..." class="d-block w-100" alt="...">
		    </div>
		  </div>
		  <a class="carousel-control-prev" href="#carouselExampleIndicators" role="button" data-slide="prev">
		    <span class="carousel-control-prev-icon" aria-hidden="true"></span>
		    <span class="sr-only">Previous</span>
		  </a>
		  <a class="carousel-control-next" href="#carouselExampleIndicators" role="button" data-slide="next">
		    <span class="carousel-control-next-icon" aria-hidden="true"></span>
		    <span class="sr-only">Next</span>
		  </a>
		</div>



	再带字幕：使用.carousel-item中的.carousel-caption元素，可以轻将字幕添加到幻灯片中。
		<div id="carouselExampleCaptions" class="carousel slide" data-ride="carousel">
		  <ol class="carousel-indicators">
		    <li data-target="#carouselExampleCaptions" data-slide-to="0" class="active"></li>
		    <li data-target="#carouselExampleCaptions" data-slide-to="1"></li>
		    <li data-target="#carouselExampleCaptions" data-slide-to="2"></li>
		  </ol>
		  <div class="carousel-inner">
		    <div class="carousel-item active">
		      <img src="..." class="d-block w-100" alt="...">
		      <div class="carousel-caption d-none d-md-block">
		        <h5>First slide label</h5>
		        <p>Nulla vitae elit libero, a pharetra augue mollis interdum.</p>
		      </div>
		    </div>
		    <div class="carousel-item">
		      <img src="..." class="d-block w-100" alt="...">
		      <div class="carousel-caption d-none d-md-block">
		        <h5>Second slide label</h5>
		        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit.</p>
		      </div>
		    </div>
		    <div class="carousel-item">
		      <img src="..." class="d-block w-100" alt="...">
		      <div class="carousel-caption d-none d-md-block">
		        <h5>Third slide label</h5>
		        <p>Praesent commodo cursus magna, vel scelerisque nisl consectetur.</p>
		      </div>
		    </div>
		  </div>
		  <a class="carousel-control-prev" href="#carouselExampleCaptions" role="button" data-slide="prev">
		    <span class="carousel-control-prev-icon" aria-hidden="true"></span>
		    <span class="sr-only">Previous</span>
		  </a>
		  <a class="carousel-control-next" href="#carouselExampleCaptions" role="button" data-slide="next">
		    <span class="carousel-control-next-icon" aria-hidden="true"></span>
		    <span class="sr-only">Next</span>
		  </a>
		</div>



	 淡入淡出：将.carousel-fade添加到轮播中，以淡入淡出过渡而不是幻灯片为幻灯片动画。

	 	<div id="carouselExampleFade" class="carousel slide carousel-fade" data-ride="carousel">
		  <div class="carousel-inner">
		    <div class="carousel-item active">
		      <img src="..." class="d-block w-100" alt="...">
		    </div>
		    <div class="carousel-item">
		      <img src="..." class="d-block w-100" alt="...">
		    </div>
		    <div class="carousel-item">
		      <img src="..." class="d-block w-100" alt="...">
		    </div>
		  </div>
		  <a class="carousel-control-prev" href="#carouselExampleFade" role="button" data-slide="prev">
		    <span class="carousel-control-prev-icon" aria-hidden="true"></span>
		    <span class="sr-only">Previous</span>
		  </a>
		  <a class="carousel-control-next" href="#carouselExampleFade" role="button" data-slide="next">
		    <span class="carousel-control-next-icon" aria-hidden="true"></span>
		    <span class="sr-only">Next</span>
		  </a>


21.大屏广告巨幕（Jumbotron）：一个轻巧，灵活的组件，可以选择扩展整个视口，展示关键的营销信息。

	基本用法：
		<div class="jumbotron">
		  <h1 class="display-4">Hello, world!</h1>
		  <p class="lead">This is a simple hero unit, a simple jumbotron-style component for calling extra attention to featured content or information.</p>
		  <hr class="my-4">
		  <p>It uses utility classes for typography and spacing to space content out within the larger container.</p>
		  <a class="btn btn-primary btn-lg" href="#" role="button">Learn more</a>
		</div>




	列表组I（List-group）：列表组是用于显示一系列内容的灵活而强大的组件。修改并扩展它们以支持其中的几乎所有内容。

		基本用法：

			<ul class="list-group">
			  <li class="list-group-item">Cras justo odio</li>
			  <li class="list-group-item">Dapibus ac facilisis in</li>
			  <li class="list-group-item">Morbi leo risus</li>
			  <li class="list-group-item">Porta ac consectetur ac</li>
			  <li class="list-group-item">Vestibulum at eros</li>
			</ul>


		激活当前框：将.active添加到.list-group-item以指示当前的活动选择，也可以加入disable禁用，aria-disabled="true"禁用所有JS触发事件

			<ul class="list-group">
			  <li class="list-group-item active">Cras justo odio</li>
			  <li class="list-group-item disabled" aria-disabled="true">Dapibus ac facilisis in</li>
			  <li class="list-group-item">Morbi leo risus</li>
			  <li class="list-group-item">Porta ac consectetur ac</li>
			  <li class="list-group-item">Vestibulum at eros</li>
			</ul>


		链接和按钮：通过添加.list-group-item-action，使用<a>或<button>s创建具有悬浮状态，禁用状态和活动状态的可操作列表组项目。

			<div class="list-group">
			  <a href="#" class="list-group-item list-group-item-action active">
			    Cras justo odio
			  </a>
			  <a href="#" class="list-group-item list-group-item-action">Dapibus ac facilisis in</a>
			  <a href="#" class="list-group-item list-group-item-action">Morbi leo risus</a>
			  <a href="#" class="list-group-item list-group-item-action">Porta ac consectetur ac</a>
			  <a href="#" class="list-group-item list-group-item-action disabled" tabindex="-1" aria-disabled="true">Vestibulum at eros</a>
			</div>


	改为单线框：
		<ul class="list-group list-group-flush">
		  <li class="list-group-item">Cras justo odio</li>
		  <li class="list-group-item">Dapibus ac facilisis in</li>
		  <li class="list-group-item">Morbi leo risus</li>
		  <li class="list-group-item">Porta ac consectetur ac</li>
		  <li class="list-group-item">Vestibulum at eros</li>
		</ul>


	横向排列：添加.list-group-horizo​​ntal可将所有断点的列表组项目的布局从垂直更改为水平。

		<ul class="list-group list-group-horizontal">
		  <li class="list-group-item">Cras justo odio</li>
		  <li class="list-group-item">Dapibus ac facilisis in</li>
		  <li class="list-group-item">Morbi leo risus</li>
		</ul>

	上下文类：使用上下文类为具有状态背景和颜色的列表项设置样式。


		改变颜色：list-group-item-primary/secondary/success/danger/warning/info/light/dark
		<li class="list-group-item list-group-item-primary">A simple primary list group item</li>


	上下文类也可以与.list-group-item-action一起使用。请注意，此处的悬停样式没有在前面的示例中提供。还支持.active状态。应用它以指示上下文列表组项上的活动选择。

		<a href="#" class="list-group-item list-group-item-action list-group-item-primary">A simple primary list group item</a>



	添加徽标：在某些实用程序的帮助下，将标志添加到任何列表组项以显示未读计数，活动等。

		<ul class="list-group">
		  <li class="list-group-item d-flex justify-content-between align-items-center">
		    Cras justo odio
		    <span class="badge badge-primary badge-pill">14</span>
		  </li>
		  <li class="list-group-item d-flex justify-content-between align-items-center">
		    Dapibus ac facilisis in
		    <span class="badge badge-primary badge-pill">2</span>
		  </li>
		  <li class="list-group-item d-flex justify-content-between align-items-center">
		    Morbi leo risus
		    <span class="badge badge-primary badge-pill">1</span>
		  </li>
		</ul>


22.媒体对象-图文混排（media-object）：Bootstrap媒体对象的文档和示例，用于构建高度重复的组件，例如博客评论，推文等。

	一个基本的、带头像、id、评论内容的的栅格：
		<div class="media">
		  <img src="..." class="mr-3" alt="...">
		  <div class="media-body">
		    <h5 class="mt-0">Media heading</h5>
		    Cras sit amet nibh libero, in gravida nulla. Nulla vel metus scelerisque ante sollicitudin. Cras purus odio, vestibulum in vulputate at, tempus viverra turpis. Fusce condimentum nunc ac nisi vulputate fringilla. Donec lacinia congue felis in faucibus.
		  </div>
		</div>


	头像相对位置：可以置顶、中部、底部：
		class="align-self-start mr-3"
		class="align-self-center mr-3"
		class="align-self-end mr-3"


	Order：添加权重，设置某些评论指定或按一定规则排列



23.弹出提示框：自定义的警报消息向访客推送通知。
	





24.提示冒泡（Tooltip）：添加自定义Bootstrap工具提示的文档和示例，例如给button添加一个鼠标悬停时的说明

	基本用法：可以给任何DOM元素绑定触发事件
		$(function () {
		  $('[data-toggle="tooltip"]').tooltip()
		})

		控制方向，向上下左右出现，data-placement="top/bottom/left/right"



25.pop提示（Popover）：用于将Bootstrap弹出窗口（如iOS中发现的）添加到网站上任何元素的文档和示例。
	点击触发以后，不会自动隐藏，需要再次点击才会隐藏
		
	基本用法：
		$(function () {
		  $('[data-toggle="popover"]').popover()
		})


		可以更改方向：data-placement="top/bottom/left/right"


	以上这两个基本就这两个地方用的多，其他地方使用的时候再去看文档


26.弹出模态框（modal）：一个类似于alert的组件	

	基本用法： data-target="#staticBackdrop" 绑定modal的id、 fade 丝滑动画、 modal-dialog-centered 弹框居中显示、
	data-backdrop="static" 弹出时点击空白区无法关闭 默认是可以关闭的、



		<!-- Button trigger modal -->
	<button type="button" class="btn btn-primary" data-toggle="modal" data-target="#staticBackdrop">
	  Launch static backdrop modal
	</button>

	<!-- Modal -->
	<div class="modal fade" id="staticBackdrop" data-backdrop="static" tabindex="-1" role="dialog" aria-labelledby="staticBackdropLabel" aria-hidden="true">
	  <div class="modal-dialog" role="document">
	    <div class="modal-content">
	      <div class="modal-header">
	        <h5 class="modal-title" id="staticBackdropLabel">Modal title</h5>
	        <button type="button" class="close" data-dismiss="modal" aria-label="Close">
	          <span aria-hidden="true">&times;</span>
	        </button>
	      </div>
	      <div class="modal-body">
	        ...
	      </div>
	      <div class="modal-footer">
	        <button type="button" class="btn btn-secondary" data-dismiss="modal">Close</button>
	        <button type="button" class="btn btn-primary">Understood</button>
	      </div>
	    </div>
	  </div>
	</div>





	当弹出长文章时：
		.modal-dialog-scrollable 添加进 .modal-dialog 中
		当模式对用户的视口或设备而言变得太长时，它们将独立于页面本身滚动。请尝试下面的演示，以了解我们的意思。
		比如用户协议


		<!-- Button trigger modal -->
		<button type="button" class="btn btn-primary" data-toggle="modal" data-target="#exampleModalScrollable">
		  Launch demo modal
		</button>

		<!-- Modal -->
		<div class="modal fade" id="exampleModalScrollable" tabindex="-1" role="dialog" aria-labelledby="exampleModalScrollableTitle" aria-hidden="true">
		  <div class="modal-dialog modal-dialog-scrollable" role="document">
		    <div class="modal-content">
		      <div class="modal-header">
		        <h5 class="modal-title" id="exampleModalScrollableTitle">Modal title</h5>
		        <button type="button" class="close" data-dismiss="modal" aria-label="Close">
		          <span aria-hidden="true">&times;</span>
		        </button>
		      </div>
		      <div class="modal-body">
		        ...
		      </div>
		      <div class="modal-footer">
		        <button type="button" class="btn btn-secondary" data-dismiss="modal">Close</button>
		        <button type="button" class="btn btn-primary">Save changes</button>
		      </div>
		    </div>
		  </div>
		</div>



	也可以和表单等功能混合使用


	内置方法：
		var mymodal = $('#id');
		$('#id').click(function(),{
			mymodal.model('show')
			})
		$('#id').click(function(),{
			mymodal.model('hide')
			})
		$('#id').click(function(),{
			mymodal.model('toggle')
			})
		


		mymodal.on('show.bs.modal',function(){

			})


27.导航-滑动门（nav）：顶部导航，

	基本用法：
		<ul class="nav">
		  <li class="nav-item">
		    <a class="nav-link active" href="#">Active</a>
		  </li>
		  <li class="nav-item">
		    <a class="nav-link" href="#">Link</a>
		  </li>
		  <li class="nav-item">
		    <a class="nav-link" href="#">Link</a>
		  </li>
		  <li class="nav-item">
		    <a class="nav-link disabled" href="#" tabindex="-1" aria-disabled="true">Disabled</a>
		  </li>
		</ul>

	切换的时候 可以在href中写组件id 也可以在data-target中写：

		<a href="#tab1" class="nav-link active">Active</a>
		<a href="#" class="nav-link active" data-target="#tab2">Active</a>



	可以设置左对齐、居中对齐、右对齐 默认是左对齐 .justify-content-left/center/end:


	也可以从上至下排列：flex-column,这个时候多与row结合使用






	改pill样式： 也可以改成 tabs 样式 看你自己喜好
		<ul class="nav nav-pills">
		  <li class="nav-item">
		    <a class="nav-link active" href="#">Active</a>
		  </li>
		  <li class="nav-item">
		    <a class="nav-link" href="#">Link</a>
		  </li>
		  <li class="nav-item">
		    <a class="nav-link" href="#">Link</a>
		  </li>
		  <li class="nav-item">
		    <a class="nav-link disabled" href="#" tabindex="-1" aria-disabled="true">Disabled</a>
		  </li>
		</ul>


	让导航栏强制填满整行，但是每个标题的宽度不一致：.nav-fill  如果要每个标题等宽，改为：  .nav-justified

		<ul class="nav nav-pills nav-fill">
		  <li class="nav-item">
		    <a class="nav-link active" href="#">Active</a>
		  </li>
		  <li class="nav-item">
		    <a class="nav-link" href="#">Much longer nav link</a>
		  </li>
		  <li class="nav-item">
		    <a class="nav-link" href="#">Link</a>
		  </li>
		  <li class="nav-item">
		    <a class="nav-link disabled" href="#" tabindex="-1" aria-disabled="true">Disabled</a>
		  </li>
		</ul>


	结合其他插件： 比如dorpdown，但是这个要在tabs或者pill式下才能用
		<ul class="nav nav-tabs">
		  <li class="nav-item">
		    <a class="nav-link active" href="#">Active</a>
		  </li>
		  <li class="nav-item dropdown">
		    <a class="nav-link dropdown-toggle" data-toggle="dropdown" href="#" role="button" aria-haspopup="true" aria-expanded="false">Dropdown</a>
		    <div class="dropdown-menu">
		      <a class="dropdown-item" href="#">Action</a>
		      <a class="dropdown-item" href="#">Another action</a>
		      <a class="dropdown-item" href="#">Something else here</a>
		      <div class="dropdown-divider"></div>
		      <a class="dropdown-item" href="#">Separated link</a>
		    </div>
		  </li>
		  <li class="nav-item">
		    <a class="nav-link" href="#">Link</a>
		  </li>
		  <li class="nav-item">
		    <a class="nav-link disabled" href="#" tabindex="-1" aria-disabled="true">Disabled</a>
		  </li>



28.导航栏Navbar：看上去比nav复杂一点，适合最顶部的一级导航
	

	基本用法：
		//最前部分是一个名称或者logo 其中也能嵌套dorpdown菜单 添加检索功能  添加fixed-top 可以让他始终显示在顶部

		<nav class="navbar navbar-expand-lg navbar-light bg-light">
  			<a class="navbar-brand" href="#">Navbar</a>
		  <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
		    <span class="navbar-toggler-icon"></span>
		  </button>

		  <div class="collapse navbar-collapse" id="navbarSupportedContent">
		    <ul class="navbar-nav mr-auto">
		      <li class="nav-item active">
		        <a class="nav-link" href="#">Home <span class="sr-only">(current)</span></a>
		      </li>
		      <li class="nav-item">
		        <a class="nav-link" href="#">Link</a>
		      </li>
		      <li class="nav-item dropdown">
		        <a class="nav-link dropdown-toggle" href="#" id="navbarDropdown" role="button" data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
		          Dropdown
		        </a> 
		        <div class="dropdown-menu" aria-labelledby="navbarDropdown">
		          <a class="dropdown-item" href="#">Action</a>
		          <a class="dropdown-item" href="#">Another action</a>
		          <div class="dropdown-divider"></div>
		          <a class="dropdown-item" href="#">Something else here</a>
		        </div>
		      </li>
		      <li class="nav-item">
		        <a class="nav-link disabled" href="#" tabindex="-1" aria-disabled="true">Disabled</a>
		      </li>
		    </ul>
		    <form class="form-inline my-2 my-lg-0">
		      <input class="form-control mr-sm-2" type="search" placeholder="Search" aria-label="Search">
		      <button class="btn btn-outline-success my-2 my-sm-0" type="submit">Search</button>
		    </form>
		  </div>
		</nav>


		添加form表单，做检索项：navbar中的直接子元素使用flex布局，默认情况下为justify-content：间隔。根据需要使用其他Flex实用程序来调整此行为。
			<nav class="navbar navbar-light bg-light">
			  <a class="navbar-brand">Navbar</a>
			  <form class="form-inline">
			    <input class="form-control mr-sm-2" type="search" placeholder="Search" aria-label="Search">
			    <button class="btn btn-outline-success my-2 my-sm-0" type="submit">Search</button>
			  </form>
			</nav>
		切换颜色：
			navbar-dark bg-dark
			navbar-dark bg-primary
			navbar-light style="background-color: #e3f2fd;



29.卡片Card：活且可扩展的内容容器。它包括页眉和页脚选项，各种内容，上下文背景颜色以及强大的显示选项。
			适合放在首页添加介绍或者描述、跳转至主要功能区



	基本用法：  card-title 主标题 、 card-submit 子标题、 card-text 描述、 a标签 点击跳转



		<div class="card" style="width: 18rem;">
		  <img src="..." class="card-img-top" alt="...">
		  <div class="card-body">
		    <h5 class="card-title">Card title</h5>
		    <p class="card-text">Some quick example text to build on the card title and make up the bulk of the card's content.</p>
		    <a href="#" class="btn btn-primary">Go somewhere</a>
		  </div>
		</div>



	Titles, text, and links：卡片支持多种内容，包括图像，文本，列表组，链接等。以下是支持的示例。


		<div class="card" style="width: 18rem;">
		  <div class="card-body">
		    <h5 class="card-title">Card title</h5>
		    <h6 class="card-subtitle mb-2 text-muted">Card subtitle</h6>
		    <p class="card-text">Some quick example text to build on the card title and make up the bulk of the card's content.</p>
		    <a href="#" class="card-link">Card link</a>
		    <a href="#" class="card-link">Another link</a>
		  </div>
		</div>


	图片：.card-img-top将图像放置在卡的顶部。使用.card-text，可以将文本添加到卡中  、卡片中可以加 .blockquote-footer添加备注

		<div class="card" style="width: 18rem;">
		  <img src="..." class="card-img-top" alt="...">
		  <div class="card-body">
		    <p class="card-text">Some quick example text to build on the card title and make up the bulk of the card's content.</p>
		  </div>
		</div>

	当然也可以放list-group： 注意添加list-group-flush 去边框
		<div class="card" style="width: 18rem;">
		  <div class="card-header">
		    Featured
		  </div>
		  <ul class="list-group list-group-flush">
		    <li class="list-group-item">Cras justo odio</li>
		    <li class="list-group-item">Dapibus ac facilisis in</li>
		    <li class="list-group-item">Vestibulum at eros</li>
		  </ul>
		</div>


	混合多种样式，可以集合图片、说明、菜单栏；或者在卡片中设置header footer等等
		<div class="card" style="width: 18rem;">
		  <img src="..." class="card-img-top" alt="...">
		  <div class="card-body">
		    <h5 class="card-title">Card title</h5>
		    <p class="card-text">Some quick example text to build on the card title and make up the bulk of the card's content.</p>
		  </div>
		  <ul class="list-group list-group-flush">
		    <li class="list-group-item">Cras justo odio</li>
		    <li class="list-group-item">Dapibus ac facilisis in</li>
		    <li class="list-group-item">Vestibulum at eros</li>
		  </ul>
		  <div class="card-body">
		    <a href="#" class="card-link">Card link</a>
		    <a href="#" class="card-link">Another link</a>
		  </div>
		</div>

	大小：用row包裹后 可用.col-   来设置大小


	添加案件 绑定函数  控制事件：text-center/right 控制对齐方式，默认左对齐
		<div class="card text-center" style="width: 18rem;">
		  <div class="card-body">
		    <h5 class="card-title">Special title treatment</h5>
		    <p class="card-text">With supporting text below as a natural lead-in to additional content.</p>
		    <a href="#" class="btn btn-primary">Go somewhere</a>
		  </div>
		</div>


	也可以结合nav 等等




	卡片组：使用卡组将卡呈现为具有相等宽度和高度列的单个附加元素。卡组使用显示：flex;实现他们的统一大小。

		<div class="card-group">
		  <div class="card">
		    <img src="..." class="card-img-top" alt="...">
		    <div class="card-body">
		      <h5 class="card-title">Card title</h5>
		      <p class="card-text">This is a wider card with supporting text below as a natural lead-in to additional content. This content is a little bit longer.</p>
		      <p class="card-text"><small class="text-muted">Last updated 3 mins ago</small></p>
		    </div>
		  </div>
		  <div class="card">
		    <img src="..." class="card-img-top" alt="...">
		    <div class="card-body">
		      <h5 class="card-title">Card title</h5>
		      <p class="card-text">This card has supporting text below as a natural lead-in to additional content.</p>
		      <p class="card-text"><small class="text-muted">Last updated 3 mins ago</small></p>
		    </div>
		  </div>
		  <div class="card">
		    <img src="..." class="card-img-top" alt="...">
		    <div class="card-body">
		      <h5 class="card-title">Card title</h5>
		      <p class="card-text">This is a wider card with supporting text below as a natural lead-in to additional content. This card has even longer content than the first to show that equal height action.</p>
		      <p class="card-text"><small class="text-muted">Last updated 3 mins ago</small></p>
		    </div>
		  </div>
		</div>


30.折叠面板Collapse：点击显示一行说明或者其他的东西，再点一下隐藏回去。

	基本用法： button的id要和需要控制的collapse的id一致  button处：data-toggle="collapse" 
	collapse处：id="collapseExample"
		<p>
		  <a class="btn btn-primary" data-toggle="collapse" href="#collapseExample" role="button" aria-expanded="false" aria-controls="collapseExample">
		    Link with href
		  </a>
		  <button class="btn btn-primary" type="button" data-toggle="collapse" data-target="#collapseExample" aria-expanded="false" aria-controls="collapseExample">
		    Button with data-target
		  </button>
		</p>
		<div class="collapse" id="collapseExample">
		  <div class="card card-body">
		    Anim pariatur cliche reprehenderit, enim eiusmod high life accusamus terry richardson ad squid. Nihil anim keffiyeh helvetica, craft beer labore wes anderson cred nesciunt sapiente ea proident.
		  </div>
		</div>
			

	结合控制语句：<button>或<a>可以通过在href属性或data-target属性中使用JQuery选择器对其进行引用来显示和隐藏多个元素。如果多个<button>或<a>各自使用href或data-target属性引用该元素，则可以显示和隐藏该元素



		<p>
  <a class="btn btn-primary" data-toggle="collapse" href="#multiCollapseExample1" role="button" aria-expanded="false" aria-controls="multiCollapseExample1">Toggle first element</a>
  <button class="btn btn-primary" type="button" data-toggle="collapse" data-target="#multiCollapseExample2" aria-expanded="false" aria-controls="multiCollapseExample2">Toggle second element</button>
  <button class="btn btn-primary" type="button" data-toggle="collapse" data-target=".multi-collapse" aria-expanded="false" aria-controls="multiCollapseExample1 multiCollapseExample2">Toggle both elements</button>
	</p>
	<div class="row">
	  <div class="col">
	    <div class="collapse multi-collapse" id="multiCollapseExample1">
	      <div class="card card-body">
	        Anim pariatur cliche reprehenderit, enim eiusmod high life accusamus terry richardson ad squid. Nihil anim keffiyeh helvetica, craft beer labore wes anderson cred nesciunt sapiente ea proident.
	      </div>
	    </div>
	  </div>
	  <div class="col">
	    <div class="collapse multi-collapse" id="multiCollapseExample2">
	      <div class="card card-body">
	        Anim pariatur cliche reprehenderit, enim eiusmod high life accusamus terry richardson ad squid. Nihil anim keffiyeh helvetica, craft beer labore wes anderson cred nesciunt sapiente ea proident.
	      </div>
	    </div>
	  </div>
	</div>






	结合card 做出类似手风琴样式：card这边只用一个card-header button按钮绑定 需要显示的html   card-body就是绑定需要显示的部分 

	如果只需要显示一个，点其他的，之前的回自动收缩，需要添加 .data-children属性，与其关联的也要用item包起来

	<div class="accordion" id="accordionExample">
	  <div class="card">
	    <div class="card-header" id="headingOne">
	      <h2 class="mb-0">
	        <button class="btn btn-link" type="button" data-toggle="collapse" data-target="#collapseOne" aria-expanded="true" aria-controls="collapseOne">
	          Collapsible Group Item #1
	        </button>
	      </h2>
	    </div>

	    <div id="collapseOne" class="collapse show" aria-labelledby="headingOne" data-parent="#accordionExample">
	      <div class="card-body">
	        Anim pariatur cliche reprehenderit, enim eiusmod high life accusamus terry richardson ad squid. 3 wolf moon officia aute, non cupidatat skateboard dolor brunch. Food truck quinoa nesciunt laborum eiusmod. Brunch 3 wolf moon tempor, sunt aliqua put a bird on it squid single-origin coffee nulla assumenda shoreditch et. Nihil anim keffiyeh helvetica, craft beer labore wes anderson cred nesciunt sapiente ea proident. Ad vegan excepteur butcher vice lomo. Leggings occaecat craft beer farm-to-table, raw denim aesthetic synth nesciunt you probably haven't heard of them accusamus labore sustainable VHS.
	      </div>
	    </div>
	  </div>
	  <div class="card">
	    <div class="card-header" id="headingTwo">
	      <h2 class="mb-0">
	        <button class="btn btn-link collapsed" type="button" data-toggle="collapse" data-target="#collapseTwo" aria-expanded="false" aria-controls="collapseTwo">
	          Collapsible Group Item #2
	        </button>
	      </h2>
	    </div>
	    <div id="collapseTwo" class="collapse" aria-labelledby="headingTwo" data-parent="#accordionExample">
	      <div class="card-body">
	        Anim pariatur cliche reprehenderit, enim eiusmod high life accusamus terry richardson ad squid. 3 wolf moon officia aute, non cupidatat skateboard dolor brunch. Food truck quinoa nesciunt laborum eiusmod. Brunch 3 wolf moon tempor, sunt aliqua put a bird on it squid single-origin coffee nulla assumenda shoreditch et. Nihil anim keffiyeh helvetica, craft beer labore wes anderson cred nesciunt sapiente ea proident. Ad vegan excepteur butcher vice lomo. Leggings occaecat craft beer farm-to-table, raw denim aesthetic synth nesciunt you probably haven't heard of them accusamus labore sustainable VHS.
	      </div>
	    </div>
	  </div>
	  <div class="card">
	    <div class="card-header" id="headingThree">
	      <h2 class="mb-0">
	        <button class="btn btn-link collapsed" type="button" data-toggle="collapse" data-target="#collapseThree" aria-expanded="false" aria-controls="collapseThree">
	          Collapsible Group Item #3
	        </button>
	      </h2>
	    </div>
	    <div id="collapseThree" class="collapse" aria-labelledby="headingThree" data-parent="#accordionExample">
	      <div class="card-body">
	        Anim pariatur cliche reprehenderit, enim eiusmod high life accusamus terry richardson ad squid. 3 wolf moon officia aute, non cupidatat skateboard dolor brunch. Food truck quinoa nesciunt laborum eiusmod. Brunch 3 wolf moon tempor, sunt aliqua put a bird on it squid single-origin coffee nulla assumenda shoreditch et. Nihil anim keffiyeh helvetica, craft beer labore wes anderson cred nesciunt sapiente ea proident. Ad vegan excepteur butcher vice lomo. Leggings occaecat craft beer farm-to-table, raw denim aesthetic synth nesciunt you probably haven't heard of them accusamus labore sustainable VHS.
	      </div>
	    </div>
	  </div>
	</div>


	JS控件：.collapse('toggle')
			.collapse('show')
			.collapse('hide')
			.collapse('dispose')


31.分页-进度条pagenation-progress：

	分页：基本用法 前进、1、2、3、后退
		<nav aria-label="Page navigation example">
		  <ul class="pagination">
		    <li class="page-item"><a class="page-link" href="#">Previous</a></li>
		    <li class="page-item"><a class="page-link" href="#">1</a></li>
		    <li class="page-item"><a class="page-link" href="#">2</a></li>
		    <li class="page-item"><a class="page-link" href="#">3</a></li>
		    <li class="page-item"><a class="page-link" href="#">Next</a></li>
		  </ul>
		</nav>

		如果想用其他前进或者后退图标代替文本，纪要确保使用aria属性提供适当的屏幕阅读器支持，这里&laquo &raquo 图片是ios上能使用的前进和后退图标

			<nav aria-label="Page navigation example">
			  <ul class="pagination">
			    <li class="page-item">
			      <a class="page-link" href="#" aria-label="Previous">
			        <span aria-hidden="true">&laquo;</span>
			      </a>
			    </li>
			    <li class="page-item"><a class="page-link" href="#">1</a></li>
			    <li class="page-item"><a class="page-link" href="#">2</a></li>
			    <li class="page-item"><a class="page-link" href="#">3</a></li>
			    <li class="page-item">
			      <a class="page-link" href="#" aria-label="Next">
			        <span aria-hidden="true">&raquo;</span>
			      </a>
			    </li>
			  </ul>
			</nav>


		当前页面高亮： .disabled和 .active
			<nav aria-label="...">
			  <ul class="pagination">
			    <li class="page-item disabled">
			      <a class="page-link" href="#" tabindex="-1" aria-disabled="true">Previous</a>
			    </li>
			    <li class="page-item"><a class="page-link" href="#">1</a></li>
			    <li class="page-item active" aria-current="page">
			      <a class="page-link" href="#">2 <span class="sr-only">(current)</span></a>
			    </li>
			    <li class="page-item"><a class="page-link" href="#">3</a></li>
			    <li class="page-item">
			      <a class="page-link" href="#">Next</a>
			    </li>
			  </ul>
			</nav>

		位置： .justify-content-center/end 控制位置 默认左对齐

	滚动条：

		基本用法：aria-valuenow="0" aria-valuemin="0" 来控制蓝条的进程

			<div class="progress">
			  <div class="progress-bar" role="progressbar" aria-valuenow="0" aria-valuemin="0" aria-valuemax="100"></div>
			</div>

		文本显示当前进度：.progress-bar

			<div class="progress">
			  <div class="progress-bar" role="progressbar" style="width: 25%;" aria-valuenow="25" aria-valuemin="0" aria-valuemax="100">25%</div>
			</div>


		颜色：可以分段控制，将颜色.bg-success 设置在不同的.progress-bar 中，可以实现分段显示颜色

			<div class="progress">
			  <div class="progress-bar" role="progressbar" style="width: 15%" aria-valuenow="15" aria-valuemin="0" aria-valuemax="100"></div>
			  <div class="progress-bar bg-success" role="progressbar" style="width: 30%" aria-valuenow="30" aria-valuemin="0" aria-valuemax="100"></div>
			  <div class="progress-bar bg-info" role="progressbar" style="width: 20%" aria-valuenow="20" aria-valuemin="0" aria-valuemax="100"></div>
			</div>


		条状：没什么好说的 好看点 用.progress-bar-striped开启 用.bg-info 调整具体颜色


			<div class="progress">
			  <div class="progress-bar progress-bar-striped bg-info" role="progressbar" style="width: 50%" aria-valuenow="50" aria-valuemin="0" aria-valuemax="100"></div>
			</div>

			条纹渐变也可以设置为动画。将.progress-bar-animated添加到.progress-bar以通过CSS3动画从右到左对条纹进行动画处理。

			<div class="progress">
			  <div class="progress-bar progress-bar-striped progress-bar-animated" role="progressbar" aria-valuenow="75" aria-valuemin="0" aria-valuemax="100" style="width: 75%"></div>
			</div>


32.滚动监听scrollspy：滚动导航栏下方的区域，然后查看活动的班级更改。下拉项也会突出显示。
					比如某些文档中你向下滑，左边的导航栏也会跟着一起走，原理也是设置了锚点，自动触发


	基本用法：必须要在 nav导航组或者group-list中使用 设置position：relative 锚点<a>必须指向上一个id 然后把active移到下一个关联的项目上 

	可以设置data-offset="100" 来设置滚动到哪里触发 默认是10


		<nav id="navbar-example2" class="navbar navbar-light bg-light">
		  <a class="navbar-brand" href="#">Navbar</a>
		  <ul class="nav nav-pills">
		    <li class="nav-item">
		      <a class="nav-link" href="#fat">@fat</a>
		    </li>
		    <li class="nav-item">
		      <a class="nav-link" href="#mdo">@mdo</a>
		    </li>
		    <li class="nav-item dropdown">
		      <a class="nav-link dropdown-toggle" data-toggle="dropdown" href="#" role="button" aria-haspopup="true" aria-expanded="false">Dropdown</a>
		      <div class="dropdown-menu">
		        <a class="dropdown-item" href="#one">one</a>
		        <a class="dropdown-item" href="#two">two</a>
		        <div role="separator" class="dropdown-divider"></div>
		        <a class="dropdown-item" href="#three">three</a>
		      </div>
		    </li>
		  </ul>
		</nav>

		<div data-spy="scroll" data-target="#navbar-example2" data-offset="0">
		  <h4 id="fat">@fat</h4>
		  <p>...</p>
		  <h4 id="mdo">@mdo</h4>
		  <p>...</p>
		  <h4 id="one">one</h4>
		  <p>...</p>
		  <h4 id="two">two</h4>
		  <p>...</p>
		  <h4 id="three">three</h4>
		  <p>...</p>
		</div>
		

		也适用于nav嵌套或者list-group中：
			<nav id="navbar-example3" class="navbar navbar-light bg-light">
			  <a class="navbar-brand" href="#">Navbar</a>
			  <nav class="nav nav-pills flex-column">
			    <a class="nav-link" href="#item-1">Item 1</a>
			    <nav class="nav nav-pills flex-column">
			      <a class="nav-link ml-3 my-1" href="#item-1-1">Item 1-1</a>
			      <a class="nav-link ml-3 my-1" href="#item-1-2">Item 1-2</a>
			    </nav>
			    <a class="nav-link" href="#item-2">Item 2</a>
			    <a class="nav-link" href="#item-3">Item 3</a>
			    <nav class="nav nav-pills flex-column">
			      <a class="nav-link ml-3 my-1" href="#item-3-1">Item 3-1</a>
			      <a class="nav-link ml-3 my-1" href="#item-3-2">Item 3-2</a>
			    </nav>
			  </nav>
			</nav>

			<div data-spy="scroll" data-target="#navbar-example3" data-offset="0">
			  <h4 id="item-1">Item 1</h4>
			  <p>...</p>
			  <h5 id="item-1-1">Item 1-1</h5>
			  <p>...</p>
			  <h5 id="item-1-2">Item 1-2</h5>
			  <p>...</p>
			  <h4 id="item-2">Item 2</h4>
			  <p>...</p>
			  <h4 id="item-3">Item 3</h4>
			  <p>...</p>
			  <h5 id="item-3-1">Item 3-1</h5>
			  <p>...</p>
			  <h5 id="item-3-2">Item 3-2</h5>
			  <p>...</p>
			</div>




		list-gruop：
			<div id="list-example" class="list-group">
			  <a class="list-group-item list-group-item-action" href="#list-item-1">Item 1</a>
			  <a class="list-group-item list-group-item-action" href="#list-item-2">Item 2</a>
			  <a class="list-group-item list-group-item-action" href="#list-item-3">Item 3</a>
			  <a class="list-group-item list-group-item-action" href="#list-item-4">Item 4</a>
			</div>


			<div data-spy="scroll" data-target="#list-example" data-offset="0" class="scrollspy-example">
			  <h4 id="list-item-1">Item 1</h4>
			  <p>...</p>
			  <h4 id="list-item-2">Item 2</h4>
			  <p>...</p>
			  <h4 id="list-item-3">Item 3</h4>
			  <p>...</p>
			  <h4 id="list-item-4">Item 4</h4>
			  <p>...</p>
			</div>


		js事件：

			$('[data-spy="scroll"]').on('activate.bs.scrollspy', function () {
			  // do something...
			})


32.旋转特效Spinners：就等待的时候转圈圈，一般转的快一点可以让人觉得速度很快

	基本用法：
		<div class="spinner-border" role="status">
		  <span class="sr-only">Loading...</span>
		</div>


	改变颜色：边框微调器使用currentColor作为其边框颜色 所以用.text-primary就能改变颜色了

		<div class="spinner-border text-primary" role="status">
		  <span class="sr-only">Loading...</span>
		</div>

	其他样式：闪点 这样看上去酷一点

		<div class="spinner-grow" role="status">
		  <span class="sr-only">Loading...</span>
		</div>

		颜色一样用 .text-primary改变


	位置：可以和别的div包在一起 用class="d-flex align-items-center"  控制
			<div class="d-flex align-items-center">
			  <strong>Loading...</strong>
			  <div class="spinner-border ml-auto" role="status" aria-hidden="true"></div>
			</div>

		可以用float控制：
			<div class="clearfix">
			  <div class="spinner-border float-right" role="status">
			    <span class="sr-only">Loading...</span>
			  </div>
			</div>

		可以text-center控制：
			<div class="text-center">
			  <div class="spinner-border" role="status">
			    <span class="sr-only">Loading...</span>
			  </div>
			</div>



	和button放在一起使用：
		<button class="btn btn-primary" type="button" disabled>
		  <span class="spinner-border spinner-border-sm" role="status" aria-hidden="true"></span>
		  <span class="sr-only">Loading...</span>
		</button>
		<button class="btn btn-primary" type="button" disabled>
		  <span class="spinner-border spinner-border-sm" role="status" aria-hidden="true"></span>
		  Loading...
		</button>


34.图标
	bs4没有自己的字体图标，可以载入第三方字体库
		比如Font Awesome，script标签加载之后 用 <i></i> 中间加对应的字符就能使用