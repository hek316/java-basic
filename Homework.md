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



/*
 * 조건연산자 문제
 * - 우리는 딸기를 팔고 있습니다. 딸기의 가격은 2000원입니다.
 *   우리의 유일한 VIP 고객이 한명 있습니다.
 *   VIP 고객의 아이디와 비밀번호는 각각 "pika"와 "pika1234"입니다.
 *   
 *   아이디, 비밀번호를 입력 받았을 때, 
 *   VIP 고객이라면 20% 할인해서 판매하세요.
 *   
 *   e.g. 
 *    
 *    ID: (콘솔창 클릭 후 입력)
 *    PW: (콘솔창 클릭 후 입력)
 *    
 *    ( VIP라면 )
 *    현재 고객님은 VIP이십니다. 20% 할인 적용하여 1600원입니다. 
 *    
 *    ( VIP가 아니라면 )
 *    현재 고객님은 일반 고객이십니다. 2000원입니다.
 *   
 */

package day03_28;

import java.util.Scanner;

public class Test02 {
		public static void main(String[] args) {
			Scanner sc = new Scanner(System.in);
			
			System.out.println("아이디를 입력하시오");
			String id = sc.next();
			
			System.out.println("비밀번호를 입력하시오");
		    String pw = sc.next();
		    
		    System.out.println("(id = pika && pw =pika) ?"+
		    		"현재 고객님은 VIP이십니다. 20% 할인"
		    		+ " 적용하여 1600원입니다 현재 고객님은 일반 고객이십니다. 2000원 입니다." );
		}

}

3.

package day03_28;

// Math.random()을 사용하여 2단 ~ 9단 중 1개를 랜덤하게 내고 
		// 답을 입력 받음
		// "정답!" 혹은 "땡!"을 출력

import java.util.Scanner;


public class Test03 {
		public static void main(String[] args) {
			Scanner sc = new Scanner(System.in);
			
			int rand = ((int)(Math.random()*8)+2);
			System.out.println(rand+"x2");
			
			System.out.println("답을 입력하시오");
			int answer = sc.nextInt();
			
			System.out.println(answer==rand*2  ? "정답!" : "땡!");
			
			
			
						
			}
}
