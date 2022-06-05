
<script>
    import "./../app.css";
    let nome_usuario = "jairo";
    let imgSrc ="https://cdn.discordapp.com/attachments/852888241349853230/863477151914524722/brand.png";
</script>

<head>
    <link
        rel="stylesheet"
        href="https://cdn.jsdelivr.net/npm/bootstrap@4.3.1/dist/css/bootstrap.min.css"
        integrity="sha384-ggOyR0iXCbMQv3Xipma34MD+dH/1fQ784/j6cY/iJTQUOhcWr7x9JvoRxT2MZw1T"
        crossorigin="anonymous"
    />
</head>

<header>
    <a href="/" class="logo movie-link">
        <img src={imgSrc} alt="SparkOfJoy" height="42" width="42" />
        <h3 class="name">SparkOfJoy</h3>
    </a>

    <div class="right-box">
        <div class="form" />

        <div class="user-box">
            <p class="user-name">
                {nome_usuario}
            </p>
            <div class="user-button">
                <a href="/login" style="cursor: pointer;">ggg 999</a>
            </div>
        </div>
    </div>
</header>

<body>
    
    <div class="user_d_container">
        <div class="corpo">
            <h1 class="title">Editar perfil</h1>
            <p class="user-name">
                {nome_usuario}
            </p>
            <p class="form-label">Nickname <button name="buttons1"class="btn btn-sm btn-outline-light">Editar</button></p>
            <p class="form-label">Email <button name="buttons2" class="btn btn-sm btn-outline-light">Editar</button></p>
            <p class="form-label">Senha <button name="buttons3" class="btn btn-outline-light btn-sm">Editar</button></p>
            <p class="form-label">Fotossenssivel? 
            <input type="checkbox" />
            </p>
            <p><button name="buttons4" class="btn btn-outline-light btn-sm">Sensibilidades</button></p>
            
            <button type="button" class="btn btn-outline-light btn-lg">Salvar</button>
        </div>
    </div>
    <div class="user_image">
        <img
        src="https://cdn-icons-png.flaticon.com/512/149/149071.png"
        alt="Imagem de perfil"
        width="200px"
        height="200px"/>
    </div>
    <div class="edit_button">
        <button type="button" class="btn-circle">Editar</button>
    </div>
</body>

<style>
    header {
        background-color: #212529;
        display: flex;
        color: white;
        justify-content: space-between;
        align-items: center;
        padding: 10px 0 10px 0;
    }
    body{
        background-color: black;
    }
    .corpo > p{
        font-size: large;
        font-family: Verdana, Geneva, Tahoma, sans-serif;
    }
    .corpo > .user-name {
        font-size: xx-large;
        font-family: Verdana, Geneva, Tahoma, sans-serif;
    }
    .corpo > .title{
        padding-top: 15px;
        padding-bottom: 10px;
    }
    input[type=checkbox] {
    transform: scale(1.3);
    }
    button[name=buttons1]{
        margin-left: 20px;
    }
    button[name=buttons2]{
        margin-left: 58px;
    }
    button[name=buttons3]{
        margin-left: 50px;
    }
    button[name=buttons4]{
        font-size: 18px;
    }
    input[type=checkbox]{
        margin-left: 12px;
    }
    .user_d_container {
        background-color: #212529;
        color: white;
        text-align: center;
        border-radius: 25px;
        width: 500px;
        height: 450px;
        margin-top: 50px;
        margin-left: 300px;
    }
    .user_image {
        margin-top: -375px;
        margin-left: 850px;
        width: 500px;
    }
    /* MUDAR ISSO embaixo*/ 
    .user-name{
        color:aquamarine;
    }
    .btn-circle {
        width: 60px;
        height: 60px;
        padding: 6px 0px;
        border-radius: 40px;
        text-align: center;
        font-size: 12px;
        line-height: 1.42857;
        margin-top: 400px;
    }
    .edit_button{
        margin-top: -445px;
        margin-left: 975px;
    }

</style>
