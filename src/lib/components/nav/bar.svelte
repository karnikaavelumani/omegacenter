<nav>
    <div class="container">
        <div class="logo-container">
            <a href="/" class="logo">
                <img src="/assets/omega.svg" alt="logo" />
                <h3>Omegacenter</h3>
            </a>
        </div>
    </div>
</nav>

<style>
    nav {
        background-color: #d3d3d3;
        padding: 10px 0;
    }

    .container {
        display: flex;
        justify-content: space-between;
        align-items: center;
        max-width: 1200px;
        margin: 0 auto;
        padding: 0 20px;
    }

    .logo-container {
        display: flex;
        align-items: center;
    }

    .logo {
        text-decoration: none;
        color: #000;
        display: flex;
        align-items: center;
    }

    .logo img {
        max-height: 40px;
        margin-right: 10px;
    }

    .logo h3 {
        font-weight: 300;
        font-size: 20px;
    }

    @media (max-width: 768px) {
        .container {
            padding: 0 10px;
        }

        .logo h3 {
            display: none;
        }
    }

    @media (max-width: 480px) {
        .logo img {
            max-height: 30px;
        }
    }

</style>