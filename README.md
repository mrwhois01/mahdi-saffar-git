# MyArray(X)

 1     cout << "Destructor" << endl;
 2   }
 3   void print(void){
 4     cout << " n = " << n << endl;
 5     for(int i = 0; i < n; i++)
 6       cout << "a[" << i << "] = "
 7            << a[i] << endl;
 8   }
 9 };
10 void f1(void);
11 int main(){
12   f1();
13   return 0;
14 }
15 void f1(void){
16   double x[]{10, 12, 34, 54};
17   myArray d(x, sizeof(x)/sizeof(x[0]));
18   myArray p(d);
19   myArray q=p;
20   p.print();
21 }/*
22 copy construcotr
23 copy construcotr
24  n = 4
25 a[0] = 10
26 a[1] = 12
27 a[2] = 34
28 a[3] = 54
29 Destructor
30 Destructor
31 Destructor */
