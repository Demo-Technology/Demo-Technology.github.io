<script>
	import Spacer from "./Spacer.svelte";

    let year = new Date().getFullYear();

</script>
<div class="footer">
    <div id="topsection">
        <div id="logosection">
            <div id="logo">
                <img src="/images/logos/w_logo.png" alt="logo" />
                <div class="section-text-title">
                DEMO TECHNOLOGY
                </div>
            </div>
            <div id="serving" class="section-text-title">
                Serving the greater Orlando area and beyond.
            </div>
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

    .footer
    {
        width: 100%;
        height:20rem;

        margin-top:10vh;

        background-color: black;
        color:white;

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

    #linksection
    {
        width:50%;
        height:100%;
    }

    #socials
    {
        display: flex;
        justify-content: center;
        align-items: center;
    }

    #socials img
    {
        width: 1.75rem;
        transform:scale(1);
        transition: .25s;
    }

    #socials img:hover
    {
        transform:scale(1.1);
        transition: .25s;
    }

    #logo
    {
        display:flex;
        justify-content: center;
        align-items: center;
    }

    #serving
    {
        padding-top:1.5rem;
        font-size: 1.25rem;
    }


</style>