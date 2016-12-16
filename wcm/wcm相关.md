# 三、学习wcm相关

## 学习周期：

* 三天

* 了解 视图、元数据、栏目、模板等概念，并完成一个简单的产品列表页和详情页

## 完成条件：

* 本地成功安装wcm，并能正常使用

* 能正常发布产品列表页和详情页


#### 本地成功安装wcm，并能正常使用
*  服务启动
  ![Markdown](http://i1.piimg.com/580567/8dabc420b5a57647.png)
* tomcate
  ![Markdown](http://i1.piimg.com/580567/bc34bbbfe83c36b6.png)
*  成功登陆
  ![Markdown](http://i1.piimg.com/580567/ca843aa705b326b8.png)
##基本概念

* #### 站点
  WCM系统里主要的对象，负责组织和管理栏目。一个站点相当于一个Internet网站，可以按照网站的结构来设计站点及栏目。 
  
* #### 库
  相同类型站点的集合，分为文字库、图片库、视频库和资源库。
  
* #### 栏目
  站点的下一级管理单元，用来组织和管理文档。栏目的存在必须依附于站点，没有站点便不能建立栏目。 

* #### 文档
  WCM系统的基本单元，也是系统的核心数据内容。系统中的每一篇文档都必须建立在某个栏目下，由具备特定权限的用户来操作和管理。 

* #### 模板
  带有TRS置标的HTML文件，用来控制发布页面的显示。系统中的站点、栏目、文档都可以分别配备不同类型模板。 
  
* #### 发布
  将系统中的数据结合模板置标生成HTML页面的过程。设置了完整发布属性的站点、栏目及文档都可以执行发布操作。
  
* #### 预览
  在对象发布之前，通过预览功能可以提前查看站点、栏目和文档发布后的效果。

* #### 元数据
  描述一个对象的属性的集合，类似数据库中表的概念。
  
* #### 视图
  建立在元数据之上、由元数据生成的属性的集合，类似数据库中视图的概念。 

* #### 分类法
  用于标识数据的一颗分类树，如按体裁分类，按机构分类。 
###  建立站点
1. 进入文字库的“站点”标签页，进入站点列表页面，在操作面板中的系统操作任务面板中，点击 『创建一个新站点』，弹出创建站点对话框。 

![Paste_Image.png](http://upload-images.jianshu.io/upload_images/3946479-49170cd7489d0d74.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
2. 在对话框中填写必填信息，站点的唯一标识：实习演示，显示名称：实习演示，存放位置：sxys，站点 HT：HTTP://127.0.0.1:8888/pub/sxys。点击确定，

![Paste_Image.png](http://upload-images.jianshu.io/upload_images/3946479-8140730676de8cbf.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
 实习演示“”创建到文 字库内。需要注意，站点的唯一标识和存放位置不能和系统中已有的站点重名。 
###  建立栏目
1. 栏目依附于站点而存在，因此只能在站点中创建。双击“实习演示”的图标进入站点，或在导航 树中点击“实习演示”直接进入站点。打开标签栏中的“栏目”，进入栏目列表页面，当然，现在的 “实习演示”下没有任何栏目。 
2. 在子栏目操作任务面板中点击『新建一个栏目』，弹出新建栏目对话框
创建一个普通栏目，在对话框中填写必填内容。唯一标识：简单商品列表，显示名称：简单商品列表，存 放位置：demo。各项必填内容编辑完成后点击确定建立栏目。与站点类似，栏目的唯一标识和存放位 置在同一个站点下不能重名。 


![Paste_Image.png](http://upload-images.jianshu.io/upload_images/3946479-6502097b98bd9864.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
### 建立文档
1. 文档只能创建在普通栏目中。在栏目列表中双击“简单商品列表”栏目图标，或者通过导航树点击 “实习演示”下的“简单商品列表”进入栏目。 
2. 打开栏目下的“文档”标签页，进入栏目的文档列表页面，当然，现在“国内新闻”栏目下没有 任何文档。在栏目文档操作任务面板中点击『创建一篇新文档』，打开文档编辑页面。

![Paste_Image.png](http://upload-images.jianshu.io/upload_images/3946479-befbc3a04f2fb469.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

3. 选择文档类型为HTML编辑一篇HTML类型的文档。编辑文档内容，其中文档标题和正文是必须 填写的，利用工具栏中丰富的工具编辑 HTML 页面，同时可在编辑器右侧的属性栏中设置文档的各项 属性。编辑完成后点击底部的“保存并关闭”按钮，保存文档且退出编辑器。这时文档列表中出现了 创建的这篇文档。 
 
### 学习置标
#### 详见---《TRSWCM7.0 发布置标手册》。
### 建立模板
*   模板是带有TRS置标的 HTML文件，用来控制发布页面的内容显示和结构布局。站点、栏目和文 档都属于可以发布的对象，要想发布，就必须先创建一些模板并配置到站点、栏目、文档这些对象 上。 
*  站点和栏目中都可以创建模板，站点下创建的模板可被站点内的所有栏目和文档使用，在栏目下 创建的模板只能被当前栏目、子栏目和文档使用。 
进入站点“新闻站点”，打开“模板”标签进入站点的模板列表页面。在“站点模板操作任务” 面板中点击『新建一个模板』，打开模板编辑器。 

![Paste_Image.png](http://upload-images.jianshu.io/upload_images/3946479-ae15a473b65d168f.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
*  模板分为概览、细览、嵌套和表单打印四种类型。概览模板用于设置站点/栏目的首页，而细览模 板用于设置文档的页面。在编辑模板时，除了必要的模板名称和内容，还需要选择合适的模板类型。 模板文件的扩展名默认为 html，概览模板的发布文件名默认为 index。 
4. 建立一个概览模板，用于展示栏目中的文档列表。编辑模板名称为“栏目概览”，选择栏目类型 为概览

![Paste_Image.png](http://upload-images.jianshu.io/upload_images/3946479-661216828b396301.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
5. 点击“添加 TRS 置标向导”，在添加置标向导的第一步选择文档类置标的“文档列表”，点击下 一步。 
6. 进入下一步编辑置标属性，在表格中设置各个置标参数，参数设置的详细说明参考《TRSWCM7.0 发布置标手册》。此处设置为默认值即可，点击下一步。 
7. 进入左侧的“预览”标签，文本框中是系统根据设置的参数值生成的一段 TRS 置标，点击插入到 光标处，这段置标代码将被复制到模板编辑器的正文中。点击“保存”完成模板的创建。 
8. 选中这个模板，右侧的“模板操作任务”面板中是对这个模板的可执行操作，从属性面板可查看 模板的详细信息
9. 按照同样的步骤，可根据实际的需求设计出多种不同的模板，以适用于各类站点、栏目和文档。 模板创建后，可以分别给以上这些对象设置模板。 
给站点设置模板：在“站点操作任务”面板中点击『修改这个站点』，弹出修改站点的对话框，设 置站点的默认首页模板，点击设置模板图标 ，弹出选择模板对话框。对话框中列出了站点中所有的 概览模板，从中选择适合站点首页的模板，点击确定并保存站点的修改，这样站点首页模板就设置成 功了。 
10. 设置栏目与文档模板的方法类似。进入栏目后，在“栏目操作任务”面板中点击『修改这个栏 目』，弹出修改栏目对话框，设置栏目的首页模板和细览模板。首页模板即当前栏目的概览模板，细览 模板则是栏目中所有文档共用的模板。点击设置模板的图标 ，分别为栏目首页和栏目的文档选择合 适的模板，点击确定并保存栏目的修改，这样栏目和文档的模板设置成功。 
## 附录

#### 简单概览模板
```html
	<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
	<HTML xmlns="http://www.w3.org/1999/xhtml">
	<HEAD>
	<META http-equiv="Content-Type" content="text/html; charset=utf-8" />
	<TITLE>666</TITLE>
	<LINK href="style.css" rel="stylesheet" type="text/css" OLDSRC="style.css" OLDID="176" RELATED="1">
	</HEAD>

	<BODY>
	<TABLE width="100%" border="0" cellpadding="0" cellspacing="0" class="dh-bg">
	<TR>
		<TD width="84%" class="dh-font01">
			<TRS_CHANNELS ID="SITE" NUM="7">
			<TRS_CHANNEL EXTRA="CLASS='dh-font01'" autolink="true">
			</TRS_CHANNEL>
			│*|
			</TRS_CHANNELS>
		</TD>
		<TD width="16%" align="center" valign="middle" style="font-size:9pt;">
		</TD>
	</TR>
	</TABLE>
	<table width="100%" cellspacing="0" cellpadding="0" border="1">
	<th width="100%"  style="height:60px"  ><font face="arial" size="5" color="blue">文章列表</font> （产品数量：<TRS_CHANNEL ID="owner" FIELD="_DataCount"/>）<th>
 
	</table>
       <table width="100%" cellspacing="0" cellpadding="0" border="0">

    	<tr>
		<td width="84%" class="pic-box01">
                <font face="arial" size="3" color="blue">题目</font>
		</td>
                <td width="16%" class="pic-box01">
                <font face="arial" size="3" color="blue">入库时间</font>
		</td>

    	</tr>

      <TRS_DOCUMENTS id="简单商品列表"  channeltype="0"  num="50" startpos="0" automore="FALSE" moretarget="_blank" moretext="更多..."      enablelimit="FALSE">
	   <tr>
		<td width="84%" class="pic-box01">
                        <TRS_APPENDIX INDEX="0" MODE="PIC" width="140" HEIGHT="97"/>
                        <div  style="position:relative;top:-20px;left:20% ">
			<TRS_DOCUMENT FIELD="DOCTITLE" extra="class='top-font'" autocolor="false"></TRS_DOCUMENT>
                         </div>
                        <BR /><TRS_DOCUMENT FIELD="DOCABSTRACT"/><BR />
		</td>
                <td width="16%" class="pic-box03">
                        <font face="arial" size="2" color="red"><TRS_DOCUMENT  FIELD="CRTIME"/></font>
		</td>
                   
	   </tr>
      </TRS_DOCUMENTS>

        </table>

       </BODY>
        </HTML>
  ```
  ### 简单细览模板
```html
  

 	 <!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
		<HTML xmlns="http://www.w3.org/1999/xhtml">
		<HEAD>
			<META http-equiv="Content-Type" content="text/html; charset=utf-8" />
		<LINK href="style.css" rel="stylesheet" type="text/css" OLDSRC="style.css" OLDID="176" RELATED="1">


		</HEAD>

		<BODY>

	
		<TABLE width="950px" style="margin:0 10%;background-color:#ffffff" align="center">
		<TR>
		<TD>
			<TRS_TEMPLATE TEMPNAME="头部嵌套模版">
			加入嵌套模版
			</TRS_TEMPLATE>


			<TABLE width="100%" height="4" border="0" cellpadding="0" cellspacing="0" bgcolor="#50a8ac">
				<TR>
					<TD></TD>
				</TR>
			</TABLE>

			<BR>
			<BR>

			<TABLE width="100%" style="padding:0px;cellspacing:0px" align="center">
				<TR>
					<TD>

				
						<TABLE>
							<TR align="left" style="font-size:14px">
								<TD WIDTH="3%" valign="top"><IMG src="../site1/icon.gif" width="12" height="12" /></TD>
								<TD WIDTH="97%">
									当前位置：
									<TRS_COLUMN id=_TRSCURPAGE>
									当前位置
									</TRS_COLUMN>
								</TD>
							</TR>
						</TABLE>
			

					</TD>
				</TR>
				<TR>
					<TD width="100%" align="center">

			
						<TABLE width="90%">
							<TR class="h1" align="center" vlign="top">
								<TD align="center">
									<TRS_DOCUMENT FIELD=DOCTITLE autocolor="false">
									标题
									</TRS_DOCUMENT>
									<BR>
								</TD>
							</TR>
							<TR align="center">
								<TD align="center" style="padding:10px">
									<SPAN class="riqi">
									<TRS_COLUMN id=DOCPUBTIME>
									发布时间
									</TRS_COLUMN>
									</SPAN>
								</TD>
							</TR>
						</TABLE>
					

					</TD>
				</TR>
				<TR>
					<TD width="100%" align="center">

				
						<TABLE width="90%">
							<TR>
								<TD>

								
									<HR color=#009efd SIZE=1>
								</TD>
							</TR>
							<TR class="h2">
								<TD style="text-align:left">
                                                               <div  >
                                                                  <TRS_APPENDIX INDEX="0" MODE="PIC" width="300" HEIGHT="200"/>
                                                                </div>
                                                                <div  style="position:absolute;left:45%;top:58%  ">
			                        <span><strong><a style="color:black;font-size:10pt">产品名称  ：</a></strong>
						</span><font face="arial" size="5" color="red"> <TRS_DOCUMENT FIELD="DOCTITLE" extra="class='top-font'" autocolor="false"></TRS_DOCUMENT></font></br>
                                                <span><strong><a style="color:black;font-size:10pt">价格  ：</a></strong>
						</span><font face="arial" size="5" color="red">3999.9￥</font></br>
                                                <span><strong><a style="color:black;font-size:10pt">数量  ：</a></strong>
						</span><font face="arial" size="5" color="red">100000</font></br>
                                                  <button class="input01">购买</button>
                                                                    </div>
								</TD>
							</TR>
						</TABLE>


					</TD>
					
				</TR>
				<TR>
				<td height='32' align='center' valign='bottom'>
						<span><strong><a href="#" onclick="window.close();" style="color:black;font-size:10pt">[关闭窗口]</a></strong>
						<span>
						<p/>
					</td>
				</TR>
			</TABLE>
		

			<TRS_TEMPLATE tempname="底部模版">
			底部模版
			</TRS_TEMPLATE>
		</TD>
		</TR>
		</TABLE>
	
		</BODY>
		</HTML>
```