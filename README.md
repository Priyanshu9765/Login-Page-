// Login-Page

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="http://unpkg.com/boxicons@2.1.4/css/boxicons.min.css">
    <link rel="stylesheet" href="https://fonts.googleapis.com/css?family=Tangerine">
    <title>Modern Website</title>
    <style>
        *{
            margin: 0;
            padding: 0%;
            box-sizing: border-box;
          font-family: sans-serif;
        }
        :root{
            --primary-color:#c6c3c3;
            --second-color:#ffffff;
            --black-color:#000;

        }
        body {
            background-image: url("background nature.png");
            background-position: center;
            background-size: cover;
            background-repeat: no-repeat;
            background-attachment: fixed;
        }
        #{
            text-decoration: underline;
        }
        .wrapper{
            width: 100%;
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            background-color: rgba(0,0,0,0.2);
        }
        .login_box{
            position: relative;
            width: 450px;
            backdrop-filter: blur(25px);
            border: 2px solid var(--primary-color);
            border-radius: 15px;
            padding: 7.5em 2.5em 4em 2.5em;
            color:var(--second-color)
            box-shadow: 0px 0px 10px 2px rgba(0,0,0,0.2);
        }
        .login-header{
            position: absolute;
            top: 0;
            left: 50%;
            transform: translate(-50%);
            display: flex;
            align-items: center;
            justify-content: center;
            background-color: var(--primary-color);
            width: 140px;
            height: 70px;
            border-radius: 0 0 20px 20px;
            
        }
        .login-header::before{
            content: "";
            position: absolute;
            top: 0;
            left: -30px;
            width: 30px;
            height: 30px;
            border-top-right-radius: 50%;
            background: transparent;
            box-shadow: 15px 0 0 0 var(--primary-color);
        }
        .login-header::after{
            content: "";
            position: absolute;
            top: 0;
            left: -30px;
            width: 30px;
            height: 30px;
            border-top-right-radius: 50%;
            background: transparent;
            box-shadow: -15px 0 0 0 var(--primary-color);
        }
        .input_box{
            position:relative;
            display: flex;
            flex-direction: column;
            margin: 20px 0;
        }
        .input-field{
            width: 100%;
            height: 75px;
            font-size: 15px;
            background: transparent;
            color: var(--second-color);
            padding-inline: 20px 50px;
            border: 2px solid var(--primary-color);
            border-radius: 30px;
            outline: none;
        }
        #user{
            margin-bottom: 15px;
        }
        .label{
            position: absolute;
            top: 7px;
            left: 20px;
            transition: 0.2%;
        }
        .input-field:focus ~ .label
        .input-field:valid.label{
            position: absolute;
            top: 10px;
            left: 20px;
            font-size: 14px;
            background-color: var(--primary-color);
            border-radius: 30px;
            color: var(--black-color);
            padding: 0 10px;
        }
        .icon{
            position: absolute;
            top: 10px;
            right: 25px;
            font-size: 20px;
        }
        .remember-forget{
            display: flex;
            justify-content: space-between;
            font-size: 15px;
        }
        .input-submit{
            width: 100px;
            height: 50px;
            background: #ececec;
            font-size: 25px;
            font-weight: 500;
            border: none;
            border-radius: 30px;
            cursor: pointer;
            transition: 0.3%;
        }
        .input-submit:hover{
            background: var(--second-color);
        }
        .register{
            text-align: center;
        }
        .register #{
            font-weight: 500;
        }
        @media only screen and (max-width:564px){
            .wrapper{
                padding: 20px;
            }
            .login_box{
                padding: 7.5em 1.5em 4em 1.5em;
            }
        }
    </style>
</head>
<body>
    <div class="wrapper">
        <div class="login_box">
            <div class="login_header">
                <span>Login</span>

                <div class="input_box">
                    <input type="text" id="user" 
                    class="input-field" required>
                    <label for="user" class="label">Username</label>
                    <i class="bx bx-user icon"></i>
                </div>

                <div class="input_box">
                <input type="Password" id="pass" 
                class="input-field" required>
                <label for="pass" class="label">Password</label>
                <i class="bx bx-lock-alt icon"></i>

            </div>

            <div class="remember-forget">
                <div class="remember-me">
                    <input type="checkbox" id="remember">
                    <label for="remember">Remember me</label>
                </div>
                <div class="Forget">
                    <a href="#">Forget Password</a>
                </div>
            </div>
        </div>
        <div class="input_box">
            <input type="submit" class="input-submit" value="Login">
        </div>
        <div class="register">
            <span>Dont't have an account?
                <a href="#"Register></a>
            </span>
          
        </div>
    </div>
</body>
</html>
