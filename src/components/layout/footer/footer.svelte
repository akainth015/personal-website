<script>
    import ContentWrapper from "../contentWrapper/contentWrapper.svelte";
    import SocialButtons from "components/UI/socialButtons/socialButtons.svelte";

    import { labels } from "content";

    const scrollToTop = () => window.scroll({ top: 0, behavior: "smooth" });
</script>

<style lang="scss">
    @import "footer";
</style>

<footer class="top-clip">
    <ContentWrapper>
        <article>
            <span>{labels.contact.name}</span>
        </article>

        <article>
            <b>{labels.footer.legalNotice}</b>
            <ul>
                <li>{labels.footer.copyright}</li>
                <li>{labels.contact.name}</li>
            </ul>
        </article>

        <article>
            <b>{labels.footer.contact}</b>
            <ul>
                <li>
                    <a href="mailto:aanand@akainth.me" target="_top">{labels.footer.email}</a>
                </li>
                <li>
                    <a href="tel:{labels.contact.phoneNumber}">{labels.contact.phoneNumber}</a>
                </li>
            </ul>
        </article>

        <article>
            <b>{labels.footer.connect}</b>
            <SocialButtons/>
        </article>
    </ContentWrapper>
</footer>