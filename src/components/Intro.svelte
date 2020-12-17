<script>
</script>

<style lang="scss">
    #intro {
        min-height: 100vh;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        gap: 120px;
    }

    .title {
        font-size: 46px;
        font-family: var(--main-font);
        letter-spacing: 3px;
    }

    .emoji {
        font-size: 60px;
    }

    .wrapper {
        display: flex;
        justify-content: center;
        align-items: center;
        gap: 30px;
    }

    .underline {
        position: relative;
        &::before {
            content: "";
            position: absolute;
            bottom: 0;
            height: 50%;
            width: 100%;
            background-color: #f5ed51;
            z-index: -1;
        }
    }

    @media (max-width: 880px) {
        #intro {
            padding: 0 15px;
            gap: 50px;
            margin-top: -80px;
        }

        .wrapper {
            gap: 10px;
        }
    }

    @media (max-width: 600px) {
        .title {
            font-size: 34px;
        }

        .bottom {
            text-align: center;
            line-height: 1.3;
        }
    }
</style>

<section id="intro">
    <div class="wrapper">
        <h1 class="title top">Hi, I'm <span class="underline">Adam</span></h1>
        <span class="emoji">👋</span>
    </div>
    <h2 class="title bottom">
        <span class="underline">Junior Front-end developer</span>
    </h2>
</section>
