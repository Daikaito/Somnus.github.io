# Java中的輸出与輸入
①Java輸出固定句式：
System.out.println();

②Java輸入三步曲：   
import java.util.Scanner;//1.導包：導入Scanner這個包，這個步驟必須放在類定義的上方  
Scanner sc=new Scanner(System.in);//2.創建對象：表示要用Scanner這個類，只有sc這個變量名可以變，其他都不能變  
int a=sc.nextInt();//3.接收數據：只有a這個變量名可以變，其他都不能變  

③制表符'\t'的作用：在打印的時候，自動將前面字符串的長度補齊到8或8的整數倍，最少補1个空格，最多補8个空格

④換行符'\n'的作用：在打印的時候，自動在插入的位置換行

### 示例代碼：
```Java
import java.util.Scanner;//導包：導入Scanner這個包,這個步驟必須放在類定義的上方
public class Input_Output {
    public static void main(String[] args) {
        //換行符\n的使用
        System.out.println("換行");
        System.out.println("換"+'\n'+"行");
        System.out.println("換\n行");
        //製表符\t的使用
        System.out.println("Name"+"Age");
        System.out.println("Name"+'\t'+"Age");
        System.out.println("Name\tAge");//合并進去也可以，只是結構沒有上面的形式清晰
        System.out.println("Tomoyo"+'\t'+"20");
        System.out.println("Jack"+'\t'+"18");

        //輸入與輸出的使用：對兩個10以内的數字求和
        System.out.println("請輸入要進行求和的兩個數字：");
        Scanner sc=new Scanner(System.in);//創建對象：表示要用Scanner這個類
        int a=sc.nextInt();//輸入加數a
        int b=sc.nextInt();//輸入加數b
        while(a<0||a>10) {
            System.out.println("數字a不合法，請輸入0-10之間的數字！");
            a = sc.nextInt();
        }
        while(b<0||b>10) {
            System.out.println("數字b不合法，請輸入0-10之間的數字！");
            b = sc.nextInt();
        }
        int sum=a+b;//求和
        System.out.println("兩數之和爲："+sum);
        //System.out.println(a);
    }
}
```

### 代碼運行結果：
![DHF3D~2K}WG7_1PP@JN7%32](https://user-images.githubusercontent.com/95532380/224869588-c18ade67-5689-4fa7-9108-783cd478e90e.png)
