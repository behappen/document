# document

打包的时候使用了参数\
-c -F,是一闪而过，用-w -F的话cmd框都没出来，我的py脚本不是带界面的。\
-D, --onedir  创建一个目录，包含exe文件和依赖文件，这是默认选项。\
-F, --onefile 创建一个exe文件，所有依赖文件都打包进了这个exe文件，这个exe会比较大，但是我觉得方便使用。\
-c, --console, --nowindowed 控制台，无界面，默认选项。\
-w, --windowed, --noconsole 窗口无控制台。

1.id定位：find_element_by_id(self, id_)\
2.name定位：find_element_by_name(self, name)\
3.class定位：find_element_by_class_name(self, name)\
4.tag定位：find_element_by_tag_name(self, name)\
5.link定位：find_element_by_link_text(self, link_text)\
6.partial_link定位find_element_by_partial_link_text(self, link_text)\
7.xpath定位：find_element_by_xpath(self, xpath)\
8.css定位：find_element_by_css_selector(self, css_selector）\
9.id复数定位find_elements_by_id(self, id_)\
10.name复数定位find_elements_by_name(self, name)\
11.class复数定位find_elements_by_class_name(self, name)\
12.tag复数定位find_elements_by_tag_name(self, name)\
13.link复数定位find_elements_by_link_text(self, text)\
14.partial_link复数定位find_elements_by_partial_link_text(self, link_text)\
15.xpath复数定位find_elements_by_xpath(self, xpath)\
16.css复数定位find_elements_by_css_selector(self, css_selector\


# macOS 10.13.1 python 环境搭建
## 安装python和添加环境变量
mac本身自带python2.7\
自己安装最新版本python3.6.3\
打开终端输入 - open ~/.bash_profile\
\
alias python="/Library/Frameworks/Python.framework/Versions/3.6/bin/python3.6"（python3.6.3安装路径）\
如何查看python安装路径：\
终端输入python或者python3（当输入python版本为2.7的时候）
import sys\
print(sys.path)\
\
终端执行：source ~/.bash_profile 或者重启终端（重新加载配置文件）\
# 安装pip
因为python3.5版本之后都自带pip，直接安装pip就行，在用户根目录下，执行sudo easy_install pip
# 安装selenium
在用户根目录下，执行 sudo pip install –U selenium\
如果执行此操作报错\
报错信息如下：\
OSError: [Errno 1] Operation not permitted: '/System/Library/Frameworks/Python.framework/Versions/2.7/
原因：\
新系统有个叫sip的机制。 你暂时不能直接在终端进行 csrutil disable 会出现错误提示，引导你去mac osx的恢复模式进行操作。 \
由于El Capitan引入了SIP机制(System Integrity Protection)，默认下系统启用SIP系统完整性保护机制，无论是对于硬盘还是运行时的进程限制对系统目录的写操作。\
重新执行：\
python -m pip install selenium
# 安装Pycharm
直接下载安装，破解度娘一下
# 安装浏览器的driver
下载地址：http://npm.taobao.org/mirrors/chromedriver/ \
解压将chromedriver拖拽到 /usr/local/bin/目录下\
说明：因为/usr/bin目录下没有写的权限，所以chromedriver文件不能拖到这个目录下边，所以把chromedriver文件放在/usr/local/bin目录下，因为环境变量的PTAH中是PATH=/usr/local/bin:/usr/bin:/bin:/usr/sbin:/sbin（path不需要进行修改操作），这样会优先调用/usr/local/bin目录下的程序
# selenium第一个脚本
#!/user/bin/env python
#-*-coding:utf-8-*-

from selenium import webdriver

driver = webdriver.Chrome()\
driver.get("http://www.baidu.com")\
driver.find_element_by_id('kw').send_keys('selenium')\
driver.find_element_by_id('su').click()\
#driver.quit()
