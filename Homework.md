# java-basic
메가스터디 IT 아카데미 3기 ( 자바기본 )

1. year를 입력 받고 윤년 판별 
   1) 400의 배수는 윤년
   2) (1)이 아닌 100의 배수는 평년
   3) (2)가 아닌 4의 배수는 윤년
   4) 그 외 모두 평년

   ```
   1600 (O)
   1500 (X)
   1504 (O)
   1501 (X)
   2020 (O)
   2000 (O)
   2100 (X)
   ```



```java
package day03_28;

import java.util.Scanner;

public class Test01 {
		public static void main(String[] args) {
			Scanner sc = new Scanner(System.in);
			
			System.out.println("년도를 입력하시오");
			int year = sc.nextInt();
			
			System.out.println((year%400)==0 ? "윤년": (year%100)==0 ?
					"평년" : (year%4)==0 ? "윤년":"평년");
		
		}
}

```

