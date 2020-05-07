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
	<input type= "text" name = "stu" placeholder= "학생이름" />  #text 에 이름은 stu  밑 표시 학생이름
	<input type= "text" name = "kor" placeholder= "국어점수" />
	<input type= "text" name = "eng" placeholder= "영어점수" />
	<input type= "text" name = "sci" placeholder= "과학점수" />
	<button onClick = "input()">입력</button> #입력을 누르면 script를 실행 하겠다

</body>
	<script>
	function input(){
		var jStu = document.getElementsByName("stu")[0].value;
		var jKor = parseInt(document.getElementsByName("kor")[0].value);
		var jEng = parseInt(document.getElementsByName("eng")[0].value);
		var jSci = parseInt(document.getElementsByName("sci")[0].value);
		var Sum = calSum(jKor,jEng,jSci);
		var Avg = calTot(Sum);
		createObject("input","text","number",1);
		createObject("input","text","학생이름",jStu);
		createObject("input","text","국어점수",jKor);
		createObject("input","text","영어점수",jEng);
		createObject("input","text","과학점수",jSci);
		createObject("input","text","합계",Sum);
		createObject("input","text","평균",Avg);
		createObject("br");
		
	}
	
	function calSum(jKor,jEng,jSci){
		return jKor+jEng+jSci;
	}
	function calTot(Sum){
		return Sum/3;
	}
	function createObject(tagName,type,name,value){
		var obj = document.createElement(tagName);
		obj.type = type;
		obj.name = name;
		obj.value = value;
		document.body.appendChild(obj);
	}
	
	</script>
</html>
```

# javascript 정리
```html
<input type= "text" name = "stu" placeholder= "학생이름" />
```
 - text 에 이름은 stu  밑 표시 학생이름

```html
<button onClick = "input()">입력</button>
```
- 입력을 누르면 script를 실행 하겠다

```html
function createObject(tagName,type,name,value){
		var obj = document.createElement(tagName);
		obj.type = type;
		obj.name = name;
		obj.value = value;
		document.body.appendChild(obj);
	}
```
- `document.creatElement`로 `tagName` 을 root document로 변수를 생성하겠다
- 그 안에 type,name,value 값을 지정하겠다
- `document.body.appendChild(obj)` 변수 obj 를 document 아래 자식노드로 추가
