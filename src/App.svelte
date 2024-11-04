<script lang="ts">
    import rushLogo from '/rush_logo.svg'
    import report from '/bringing_the_rush_programming_language_to_the_s390x_architecture.pdf'
    // NOTE: Will only be used if the HPI link dies.
    // import article from '/article.pdf'
</script>

<main id="app">
    <a href="https://github.com/rush-rs" target="_blank" rel="noreferrer">
        <img src={rushLogo} id="logo" alt="rush Logo" />
    </a>

    <h1>The rush Programming Language: <a href="https://www.ibm.com/history/system-390" target="_blank" rel="noreferrer"><b>S/390x</b></a> Version</h1>
    <h2>
        A simple programming language for researching different ways of program execution and
        compilation.

        <br>
        Forked to support code generation for IBM S/390x GNU Assembly.
    </h2>

    <!-- <div id="rush-demo"> -->
    <!--     <div id="rush-demo__src"> -->
    <!--         {@html currRush} -->
    <!--     </div> -->
    <!--     <button> -->
    <!--         <a href="https://play.rush-lang.de" target="_blank" rel="noreferrer"> Code Yourself </a> -->
    <!--     </button> -->
    <!-- </div> -->

    <div id="buttons">
        <button>
            <a href={report} target="_blank" rel="noreferrer"> Technical Report </a>
        </button>
        <button>
            <a href="https://github.com/rush-rs/rush/tree/s390x/crates/rush-compiler-s390x" target="_blank" rel="noreferrer"> GitHub </a>
        </button>
        <button>
            <a href="https://hpi.de/artikel/studierende-lernen-auf-ibm-grossrechner-mit-echtzeit-ki/" target="_blank" rel="noreferrer"> IBM Event at HPI </a>
        </button>
    </div>

    <p>
        Created by <a href="https://github.com/MikMuellerDev/" target="_blank" rel="noreferrer"
            >Mik Müller</a
        >
        and <a href="https://github.com/RubixDev/" target="_blank" rel="noreferrer">Silas Groh</a>.
    </p>

    <p id="footnote">
        Note: Since this project is part of a research project, the language cannot be considered
        production-ready.
    </p>
</main>

<style lang="scss">
    @use './mixins' as *;

    :root {
        font-family: Inter, system-ui, Avenir, Helvetica, Arial, sans-serif;
        line-height: 1.5;
        font-weight: 400;

        font-synthesis: none;
        text-rendering: optimizeLegibility;
        -webkit-font-smoothing: antialiased;
        -moz-osx-font-smoothing: grayscale;
        -webkit-text-size-adjust: 100%;
    }

    a {
        font-weight: 500;
        color: #646cff;
        text-decoration: inherit;
    }

    :global(body) {
        margin: 0;
        background-color: white;
        height: 100vh;
        width: 100vw;
    }

    #app {
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        text-align: center;
        height: 100vh;
        padding: 0 2rem;
    }

    h1 {
        font-size: 3.2em;
        line-height: 1.1;

        @include mobile {
            font-size: 2.3em;
        }
    }

    h2 {
        @include mobile {
            font-size: 1em;
        }
    }

    #buttons {
        padding: 2em;

        @include mobile {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            gap: 0.5rem;
        }
    }

    #logo {
        height: 6em;
        padding: 1.5em;
        will-change: filter;
        transition: filter 300ms;

        @include mobile {
            height: 4rem;
        }
    }

    #logo:hover {
        filter: drop-shadow(0 0 2em #646cffaa);
    }

    #footnote {
        color: #888;

        @include mobile {
            font-size: 0.7rem;
        }
    }

    button {
        border-radius: 8px;
        border: 1px solid transparent;
        padding: 0.6em 1.2em;
        font-size: 1em;
        font-weight: 500;
        font-family: inherit;
        background-color: #1a1a1a;
        color: white;

        a {
            color: white;
            transition: color 0.1s;
        }

        cursor: pointer;
        transition: border-color 0.25s;

        @include mobile {
            font-size: 0.94rem;
        }
    }

    button:hover {
        border-color: #646cff;

        a {
            color: #646cff;
        }
    }
    button:focus,
    button:focus-visible {
        outline: 4px auto -webkit-focus-ring-color;
    }

    /* #rush-demo { */
    /*     &__src { */
    /*         background-color: #282c34; */
    /*         width: 80%; */
    /*     } */
    /**/
    /*     width: 40%; */
    /*     display: flex; */
    /*     justify-content: space-between; */
    /*     align-items: center; */
    /* } */
</style>
