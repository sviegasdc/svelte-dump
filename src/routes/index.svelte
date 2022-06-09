
<script>
    import "./../app.css";
    import Modal from "./modal.svelte"
    let modal;
    let isOpen = false;
    let nome_usuario = "jairo";
    let sensibilidades = [{name: "Aracnofobia"},{name:"Glossofobia"},{name:"Nictofobia"},{name:"Claustrofobia"}];
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
            <p class="dados">
                <!-- dados do usuário para edição -->
                <input placeholder="Nickname" value="Nickname">
                <input placeholder="Email" type="email" value="jairo@email.com">
                <input placeholder="Senha" type="password" value="Senha">
                <p class="form-label">Fotossenssivel? 
                    <input type="checkbox" />
            </p>
            <!-- abiri um modal com as opções de sensibilidade do banco -->
            <p><button name="buttons4" on:click={() => (isOpen = !isOpen)}  class="btn btn-outline-light btn-sm">Sensibilidades</button></p>
            <Modal bind:this={modal} {isOpen}>
                <div class="tela_modal">
                    <h2 class="modal_title">Selecione suas sensibilidades</h2>
                    {#each sensibilidades as sensibilidade}
                        <p class="sensibilidade">{sensibilidade.name}<input type="checkbox"></p>
                    {/each}
                </div>
            </Modal>
            <button type="button" class="btn btn-outline-light btn-lg">Salvar</button>
        </div>
    </div>
    <!-- pode mudar a imagem só clicando nela -->
    <div class="user_image">
        <img
        src="https://cdn-icons-png.flaticon.com/512/149/149071.png"
        alt="Imagem de perfil"
        width="200px"
        height="200px"/>
    </div>
    <!-- <div class="edit_button">
        <button type="button" class="btn-circle">Editar</button>
        botão ou estilizar o input <input class="input-circle" type="file">
    </div>-->
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
    .tela_modal{
        display: flex;
        flex-flow: row wrap;
        align-items: flex-start;
    }
    .modal_title{
        font-family: Verdana, Geneva, Tahoma, sans-serif;
        color: white;
       
    }
    .sensibilidade{
        padding-top: 10px;
        color: white;
        font-family: Verdana, Geneva, Tahoma, sans-serif;
        font-size: large;
        text-align: center;
        display: table-column;
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
    .dados > input{
        margin-bottom: 10px;
        font-family: Verdana, Geneva, Tahoma, sans-serif;
        outline: none;
        border-radius: 6px;
        border-width:1px;
        height: 30px;
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
    .user_image:hover{
        cursor: pointer;
    }
    /* MUDAR ISSO embaixo*/ 
    .user-name{
        color:aquamarine;
    }
    /* .btn-circle {
        width: 60px;
        height: 60px;
        padding: 6px 0px;
        border-radius: 40px;
        text-align: center;
        font-size: 12px;
        line-height: 1.42857;
        margin-top: 400px;
        outline: none;
    }
    .edit_button{
        margin-top: -445px;
        margin-left: 975px;
    } */

</style>
