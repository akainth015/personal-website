<script>
    import Navbar from "components/layout/navbar/navbar.svelte";
    import Title from "components/layout/title/title.svelte";
    import Footer from "components/layout/footer/footer.svelte";

    import Header from "components/sections/header/header.svelte"
    import Frontend from "components/sections/frontend/frontend.svelte"
    import Backend from "components/sections/backend/backend.svelte";
    import Banner from "components/sections/banner/banner.svelte";

    import { labels } from "content";

    let workAnchor, aboutAnchor, referenceAnchor;
</script>


<Navbar workAnchor="{workAnchor}" aboutAnchor="{aboutAnchor}"/>

<main>
    <!--Header-->
    <Header/>

    <!--Work-->
    <span bind:this={workAnchor}></span>
    <Title title="{labels.titles.work}" subtitle="{labels.titles.workSubtitle}"/>

    <!--Stack-->
    <span bind:this={aboutAnchor}></span>
    <Title title="{labels.titles.stack}" />
    <Frontend/>
    <Backend/>

    <Banner />
</main>

<Footer />