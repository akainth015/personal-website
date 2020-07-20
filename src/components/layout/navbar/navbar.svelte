<script>
    import { labels } from "content";

    export let workAnchor;
    export let aboutAnchor;

    let yOffset = 0;
    let translate;
    let previousScrollPosition = yOffset;

    const handleScroll = () => {
        if (Math.abs(yOffset - previousScrollPosition) > 100) {
            translate = yOffset < previousScrollPosition ? "0" : "-100%";
            previousScrollPosition = yOffset;
        }
    };

    window.onscroll = handleScroll;
</script>

<svelte:window bind:scrollY={yOffset}/>

<style lang="scss">
    @import "navbar";
</style>

<header style="transform: translateY({translate});">
    <div class="wrapper">
        <img src="/assets/icons/logo192.png" alt="">
        <p>Aanand Kainth</p>

    </div>
</header>