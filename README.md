# Array
Array数组
一维数组的创建及使用
二位数组的创建及使用
数组的基本操作
数组排序算法
public calss Arra{
       public static void main(String[] args){

/*
           int arr[];
           int[] arr2;  //简单的数组 不能放元素
            //三种初始化方法
           int arr3[] = new int[3];
           arr3[0] = 7;
           arr3[1] = 8;
           arr3[2] = 9;

           int b[] = new int[]{4,5,6};

           int c[]={1,2,3};

            */
           /*
            int a[]=new int[3]{4,5,6};//错误语法
            int a[]=new int[]{4,5,6}; //正确语法
            int a[]=new int[3];       //正确语法

            */

           /*
           //返回数组长度
            int arr[]= new int[2+3];
            System.out.println(arr.length);
            //输出结果是 5

            */

           int arr[]=new int[]{31,28,30,31,30,31,31,30,31,30,31};
           for (int i=0;i<arr.length;i++){
               System.out.println((i+1)+"月有"+arr[i]+"天");
           }
           
           //二维数组创建
           int mayrr[][];
           int[][] mayrr2;
           
           //二维数组初始化
           int tdarr1[][] = {{13,12},{45,2}};

           int tdarr2[][] = new int[][]{{56,34,33},{12,33,54}};

           int tdarr3[][] = new int[2][3];
           tdarr3[0] = new int[]{6,54,71};  //给第一行赋值
           tdarr3[1][0] = 63;
           tdarr3[1][1] = 10;               //给第二行赋值
           tdarr3[1][2] = 7;
           
           //   使用二维数组
           /*
           int a[][] = new int[3][4];           //定义二维数组
           for (int i=0;i<a[1].length;i++){
               for (int j=0;j<a[1].length;j++){ //循环遍历数组中的每个元素
                   System.out.print(a[i][j]);   //将数组中的元素输出
               }
               System.out.println();            //输出空格
           }
            //输出结果：0000
           //         0000
           //         0000
            */
           //数组的基本操作
           //   历遍数组
           /*
           int b[][] = new int[][]{{1},{12},{123}}; //定义二维数组
           for (int k=0;k<b.length;k++){
               for (int j=0;j<b[k].length;j++){     //循环遍历二维数组中的每一个元素
                   System.out.print(b[k][j]);       //将数组中的元素输出
               }
               System.out.println();
           }
           //结果呈梯形输出
           /*
            1
            12
            123
            */

           char arr[][]=new char[4][];
           arr[0]=new char[]{'春','眠','不','觉','晓'};
           arr[1]=new char[]{'处','处','闻','啼','鸟'};
           arr[2]=new char[]{'夜','来','风','雨','声'};
           arr[3]=new char[]{'花','落','知','多','少'};
           for (int a=0;a<arr.length;a++) {
               for (int b = 0; b < arr[a].length; b++) {
                   System.out.print(arr[a][b]);
               }
                if (a%2==0)
                    System.out.println("，");
                else
                    System.out.print("。");
           }
       }
}
