# web.xml新增配置：
<filter>\
	  <filter-name>HttpMethodFilter</filter-name>\
	  <filter-class>org.springframework.web.filter.HttpPutFormContentFilter</filter-class>\
  </filter>\
  <filter-mapping>\
	  <filter-name>HttpMethodFilter</filter-name>\
	  <url-pattern>/*</url-pattern>\
  </filter-mapping>\
  <filter>\
	  <filter-name>HiddenHttpMethodFilter</filter-name>\
	  <filter-class>org.springframework.web.filter.HiddenHttpMethodFilter</filter-class>\
  </filter>\
  <filter-mapping>\
	  <filter-name>HiddenHttpMethodFilter</filter-name>\
	  <servlet-name>dispatcher</servlet-name>\
	  <url-pattern>/*</url-pattern>\
  </filter-mapping>\
