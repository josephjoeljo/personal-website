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
    background-color: var(--color-background);
    border-bottom: solid 2px var(--color-background-soft);

    .logo {
        color: var(--text-color);
        text-decoration: none !important;
    }

    h1 {
        font-size: 1rem;
        line-height: 2rem;
        color: var(--text-color);
        text-transform: uppercase;
        margin: 0.5rem 0rem 0.5rem 3rem;
        text-decoration: none !important;
    }

    #routes {
        margin: auto;
        display: flex;
        align-items: center;
        flex-direction: row;

        a {
            margin: 0rem 1.5rem;
            text-decoration: none;
            color: var(--text-color);
        }
    }
}
</style>