## ESTE CODIGO E UM INTERFACE DE UM LOGIN FEITO POR HTML E CSS ##
<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Login | Projeto </title>
    <link rel="stylesheet" href="./style.css">
</head>
<body>
    <div class="container">
        <div class="box loginbox">
            <div class="details dtsignin">
                <h2>Login</h2>
                <div class="box-wrapper">
                    <input type="text" placeholder="Login">
                    <label for="#">Login</label>
                    <i class="fa-solid fa-user"></i>
                </div>
                <div class="box-wrapper">
                    <input type="Senha" placeholder="Senha">
                    <label for="#">Senha</label>
                    <i class="fa-solid fa-user"></i>
                </div>
                <div class="checkbox">
                    <input type="checkbox">
                    <span> Salvar senha ?</span>
                </div>
                <button id="btnlogin">Login</button>
                <p>Não possui cadastro ? <a href="#">Cadastrar</a></p>
            </div>
</body>
</html>


## Esse abaixo é o CSS ##

*{
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    list-style: none;
    text-decoration: none;
    font-family: 'poppins';

}
.container{
    min-height: 100vh;
    width: 100%;
    background: url(./imagem/uma-pintura-de-um-lago-de-montanha-com-uma-montanha-ao-fundo_188544-9126.avif);
    background-size: cover;
    background-position: center;
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 18px;

}
.box{
    height: 500px;
    width: 400px;
    background-color: rgba(255, 255, 255, 0.04);
    border: 0.2px solid rgba(255, 255, 255, 1);
    border-radius: 12px;
    backdrop-filter: blur(5px);
    position: relative;
    overflow: hidden;
    transition: .6s;

}
.box::after{
    position: absolute;
    content: "";
    height: 120%;
    width: 150%;
    top: -35%;
    left: 50%;
    background-size: cover;
    border-radius: 58%;
    transform: translate(-50%,-50%);
    z-index: -1;
    transition: .6s;

}
.box:hover:after {
    top: -36%;

}
.details{
    height: 100%;
    width: 100%;
    display: flex;
    flex-direction: column;
    padding: 4%;
    align-items: center;
    justify-content: flex-start;
    gap: 18px;

}

.dtsignin{
    position: absolute;
    top: 0;
    right: 0;
    padding: 12% 15%;

}

h2{
    color: #fff;
    font-size: 2.7rem;
    transition: .6s;

}

.box:hover h2{
    transform: translateY(-8px) scale(1.05);
}


.box-wrapper{
    position: relative;
    height: 50px;
    width: 100%;
    margin-top: 8px;
    
}

input{
    height: 40px;
    width: 100%;
    border: none;
    outline: none;
    background-color: #fff;
    padding: 0 8px;
    border-radius: 8px;

}

input::placeholder{
    transition: .6s;
}

.box-wrapper:hover input::placeholder{
    position: absolute;
    top: -12px;
    opacity: 0;

}
label{
    position: absolute;
    top: -20px;
    left: 0;
    color: rgba(255, 255, 255, 1);
    opacity: 0;
    transition: .6s;
}

.box-wrapper:hover label{
    top: -25px;
    opacity: 1;

}

.checkbox{
    display: flex;
    justify-content: start;
    align-items: center;
    width: 100%;
    color: #111142;
    margin-top: -14px;

}

input[type="checkbox"]{
    height: 14px;
    width: 14px;
    margin-right: 8px;
    
}

.checkbox span{
    color: #fff;
    font-weight: 500;
}

.box-wrapper i{
    position: absolute;
    top: 12px;
    right: 5%;
    color: #32349b;
}

button{
    height: 50px;
    width: 100%;
    border: none;
    border-radius: 8px;
    color: #fff;
    background-color: #32349b;
    letter-spacing: 1.2rem;
    font-size: 400;
    cursor: pointer;
    margin-top: 8px;
    
}

p{
    font-weight: 500;
}


p,p a{
    color: #fff;
    letter-spacing: 0.12;

}

p a{
    color: rgba(7, 42, 107, 0.8);
    font-weight: 600;
    text-decoration: underline;
}
