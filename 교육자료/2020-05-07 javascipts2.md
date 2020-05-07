# html 최종

```html
<! DOCTYPE html>
<html>

<head>
	<meta charset="UTF-8">
	<title>score table</title>
</head>

<body>
	<h1>학생 점수 입력</h1>
	<input type= "text" name = "stu" placeholder= "학생이름" />
	<input type= "text" name = "kor" placeholder= "국어점수" />
	<input type= "text" name = "eng" placeholder= "영어점수" />
	<input type= "text" name = "sci" placeholder= "과학점수" />
	<button class= "btn" onClick = "input()">입력</button>

</body>
	<script>
	var num= 0;
	
	function input(){
		var jStu = document.getElementsByName("stu")[0]; //value 값을 출력하지 않고 list값 [0]을 출력한다
		var jKor = document.getElementsByName("kor")[0];
		var jEng = document.getElementsByName("eng")[0];
		var jSci = document.getElementsByName("sci")[0];
		var Sum = calSum(parseInt(jKor.value),parseInt(jEng.value),parseInt(jSci.value)); 
		var Avg = calTot(Sum);
		num = num + 1;  //var로 새롭게 변수 만들 필요 x 
		
		createObject("input","text","number",num);
		createObject("input","text","학생이름",jStu.value);  
		createObject("input","text","국어점수",jKor.value);
		createObject("input","text","영어점수",jEng.value);
		createObject("input","text","과학점수",jSci.value);
		createObject("input","text","합계",Sum);
		createObject("input","text","평균",Avg);
		createObject("br");
		
		clearValue(jStu); //'jStu' string 값으로 들어가므로 '' 없애주기
		clearValue(jKor);
		clearValue(jEng);
		clearValue(jSci);
		
	}
	//calSum 3변수의 합
	function calSum(jKor,jEng,jSci){
		return jKor+jEng+jSci;
	}
	
	//calTot 합/3
	function calTot(Sum){
		return Sum/3;
	}
	
	//createObject 태그이름,타임,이름,값 지정
	function createObject(tagName,type,name,value){
		var obj = document.createElement(tagName);
		obj.type = type;
		obj.name = name;
		obj.value = value;
		document.body.appendChild(obj);
	}

	function clearValue(a){ 
		a.value=""; 
	}

	</script>
</html>
```

# JavaScript

```html
var jStu = document.getElementsByName("stu")[0];
```
- value 값을 출력하지 않고 list값 [0]을 출력한다

```html
var Sum = calSum(parseInt(jKor.value),parseInt(jEng.value),parseInt(jSci.value));
```
- Sum 변경

#추가 정리

```html
.createElement('h1')
<h1></h1>  -> 출력

.createTextNode('My Text')  -> 선택한 요소에 텍스트를 추가
```

```html
<script>
  var jp = document.createElement('button'); ->새로운 요소를 만들어줌
  var jptext = document.createTextNode('click) ; -> 클릭이라는 문구 노드를 생성
  jp.appendChild(jptext);  -> jp 에 jptext 추가 
</script>
```
![사진](./img/2020-05-07.PNG)
