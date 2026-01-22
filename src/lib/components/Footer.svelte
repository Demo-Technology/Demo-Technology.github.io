<script>
	import Spacer from "./Spacer.svelte";
    let year = new Date().getFullYear();
</script>

<div class="footer">
    <div id="topsection">
        <div id="logosection">
            <div id="logo">
                <img src="/images/logos/w_logo.png" alt="logo" />
                <h1 class="section-text-title">Demo Technology</h1>
            </div>
            <p id="serving" class="section-text-title">
                Serving the greater Orlando area and beyond.
            </p>
        </div>
    </div>
    <Spacer width="80%" height=".05rem" color="gray" />
    <div id="bottomsection">
        <div id="copyright">
            &copy; {year} DEMO TECHNOLOGY, LLC. ALL RIGHTS RESERVED
        </div>
    </div>
</div>

<style>

    h1 {
        text-transform: uppercase;
    }

    .footer
    {
        width: 100%;
        height:20rem;

        background-color: var(--color-dark-primary);
        color: var(--color-light-primary);

        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
    }

    #topsection
    {
        width:100%;
        height:80%;

        display:flex;
        justify-content: center;
        align-items: center;
    }

    #bottomsection
    {
        width:100%;
        height:20%;

        display:flex;
        justify-content: center;
        align-items: center;
        text-align: center;
    }

    #logosection
    {
        width:50%;
        height:100%;

        font-size:2.5rem;

        display:flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
    }

    #logosection img
    {
        width:6rem;
        margin-right:2rem;
    }

    #logo
    {
        display:flex;
        justify-content: center;
        align-items: center;
        padding: 0 1rem;
    }

    #serving
    {
        padding-top:1.5rem;
        font-size: 1.25rem;
    }
</style>