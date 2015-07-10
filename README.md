<?php
if (isset($login)) {
    if ($login->errors) {
        foreach ($login->errors as $error) {
            echo $error;
        }
    }
    if ($login->messages) {
        foreach ($login->messages as $message) {
            echo $message;
        }
    }
}
?>
<!DOCTYPE html>
<html>
<head>
    <title>Code Network</title>
    <Link rel = "ícone de atalho" type = "image / x-icon" href = "http://localhost/php-login-minimal-master/favicon.ico">
    <style>

         #geral {
            text-align: center;
            margin-top: 160px;

        }

         #geral .caixa {
             margin-left: 800px;
             width: 15%;
             height: 40%;
         }

        #geral .campo {
            font-family: tahoma, arial;
            color: black;
        }

        #geral input.login_input {
            margin-top: 15px;
            border-radius: 5px;
            outline: none;
        }

        #geral input.entrar {
            width: 140px;
            height: 25px;
            color: white;
            background: #0097a5;
            border-radius: 5px;
        }

        #geral input.entrar:hover {
            border: solid 2px black;
        }

        #geral a.registro {
            text-decoration: none;
            font-family: tahoma, arial;
            color: blue;
        }
    </style>
</head>
<body>

    <div id="geral">
        <fieldset class="caixa">
            <form method="post" action="index.php" name="loginform">

                <label class="campo">Usuário</label><br>
                    <input class="login_input" type="text" name="user_name" placeholder="Usuário" required /><br><br>

                <label class="campo">Senha</label><br>
                    <input class="login_input" type="password" name="user_password" autocomplete="off" placeholder="Senha" required /><br><br>

                <input type="submit" class="entrar"  name="login" value="Entrar" />

         </form>
    <a href="register.php" class="registro">Registre-se</a>
        </fieldset>
    </div>
</body>
</html>

