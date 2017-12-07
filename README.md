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
