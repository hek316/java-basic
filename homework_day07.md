# java-basic
메가스터디 IT 아카데미 3기 ( 자바기본 )
```java
package day07.howork;
//1. 1이상 ~ 100미만의 홀수를 출력하기 

public class homework01 {
	public static void main(String[] args) {
		int n =1;
		
		while(n<100) {
			System.out.println(n);
			n+=2;
		}
	}

}
```


```java
package day07.howork;
//2. 100 부터 1까지 거꾸로 출력 
//100 99 98 ...
public class homework02 {
	public static void main(String[] args) {
		int n=100;
		while(n>0) {
			System.out.println(n);
			n--;
		}
	}

}
```

```java
package day07.howork;
//3. 구구단 5단 출력
public class homework03 {
	public static void main(String[] args) {
		int n = 1;
		while(n<10) {
			
			System.out.println("5"+"x"+n+"="+5*n);
			n++;
		}
		
	}

}

```
```java
package day07.howork;
//4. 30 + 31 + 32 + 33 + ... + 100 의 결과를 출력하세요. 4615가 나오면 정답.
public class homework04 {
	public static void main(String[] args) {
		int n, sum;
		sum =0;
		n = 30 ;
		
		while(n<=100) {
			sum+=n;
			n++;
		}
		System.out.println(sum);
	}

}
```
```java
package day07.howork;

import java.util.Scanner;

/*
 * 5. 사용자가 -1을 입력할 때까지 정수를 무한히 입력 받고 
   -1을 입력하면 입력 받은 정수들의 총합을 출력하세요.

 */

public class homework05 {
	public static void main(String[] args) {
		Scanner sc = new Scanner(System.in);
		int n ,sum ,rand;
		sum =0; n=0;
		System.out.println("정수를 입력하시오");
	    n = sc.nextInt();
	    
		
		while (n!=-1) {
			rand = (int)(Math.random()*10);
			sum+=rand; 
	    System.out.println(rand+"+"+sum+"="+sum);
	    System.out.println("정수를 입력하시오");
	    n = sc.nextInt();
	    }
		System.out.println("총합:"+sum);
	}

}

```

```java

import java.util.Scanner;

/*
 * 6.Math.random()을 사용하여 구구단 문제를 랜덤하게 내고(2~9단), 
답을 입력 받아 "정답!" 혹은 "땡.."을 출력
정답이 5번 나올 때까지 반복
 * 
 * 
 */

public class homework06 {
	public static void main(String[] args) {
		Scanner sc = new Scanner(System.in);
		int x, y ;
		int answer;
		
		
		x = (int)((Math.random()*8)+2);
		y = (int)((Math.random()*9)+1);
		
		while(x*y!=5){
			System.out.println(x+"X"+y+"=");
			answer = sc.nextInt();
			System.out.println(x*y==answer ? "정답!":"떙..");
			x = (int)((Math.random()*8)+2);
			y = (int)((Math.random()*9)+1);
				
				
		}
		System.out.println("답이 5이므로 프로그램이 종류되었습니다");
	}
	
	
	

}
```


```java
package day07.howork;

import java.util.Scanner;

/*
 * 7. Up & Down 게임 만들기
    - 컴퓨터는 1 ~ 1000 중 임의의 정수 1개를 뽑습니다.
    - 사용자는 컴퓨터가 뽑은 정수를 맞출 때까지 정수를 계속 입력 합니다.
      정답 > 입력값 의 경우 : 'Up!' 출력
      정답 < 입력값 의 경우 : 'Down!' 출력
    - 시도횟수가 15회 미만이라면 "승리!"를, 그렇지 않으면 "패배.." 를 출력하세요.
    (정답이 입력될 때까지 프로그램은 종료되지 않는 것으로 가정합니다.)
 * 
 * 
 */
public class homework07 {
	public static void main(String[] args) {
		Scanner sc = new Scanner(System.in);
		
		int n , user, cnt;
		cnt=0;
		
		n = (int)((Math.random()*1000)+1);
	  System.out.println("1~1000 사이의 정수를 입력하시오");
		user = sc.nextInt();
		
		while(n!=user) {
			if(n>user)
			System.out.println("random값:"+n +" up");
			if(n<user)
			System.out.println("random값:"+n +"down");
			cnt++;
			System.out.println("1~1000 사이의 정수를 입력하시오");
			user = sc.nextInt();
			
			
		}
		System.out.println(cnt>15 ? "승리!": "패배");
	}

}
```

```java
package day07.howork;


/*
 * 
8.
500 이하까지 피보나치 수열을 출력하라 (1부터 시작한 앞 두 수의 합이 다음 수)
 * 
 * 
 */

public class homework08 {
		public static void main(String[] args) {
			int[] a ;
			a = new int[500];
			a[1]=1;
			a[2]=1;
			int n;
			n=1;
			while(n!=501) {
				a[n+2]= a[n] + a[n+1];
			    System.out.println(a[n]);
				n++;	
			}
			
			
		}

}
```


