## HTML Display 속성.

<img src="https://github.com/bamjun/blog/blob/main/images/display%20image.png?raw=true" style="width=500px;">


      
CSS에서 `display` 속성은 HTML 요소가 문서 내에서 어떻게 보여질지를 결정합니다. 이 속성은 요소의 레이아웃 및 박스 모델의 동작을 제어하는 데 중요한 역할을 합니다. 주요 `display` 값에는 다음과 같은 것들이 있습니다:  


      

# 기본 html 예제
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>display</title>
    <style>
        .parent{
            display: inline-block;
            margin: 0 20px;

        }
        .child{
            width: 150px;
            height: 150px;
            background-color: skyblue;

        }
        .parent:nth-child(2) > .child{
            background-color: red;
        }
    </style>

</head>
<body>
    <div class="parent">
        <div class="child"></div>
    </div>
    <div class="parent">
        <div class="child"></div>
    </div>
    <div class="parent">
        <div class="child"></div>
    </div>
    <div class="parent">
        <div class="child"></div>
    </div>
    
</body>
</html>
```


      
<img width="520" alt="image" src="https://github.com/bamjun/blog/assets/21354840/8e0b00b1-cec9-4868-8b30-4a58360927b0">


        

1\. `block`: 요소가 블록 레벨 요소처럼 동작하게 합니다. 즉, 새로운 줄에서 시작하고, 가능한 최대 너비로 확장됩니다.
     
  
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>display</title>
    <style>
        .parent{
            /* display: inline-block; */
            display: block;
            margin: 0 20px;

        }
        .child{
            width: 150px;
            height: 150px;
            background-color: skyblue;

        }
        .parent:nth-child(2) > .child{
            background-color: red;
        }
    </style>

</head>
<body>
    <div class="parent">
        <div class="child"></div>
    </div>
    <div class="parent">
        <div class="child"></div>
    </div>
    <div class="parent">
        <div class="child"></div>
    </div>
    <div class="parent">
        <div class="child"></div>
    </div>
    
</body>
</html>
```


      
<img width="209" alt="image" src="https://github.com/bamjun/blog/assets/21354840/fd6fbebd-ca0c-49ab-8d2e-8ab6240cef00">

    
<img width="123" alt="image" src="https://github.com/bamjun/blog/assets/21354840/302b02ad-db2a-430a-8750-46a49bf7b35f">

      
2\. `inline`: 요소가 인라인 요소처럼 동작하게 합니다. 즉, 새로운 줄을 시작하지 않고, 내용의 너비만큼만 차지합니다.
     
       
      
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>display</title>
    <style>
        .parent{
            /* display: inline-block; */
            /* display: block; */
            display: inline;
            margin: 0 20px;

        }
        .child{
            width: 150px;
            height: 150px;
            background-color: skyblue;

        }
        .parent:nth-child(2) > .child{
            background-color: red;
        }
    </style>

</head>
<body>
    <div class="parent">
        <div class="child"></div>
    </div>
    <div class="parent">
        <div class="child"></div>
    </div>
    <div class="parent">
        <div class="child"></div>
    </div>
    <div class="parent">
        <div class="child"></div>
    </div>
    
</body>
</html>
```

           
<img width="194" alt="image" src="https://github.com/bamjun/blog/assets/21354840/9c6e004e-415f-4317-b814-7a5db1f73899">
    
  
<img width="122" alt="image" src="https://github.com/bamjun/blog/assets/21354840/5673b851-5971-4cc5-8133-96dc80e5cfc1">  
  
      
    
3\. `inline-block`: 요소가 인라인 요소처럼 줄에 배치되지만, 블록 요소처럼 너비와 높이를 가질 수 있습니다.


                
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>display</title>
    <style>
        .parent{
            /* display: inline-block; */
            /* display: block; */
            /* display: inline; */
            display: inline-block;
            margin: 0 20px;

        }
        .child{
            width: 150px;
            height: 150px;
            background-color: skyblue;

        }
        .parent:nth-child(2) > .child{
            background-color: red;
        }
    </style>

</head>
<body>
    <div class="parent">
        <div class="child"></div>
    </div>
    <div class="parent">
        <div class="child"></div>
    </div>
    <div class="parent">
        <div class="child"></div>
    </div>
    <div class="parent">
        <div class="child"></div>
    </div>
    
</body>
</html>
```
  
    
<img width="199" alt="image" src="https://github.com/bamjun/blog/assets/21354840/fa58dd72-5821-4c2d-8191-34562c031532">
    
      
  
<img width="512" alt="image" src="https://github.com/bamjun/blog/assets/21354840/af086058-8939-4bab-881c-a174e4710825">
       
      
     
4\. `none`: 요소가 화면에 표시되지 않습니다. 이 요소와 이 요소의 자식 요소들은 레이아웃에서 완전히 제거되며, 공간도 차지하지 않습니다.    
5\. `flex`: 요소를 플렉스 컨테이너로 만들어, 그 안의 자식 요소들을 플렉스 아이템으로 배치합니다.    
6\. `grid`: 요소를 그리드 컨테이너로 만들어, 그 안의 자식 요소들을 그리드 아이템으로 배치합니다.    
    
`display` 속성은 웹 페이지의 레이아웃을 조정하는 데 매우 유용하며, 다양한 화면 크기와 기기에 대응하는 반응형 웹 디자인을 구현하는 데에도 중요한 역할을 합니다.
