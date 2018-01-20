- awk 작업을 하다보면, 액션이후 '1'를 써 주는 경우가 있는데.  

	가령 파일을 읽어서 가장 첫번째 라인에 header를 추가하는 경우,  

 	    > awk 'NR==1{$0="This is Test"}1' input.txt

 	awk { } 액션 이후 1를 추가한다.  

stackoverflow에 동일한 의문을 제기했고,
 
  https://stackoverflow.com/questions/20262869/why-does-1-in-awk-print-the-current-line

  결론은,

    > the always-true condition "1" prints each line (you could even use "42", or "19", or any other nonzero value if you want; "1" is just what people traditionally use).


