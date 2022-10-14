<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Registration and Login pages</title>
    <style>
        *{
            margin: o;
            padding: 0;
        }
        body{
            background-color:rgb(47, 17, 17) ;
        }
        .container{
            width: 100%;
            height: 100vh;
            font-family: sans-serif;
            background-color:rgb(187, 174, 34) ;
            color:#fff;
            display: flex;
            align-items: center;
            justify-content: center;


        }
        .card{
            width: 350px;
            height: 500px;
            box-shadow: 0 0 40px 20px rgba(3, 18, 56, 0.1);
            perspective: 1000px;
           
        }
        .inner-box{
            position: relative;
            width:100%;
            height: 100%;
            transform-style: preserve-3d;
            transition: transform 1s;
            
        }
        .card-front , .card-back{
            position: absolute;
            width:100%;
            height: 100%;
            /* background-position: center; */
            /* background-size: cover; */
            background-image: linear-gradient(rgba(130, 9, 9, 0.8),rgba(173, 96, 36, 0.8)),url('img.jpeg');
            padding: 55px;
            box-sizing: border-box;
            backface-visibility: hidden;
            border-radius: 24px;

        }
        .card-back{
            transform: rotateY(180deg);
        }
        .card h2{
            font-weight: normal;
            font-size: 29px;
            text-align: center;
            margin-bottom: 20px;


        }
        .name{
            width: 100%;
            background: transparent;
            border: 1px solid rgb(248, 244, 244);
            margin: 6px 0;
            height: 32px;
            border-radius: 20px;
            padding: 0 10px;
            box-sizing: border-box;
            outline:none;
            text-align: center;
            color: #fff;

        }
        ::placeholder{
            color: rgb(248, 243, 243);
            font-size: 12px;
        }
        button{
            width: 100%;
            background: transparent;
            border: 1px solid rgb(250, 247, 247);
            margin: 35px 0 10px;
            height: 32px;
            border-radius: 12px;
            padding: 0 10px;
            box-sizing: border-box;
            outline:none;
            text-align: center;
            color: rgb(252, 244, 244);
            cursor: pointer;
        }
        .submit-btn{
            position: relative;

        }
        .submit-btn::after{
            content: '\27a4';
            color: #333;
            line-height: 32px;
            font-size: 17px;
            height: 32px;
            width: 32px;
            border-radius: 50%;
            background: rgb(252, 250, 250);
            position: absolute;
            right: -1px;
            top: -1px;


        }
        span{
            font-size: 13px;
            margin-left: 10px;
        }
       .card .btn{
            margin-top: 70px;
        }
        .card a{
            color: #fff;
            text-decoration: none;
            display: block;
            text-align: center;
            font-size: 13px;
            margin-top: 8px;

        }

    </style>
</head>
<body>
    <div class="container">
        <div class="card">
            <div class="inner-box" id="card">
                <div class="card-front">
                    <h2>LOGIN</h2>
                    <form>
                        <input type="email" class="name" placeholder="Email-ID"required>
                        <input type="password" class="name" placeholder="password"required>
                        <button type="submit" class="submit-btn">Submit</button>
                        <input type="checkbox"><span>Remember me</span>
                        
                        
                    
                    </form>
                    <button type="button" class="btn" onclick="openRegister()">I am new here</button>
                    <a href="">Forgot password</a>
                </div>
                <div class="card-back">
                    <h2>REGISTRATION</h2>
                    <form>
                        <input type="text" class="name" placeholder="Your Name"required>
                        <input type="email" class="name" placeholder="Your Email-id"required>
                        <input type="password" class="name" placeholder="password"required>
                        <button type="submit" class="submit-btn">Submit</button>
                        <input type="checkbox"><span>Remember me</span>
                        
                        
                    
                    </form>
                    <button type="button" class="btn" onclick="openLogin()">I've an account</button>
                    <a href="">Forgot password</a>
                
                </div>
            </div>
        </div>

    </div>

    <script>

        var card = document.getElementById("card");

        function openRegister(){
            card.style.transform  = "rotateY(-180deg)";
        }
        function openLogin(){
            card.style.transform  = "rotateY(0deg)";
        }
    </script>
    
</body>
</html>
