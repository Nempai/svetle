<svetle:head>
    <title>Партфолио</title>
</svetle:head>

<!--<div class="container">
    <h1>Мои проекты</h1>
    <div class="apps">
        {#each routes as page}
        <div class="app">
            <h2>{page.title}</h2>
            <p>{page.body}</p>
            <p class="readmore">
                <a class="link" href={`/project/apps/${page.id}`}>
                    Читать далее
                </a>
            </p>
        </div>
        {/each}
    </div>
</div>-->

<svelte:head>
    <title>Имя Фамилия</title>
    </svelte:head>
    
    <div class='container'>
        <div class='info'>
            <div class='animate-background'>
                <div class='container info-container'>
                    <div class='info-text'>
                        <h1>
                            <p class='animate-text-1'>Я фронтенд программист,</p>
                            <p class='text-2'>А это мой сайт с моими работами.</p>
                        </h1>
                    </div>
                    <h2 class='subtitle'>
                        На моем сайте вы можете увидеть статьи и мои проекты
                        А так же вы можете со мной связаться во вкладке "Обо мне"
                    </h2>
                    <div style='color:black' class='scroll-button animate-scroll' tabindex='0'>
                        <a href='/about'>Click Here</a>
                        <div class='arrow'>→</div>
                    </div>
                </div>
            </div>
        </div>
    </div>
    
    <div class='background-div'></div>

    

<script>
    import { routes } from './routes.js'
</script>

<style>
    .container {
        margin:50px auto;
        max-width:800px;
        padding: 0 20px;
    }

    .apps {
        display:grid;
        grid-template-columns: 1fr 1fr;
        grid-gap:20px;
    }

    .app {
        border:1px silid #ddd;
        padding:10px;
        box-shadow:0 0 10px #eee;
    }

    .link {
        color: rgb(10,10,139)
    }

    .info {
        text-align: center;
        position: relative;
    }
    .info-container {
        height: 100%;
        display: flex;
        flex-direction: column;
        justify-content: center;
        text-align: left;
        align-items: start;
    }
    .container {
        max-width: 1400px;
        margin: 190px 0 0 2.5rem;
    }

    .info h1 {
        font-size: 4rem;
        margin: 0;
    }
    .info h1 p {
        position: relative;
        font: inherit;
        margin: 0;
        text-align: left;
        line-height: 130%;
        width: fit-content;
        font-weight: 800;
        letter-spacing: -0.03em;
    }
    .info h2 {
        max-width: 65ch;
        font-weight: 200;
        margin-top: 0.50rem;
    }

    .background-div {
        background-color: #ecebe8;
        width: 100%;
        height: 56vh;
        margin: -205px auto;
    }
    .info .info-text {
        position: relative;
    }
    .scroll-button {
        display: flex;
        border: none;
        outline: none;
        cursor: pointer;
    }
    .scroll-button .arrow {
        margin-left: 0.50rem;
    }
</style>
