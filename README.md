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
           arr[2]=new char[]{'夜','来','风','雨','声'};      //定义二维数组
           arr[3]=new char[]{'花','落','知','多','少'};

           System.out.println("--横版--");

           for (int a=0;a<arr.length;a++) {
               for (int b = 0; b < arr[a].length; b++) {    //循环遍历数组，横版遍历
                   System.out.print(arr[a][b]);
               }
                if (a%2==0)
                    System.out.println("，");
                else {                                      //奇数打印“,”偶数打印“。"
                    System.out.println("。");
                }
           }

           System.out.println("--竖版--");

           for (int j=0;j<arr[0].length;j++){
               for (int i=3;i>=0;i--){
                   System.out.print(arr[i][j]);             //循环遍历数组，竖版遍历
               }
               System.out.println();
           }
           System.out.println("。，。，");
           //打印结果
            /*
            --横版--
            春眠不觉晓，
            处处闻啼鸟。
            夜来风雨声，
            花落知多少。
            --竖版--
            花夜处春
            落来处眠
            知风闻不
            多雨啼觉
            少声鸟晓
            。，。，
             */
             
              //for循环 遍历数组
             for (int i=0;i<arr.length;i++){
                 for (int j=0;j<arr[i].length;j++){
                     System.out.print(arr[i][j]);
                 }
                 System.out.println();
             }

             System.out.println("-----分割线-----");
            //foreach循环
             for (char a[]:arr){
                 for (char b : a){
                     System.out.print(b);
                 }
                 System.out.println();
             }
             
             int arr2[][]={{4,3},{1,2}};                 //定义二维数组
            System.out.println("数组中的元素是：");        //提示信息
            int i=0;                                    //外层循环计数器变量
            for (int x[]:arr2){                         //外层循环变量为一位数组
                i++;                                    //外层计数器递增
                int j=0;                                //内层循环计数器
                for (int e:x){                          //循环遍历每一个数组元素
                    j++;                                //内层循环计数器递增
                    if (i==arr2.length && j==x.length){ //判断变量是二维数组中的最后一个元素
                        System.out.print(e);            //输出二维数组中额最后一个元素
                    }else{                              //如果不是二维数组的最后一个元素
                        System.out.print(e+"、");
                    }
                }
                
                 //填充数组
           /*
            int arr[]=new int[5];   //定义一位数组 创建int型整数
            arr[0]=5;               //后面使用Arrays方法，前面的初始化是没有效果的
            arr[1]=6;               //输出结果没有改动
            Arrays.fill(arr,8);     //使用同一个值对数组进行填充
            for (int j=0;j<arr.length;j++){    //循环遍历每个数组
                System.out.println("弟"+j+"个元素是："+arr[j]);
                /*输出结果为
                弟0个元素是：8
                弟1个元素是：8
                弟2个元素是：8
                弟3个元素是：8
                弟4个元素是：8

            }
            */
            //替换数组元素
           int arr[]={1,3,5,9,8,7,6,3,5,3,6};
           Arrays.fill(arr,3,7,0);
           for (int i=0;i<arr.length;i++){
               if (arr[i]==0){
                   System.out.print("*");
               }else{
                   System.out.print(arr[i]);
               }

           }
           //对数组进行排序
           int arr[]=new int[]{13,63,33,93};    //声明数组
           Arrays.sort(arr);                    //将数组进行排序
           for (int amp:arr){                   //遍历循环排序后的数组
               System.out.print(amp+" ");       //将排序后的数组中的个元素输出
               //输出结果 13 33 63 93
           }
           
           double arr2[]=new double[]{1.3,6.3,3.3,9.3};
           Arrays.sort(arr2);
           for (double map:arr2){
               System.out.print(map+" ");
               //输出结果 1.3 3.3 6.3 9.3 
           }
           //复制数组
           int arr[]=new int[]{12,13,14};
           int newarr[]=Aarrays.copyOf(arr,5);
           for(int j=0;j<newarr.lenght;j++){
              System.out.ptint(newarr[j]);
           }
           
           int arr[]=new int[]{12,13,14,15,16,17};              //定义数组
           int newarr[]=Arrays.copyOfRange(arr,2,5);   //复制数组
           for (int i=0;i<newarr.length;i++){                   //遍历循环复制后的数组
               System.out.print(newarr[i]+" ");                 //将新数组中的元素输出
               //输出结果： 12 13 14
           }

           ///数组查询
              /*
              int arr[]=new int[]{2,9,4,25,4,10};        //定义数值
              Arrays.sort(arr);                          //对数组进行排序
              int index= Arrays.binarySearch(arr,4);//查找数组arr中元素4的索引位置
              System.out.println("4的索引位置是："+index); //将索引输出

               */
              /*
              int arr[]=new int[]{4,25,10};
              Arrays.sort(arr);                  //对数组进行排列
              int index=Arrays.binarySearch(arr,0,1,8);
              System.out.print(index);           //输出结果：-2
               */
              /*
              int ia[]=new int[]{1,8,9,4,5};            //定义数组
              Arrays.sort(ia);                          //对数组进行排序
              int index = Arrays.binarySearch(ia,4);//查找数值中ia中元素4的索引位置
              System.out.print("4的索引位置是："+index);   //输出结果： 4的索引位置是：1

               */
              //binanrySearch(Object[],int fromIndex,int toIndex,Object key)
              //定义Stering型数组arr
              String srr[]=new String[]{"ab","cd","ef","yz"};
              Arrays.sort(srr);    //讲数组进行排序
              //指定索引范围搜索元素“cd”的索引位置
              System.out.println(srr.length);
              int index = Arrays.binarySearch(srr,0,2,"cd");
              System.out.println("赵某的索引位置是："+index);//结果输出：赵某的索引位置是：1
              
              //冒泡排序
              int a[]=new int[]{63,4,24,1,3,15};      //创建数组
              //比较相邻两个元素，较大的数往后冒泡
              for (int i=1;i<a.length;i++){
                     for (int j=0;j<a.length -i;j++){
                            if (a[j]>a[j+1]){
                                   int tmp = a[j];   //把第一个元素值保存到临时变量中
                                   a[j] = a[j+1];    //把第二个元素值保存到第一个元素单元中
                                   a[j+1] = tmp;     //把临时变量（也就是第一个元素原值）保存到第二个元素中
                            }
                     }
              }

              for (int i:a){                         //遍历数组
                     System.out.print(i+">");        //输出结果：1>3>4>15>24>63>
              }
       }
}
