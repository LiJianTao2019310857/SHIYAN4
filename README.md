# SHIYAN4
## 实验目的
1.掌握Java中抽象类和抽象方法的定义； 

2.掌握Java中接口的定义，熟练掌握接口的定义形式以及接口的实现方法。

3.了解异常的使用方法，并在程序中根据输入情况做异常处理。

## 实验内容
某学校为了给学生提供勤工俭学机会，也减轻授课教师的部分压力，准许博士研究生参与课程的助教工作。此时，该博士研究生有双重身份：学生和助教教师。
1.设计两个管理接口：学生管理接口和教师管理接口。学生接口必须包括缴纳学费、查学费的方法；教师接口包括发放薪水和查询薪水的方法。

2.设计博士研究生类，实现上述的两个接口，该博士研究生应具有姓名、性别、年龄、每学期学费、每月薪水等属性。（其他属性及方法，可自行发挥）。

3.编写测试类，并实例化至少两名博士研究生，统计他们的年收入和学费。根据两者之差，算出每名博士研究生的年应纳税金额（国家最新工资纳税标准，请自行检索）。
 
## 实验要求
1.在博士研究生类中实现各个接口定义的抽象方法;

2.对年学费和年收入进行统计，用收入减去学费，求得纳税额；

3.国家最新纳税标准（系数），属于某一时期的特定固定值，与实例化对象没有关系，考虑如何用static  final修饰定义。

4.实例化研究生类时，可采用运行时通过main方法的参数args一次性赋值，也可采用Scanner类实现运行时交互式输入。

5.根据输入情况，要在程序中做异常处理。

## 实验步骤
1.定义接口声明方法。

2.在类中写出研究生应有的属性(性别，年龄，学号等)及学费和工资的算法并实现两个接口中的方法。

3.写出纳税额的算法输入月工资和学费，经过计算输出结果。

4.整理代码，消除错误。

## 核心代码
```
 public double find_tuition() {
            System.out.println("每年学费：" + tuition);
            return tuition;
        }

        public double find_salary() {
            System.out.println("每月工资：" + salary);
            return salary;
        }

        public double afford_tuition() {
            System.out.println("缴纳成功，已缴纳学费" + tuition);
            return tuition;
        }

        public double get_salary() {
            double c;
            c = salary - (salary - 800) * STANDARD;
            System.out.println("薪水已经发放，发放金额：" + c);
            return salary;
        }

        public void taxation() {
            double a;
            a = 12 * ((salary - 800) * STANDARD);
            System.out.println("每年应纳税为：" + a);
        }
    }
}
```

## 实验结果
******************研究生一*********************
姓名:唐映枫
年龄:35
编号:2019310001
性别:男
每年学费：6666.0
每月工资：1000.0
每年纳税为：480.0
******************研究生二*********************
学生姓名:黄楚桐
学生年龄:36
学生编号:2019310002
学生性别:女
每年学费：6666.0
每月工资：1100.0
每年纳税为：720.0

## 实验感想
通过此次实验使我对interface定义接口，implement实现接口有了一定了解，使我更好的懂得了接口的使用方法，同时编程能力得到了提升，使我近一步了解java的内涵。根据输入情况，在程序中做异常处理的能力。让我在以后的程序运行中更加懂的了接口的重要性。




 
