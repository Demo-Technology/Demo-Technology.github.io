<script lang="ts">
</script>

<div id="navbar">
    <div class="logo">
        <a href="/">
            <img id="logoreg" src="images/logo.png" alt="logo"/>
            <img id="logoglow" src="images/logo_glow.png" alt="logo"/>
        </a>
    </div>

    <div class="navigation">
        <a href="#iot">
            IoT & Electronics
            <div class="scaler"></div>
        </a>
        <a href="#cloud">
            Cloud Services
            <div class="scaler"></div>
        </a>
        <a href="#xrtechnology">
            XR Technology
            <div class="scaler"></div>
        </a>
        <a href="#ourteam">
            Our Team
            <div class="scaler"></div>
        </a>
    </div>
</div>

<style>

#navbar
{
    width:100%;
    height:80px;
    background-color: var(--color-background-primary);

    display: flex;
    justify-content: flex-start;
    align-items: center;
    align-content: center;

    /* Stick to top of page */
    position: relative;
    top: 0;
}

.logo a
{
    display: flex;
    align-items: center;
}

.logo
{
    height: 100%;
    padding-left:1vw;
    
    display: flex;
    justify-content: center;
    align-items: center;
}

.logo img
{
    height: 85%;
    position: absolute;
}

#logoreg
{
    opacity: 1;
    z-index:5;
    transition: .5s;
}

#logoglow
{
    opacity: 0;
    transition: .5s;
}

.logo:hover #logoreg
{
    opacity:0;
    transition: .5s;
}

.logo:hover #logoglow
{
    opacity:1;
    transition: .5s;
}

.navigation
{
    font-family: "Futura Hv BT";

    position: absolute;
    right: 0;
    padding-right: 50px;

    height: 100%;

    display: flex;
}

.navigation a
{
    color: var(--color-text-primary);
    text-decoration: none;
    font-size: 1.2em;
    
    position: relative;
    margin-left: 50px;
    min-width:150px;
    height: 100%;

    display: flex;
    align-items: center;
    justify-content: center;

}

.navigation a:hover .scaler
{
    width: 100%;
    transition: .4s;
    opacity: 1;
}

.scaler
{
    background-color: var(--color-text-primary);
    width: 0%;
    height: 6%;
    opacity: 0.25;

    position: absolute;
    bottom: 0;

    transition: .4s;
}

</style>