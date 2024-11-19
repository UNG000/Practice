<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>프론트엔드프로그래밍II 복습및 스타일링</title>
    <style>
        body {
            background-color: orange;
            font-family: Arial, sans-serif;
            margin: 0;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
        }
        ol {
            background: white;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
            list-style-type: none;
            margin: 0;
            padding-left: 0;
        }
        li {
            font-size: 20px;
            padding: 15px 0;
            text-align: center;
            color: #333;
            cursor: pointer;
            transition: background-color 0.3s ease, color 0.3s ease;
        }
        li:hover {
            background-color: #f0f0f0;
        }
        h1 {
            text-align: center;
            margin-bottom: 20px;
            color: white;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.5);
            transition: color 0.3s ease;
        }

        @media (max-width: 600px) {
            li {
                font-size: 16px;
                padding: 10px 0;
            }
            ol {
                padding: 15px;
            }
            h1 {
                font-size: 18px;
            }
        }
    </style>
    <script>
        window.onload = function() {
            let listLI = document.querySelectorAll("li");

            
            listLI.forEach(item => {
                item.addEventListener('click', function() {
                    listLI.forEach(li => li.style.backgroundColor = ''); 
                    this.style.backgroundColor = 'yellow'; 
                });
            });

            
            let h1 = document.querySelector("h1");
            h1.onmouseover = function() {
                this.style.color = "black";
            }
            h1.onmouseout = function() {
                this.style.color = "white";
            }
        }
    </script>
</head>
<body>
    <div>
        <h1>12주차 프론트엔드프로그래밍II 실습 연습</h1>
        <ol>
            <li>프론트엔드프로그래밍II</li>
            <li>데이터베이스</li>
            <li>자바프로그래밍</li>
        </ol>
    </div>
</body>
</html>
