<script>
</script>

<style lang="scss">
    #stack {
        min-height: 100vh;
        display: grid;
        flex-direction: column;
        align-items: center;
        grid-template-rows: repeat(4, 1fr);
        margin-bottom: 70px;
    }

    .title {
        text-align: center;
        font-size: 42px;
        font-family: var(--main-font);
        letter-spacing: 3px;
    }

    .underline {
        position: relative;
        &::before {
            content: "";
            position: absolute;
            bottom: 0;
            height: 50%;
            width: 100%;
            background-color: #6494aa;
            z-index: -1;
        }
    }
    .wrapper {
        display: grid;
        grid-template-rows: repeat(2, 1fr);
        align-items: center;
        justify-content: center;
        grid-gap: 20px;
        padding: 20px;
        background-color: lighten(#6494aa, 40%);
        margin: 0 auto;

        p {
            justify-self: center;
            letter-spacing: 1px;
            font-size: 24px;
            font-family: var(--main-font);
        }
    }

    .tech_list {
        display: flex;
        align-items: center;
        justify-content: center;
        gap: 40px;

        li {
            font-size: 20px;
            font-family: var(--main-font);
        }
    }

    @media (max-width: 660px) {
        #stack {
            grid-template-rows: auto;
            grid-gap: 35px;

            .title {
                margin-top: 95px;
                margin-bottom: 20px;
            }

            .front {
                grid-template-rows: 140px 1fr;
            }

            .back {
                grid-gap: 15px;
            }
            .future {
                grid-gap: 15px;
            }
        }

        .wrapper {
            gap: 0;
            margin: 0 50px;
        }

        .tech_list {
            display: grid;
            grid-template-columns: repeat(2, 1fr);

            li {
                justify-self: center;
            }

            &:last-child {
                text-align: center;
            }
        }

        p {
            text-align: center;
            line-height: 1.3;
        }

        .future {
            gap: 10px;
        }
    }
</style>

<section id="stack">
    <h4 class="title"><span class="underline">Technologies</span></h4>
    <div class="wrapper front">
        <p>Front End</p>
        <ul class="tech_list">
            <li>HTML</li>
            <li>CSS/SASS</li>
            <li>JavaScript</li>
            <li>React</li>
            <li>jQuery</li>
            <li>Tailwind</li>
            <li>Bootstrap</li>
            <li>Material UI</li>
        </ul>
    </div>
    <div class="wrapper back">
        <p>Back end</p>
        <ul class="tech_list">
            <li>NodeJS</li>
            <li>ExpressJS</li>
            <li>MongoDB</li>
        </ul>
    </div>
    <div class="wrapper future">
        <p>I'm going to learn in near future</p>
        <ul class="tech_list">
            <li>GraphQL</li>
            <li>TypeScript</li>
            <li>PHP</li>
            <li>MySQL</li>
            <li>Vue</li>
        </ul>
    </div>
</section>
