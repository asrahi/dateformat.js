# dateformat.js
	PHP date() 형식의 javascript Date.prototype.format

# example
	var now = new Date();
	now.format('Y-m-d H:i:s');
	"2019-07-21 07:43:52"

# format
	https://www.php.net/manual/en/function.date.php

	* 연
		- Y 연도의 완전한 숫자 표현, 4 숫자 예시: 1999나 2003 
		- y 연도의 두 숫자 표현 예시: 99나 03 

	* 월
		- F January나 March 같은 월의 완전한 글자 표현 January에서 December 
		- m 0이 붙는 월 숫자 표현 01에서 12 
		- M 월의 축약 글자 표현, 3 문자 Jan에서 Dec 
		- n 0이 붙지 않는 월 숫자 표현 1에서 12 

	* 일
		- d 일, 앞에 0이 붙는 2 숫자 01에서 31 
		- D 요일 글자 표현, 3 문자 Mon에서 Sun 
		- l (소문자 'L') 요일의 완전한 글자 표현 Sunday에서 Saturday 
		- w 요일 숫자 표현 0(일요일)에서 6(토요일) 

	* 시간
		- a 오전과 오후의 소문자 am 또는 pm 
		- A 오전과 오후의 대문자 AM 또는 PM 
		- g 0이 붙지 않는 12시간 형식 시 1에서 12 
		- G 0이 붙지 않는 24시간 형식 시 0에서 23 
		- h 0이 붙는 12시간 형식 시 01에서 12 
		- H 0이 붙는 24시간 형식 시 00에서 23 
		- i 0이 붙는 분 00에서 59 
		- s 초, 0이 붙음 00에서 59 
