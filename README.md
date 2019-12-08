# Finaly
综合性实验  学生选课系统设计
---------
一、实验目的
##
1.分析学生选课系统  
2.使用GUI窗体及其组件设计窗体界面  
3.完成学生选课过程业务逻辑编程  
4.基于文件保存并读取数据  
5.处理异常    

二、实验要求
##
一、系统角色分析及类设计  
例如：学校有“人员”，分为“教师”和“学生”，教师教授“课程”，学生选择课程。
定义每种角色人员的属性，及其操作方法。
属性示例：	人员（编号、姓名、性别……）  
教师（编号、姓名、性别、所授课程、……）  
			学生（编号、姓名、性别、所选课程、……）  
二、要求:  
1.设计GUI窗体，支持学生注册、课程新加、学生选课、学生退课、打印学生选课列表等操作。  
2.基于事件模型对业务逻辑编程，实现在界面上支持上述操作。  
3.针对操作过程中可能会出现的各种异常，做异常处理。  
4.基于输入/输出编程，支持学生、课程、教师等数据的读写操作。  
三、核心代码
##
               	File f = new File("d:" + File.separator + "test.txt"); /// 声明File 对象
			// 第2步：通过子类实例化父类对象
			// OutputStream out = new FileOutputStream(f);
			FileOutputStream out = null;
			try {
				out = new FileOutputStream(f);
			} catch (FileNotFoundException e1) {
				// TODO Auto-generated catch block
				e1.printStackTrace();
			}
			// 准备好一个输出的对象
			try {
				out = new FileOutputStream(f);
			} catch (FileNotFoundException e1) {
				// TODO Auto-generated catch block
				e1.printStackTrace();
			}
			// 写入
		   //写入姓名 String str =textField2.getText();
		    String str2=textField.getText();
		    String str3=passwordField1.getText();
        
           File f = new File("d:" + File.separator + "chooseclass.txt"); /// 声明File 对象
    			// 第2步：通过子类实例化父类对象
    			// OutputStream out = new FileOutputStream(f);
    			FileOutputStream out = null;
    			try {
    				out = new FileOutputStream(f);
    			} catch (FileNotFoundException e1) {
    				// TODO Auto-generated catch block
    				e1.printStackTrace();
    			}
    			// 准备好一个输出的对象
    			try {
    				out = new FileOutputStream(f);
    			} catch (FileNotFoundException e1) {
    				// TODO Auto-generated catch block
    				e1.printStackTrace();
    			}
    			// 获取选课信息
    		    String str2=allInfo.getText();
    		    try {
    			  	out.write(str2.getBytes("UTF-8"));
    				out.close();
    			} catch (IOException e1) {
    				// TODO Auto-generated catch block
    				e1.printStackTrace();
    			}
          
四、运行截图
##

![Image text](https://github.com/augusttail/Finaly/blob/master/%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_20191208230228.png)  
![Image text](https://github.com/augusttail/Finaly/blob/master/%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_20191208230247.png)  
![Image text](https://github.com/augusttail/Finaly/blob/master/%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_20191208230307.png)  
![Image text](https://github.com/augusttail/Finaly/blob/master/%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_20191208230329.png)  

五、说明
##
学生选课系统，可以进行账号注册，并将账号信息存在txt中，利用注册的账号进行登录选课，登录验证等，选课信息同样存在txt中，可以进行修改。更新txt即可。
六、编程感想
这次编程花费时间比较久，特别是信息的存储，还有就是信息的时候，比如你注册的时候，写入的姓名，学号，密码，三个信息，存的时候吧他全部存进去，然后取的时候，要取姓名和密码，不知道怎么实现，取的时候只能一通取出来，还有就是io流存放信息，容易出现乱码，在编写的时候要注意统一。
