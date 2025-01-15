<template>
    <div id="navigation-bar">
        <RouterLink to="/" class="logo">
            <h1>Joel Joseph</h1>
        </RouterLink>

        <div id="routes">
            <RouterLink to="/projects" active-class="active">Projects</RouterLink>
            <RouterLink to="/resume" active-class="active">Resume</RouterLink>
        </div>
    </div>
</template>

<style>
#navigation-bar {
    width: 100%;
    height: 50px;
    display: flex;
    background-color: white;
    border-bottom: solid 2px black;

    .logo {
        text-decoration: none !important;
    }

    h1 {
        color: black;
        font-size: 1rem;
        line-height: 2rem;
        text-transform: uppercase;
        margin: 0.5rem 0rem 0.5rem 1rem;
        text-decoration: none !important;
    }

    #routes {
        margin: auto;
        display: flex;
        align-items: center;
        flex-direction: row;

        a {
            color: black;
            margin: 0rem 1.5rem;
            text-decoration: none;
        }
    }
}
</style>