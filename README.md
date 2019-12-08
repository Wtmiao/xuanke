# xuanke
班级：计181 姓名：王同淼 学号：2018310723   
一、实验目的

  分析学生选课系统
  使用GUI窗体及其组件设计窗体界面
  完成学生选课过程业务逻辑编程
  基于文件保存并读取数据
  处理异常
二、实验要求

  设计GUI窗体，支持学生注册、课程新加、学生选课、学生退课、打印学生选课列表等操作。
  基于事件模型对业务逻辑编程，实现在界面上支持上述操作。
  针对操作过程中可能会出现的各种异常，做异常处理
三、实验过程   
1、流程图
![](https://github.com/Wtmiao/xuanke/blob/master/%E5%BE%AE%E4%BF%A1%E5%9B%BE%E7%89%87_20191208230744.png)

2、代码
JLabel a = new JLabel("请选择课程：");
	JButton r = new JButton("确定");
	JCheckBox jc1 = new JCheckBox("老师名称：安安    老师编号： 1  所授课程：高数   学分：6 地点：教202   时间：10:00am-11:00am");
	JCheckBox jc2 = new JCheckBox("老师名称：堡包    老师编号： 2  所授课程：英语   学分：5 地点：教302   时间：11:00pm-12:00pm");
	JCheckBox jc3 = new JCheckBox("老师名称：常常    老师编号： 3 所授课程： 物理   学分： 4  地点：教403  时间：13:00pm-14:00pm");
	
	Choosing(){
		setTitle("选课");
		setSize(600,250);
		setDefaultCloseOperation(EXIT_ON_CLOSE);
		setVisible(true);
		setLayout(new FlowLayout());
		
		add(a);
		add(jc1);
		add(jc2);
		add(jc3);
		add(r);
		jc1.addActionListener(this);
		jc2.addActionListener(this);
		jc3.addActionListener(this);
		r.addActionListener(this);
	}、
  public Stu(String i, String n,String p) {
	    id = i;
	    name = n;
	    password = p;
	  }
	  public String getid() {
	    return id;
	  }
	  public String getname() {
	    return name;
	  }
	  public String getpassword() {
		  return password;
	  }
      public String toString() {
		   return "  学号：" + id+ " 姓名：" + name 
				   + " 密码：" + password;
		   }
}
public void actionPerformed(ActionEvent e) {
		String s1 = jtf1.getText();
		String s2 = jtf2.getText();
	
		if(e.getSource() ==login1&&s1.equals("1")&&s2.equals("12345")) {
			new caozuo();
		} 
		else if(e.getSource()==login2) {
			new register();
			}
		else {
			JOptionPane.showMessageDialog(null, "学号或密码错误，请重新输入");
		}
		
		
	}
四、编程感想
本次实验我从头开始了解了面对对象编程，分析对象属性，设置方法处理属性等等。我在这次实验中加深了自己对面对对象编程这一方法的认识，同时也让我更加了解java的规则和编程的习惯。
