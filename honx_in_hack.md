红杏
	chrome-extension
		ID:npacipdgogmamniefcahnbddckbejjoc
		Download URI:
			Google：https://chrome.google.com/webstore/detail/%E7%BA%A2%E6%9D%8F/heehjpdocpefckjobfgnfdbhoebhphkf?hl=zh-CN
	Main Inviate Page URI
		http://honx.in/guide?account=471030698@qq.com#/8
	HACK REFERENCE
		http://bindog.github.io/blog/2014/07/03/analysis-and-hack-of-hongxin/
		http://bindog.github.io/blog/2014/08/17/hack-hongxing-2nd/
		http://huts.cc/2015-07-03/%E6%9C%80%E6%96%B0%E7%BA%A2%E6%9D%8F%E5%87%BA%E5%A2%99%E7%A0%B4%E8%A7%A3%E6%96%B9%E6%B3%95%EF%BC%88%E4%BA%B2%E6%B5%8B%E6%9C%89%E6%95%88%EF%BC%89/
		进入chrome的扩展程序界面
			输入如下网址：chrome://extensions/
		勾选开发者模式
			搜索：红杏
			获取ID：
				ID： npacipdgogmamniefcahnbddckbejjoc
			点击背景页
				选中source标签
				左侧选中，js/services/userManager.js
				解密并格式化js代码（eval()加密）
					只格式化
						单击文本编辑窗口的{}
					解密并格式化
						http://tool.lu/js/
		根据上述ID，进入如下目录（可直接使用everything神器搜索ID）
			C:\Users\chenhaixin\AppData\Local\Google\Chrome\User Data\Default\Extensions\npacipdgogmamniefcahnbddckbejjoc\2.1.5_0
			notepad++打开userManager.js
			搜索如下一处			
				if (data.level) {
					$rootScope.user.role = ROLES.VIP
				} else if (data.name) {
					$rootScope.user.role = ROLES.USER
				} else {
					$rootScope.user.role = ROLES.GUEST
				}
			在上段代码后添加：

				$rootScope.user.profile.anonymous = false;
				$rootScope.user.profile.no_password = false;
				$rootScope.user.profile.until = 4070908800;
				$rootScope.user.profile.level = 'VIP';
				$rootScope.user.role = ROLES.VIP
				$rootScope.proxies = [{"group":"t19","scheme":"HTTPS","port":443,"name":"hz.ali.0304.d.8","host":
				"kfc0202c1.pw","fail":-76,"latency":312,"speed":206,"stability":0.998}];				
			加密之
				http://tool.lu/js/
		重启浏览器
