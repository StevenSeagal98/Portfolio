<template>
    <div class="container d-flex flex-row flex-wrap mt-4 py-2 px-4">
        <div class="col-12 text-white">
            <h1>Recent Projects</h1>
        </div>
        <!--Card 1-->
        <div class="row justify-self-start my-2 d-flex flex-row p-2 align-items-center">
            <div class="col-md-6 col-12 text-light text-cont first">
                <h6 class="small feat">Featured Project</h6>
                <h4>PB Alerts</h4>
                <div class="align-content-center d-flex py-2">
                    <p class="my-auto">A modern SSR Nuxt and Express web application built with speed and SEO in mind. This was a unique opportunity for me to work with a small team of talented devs while taking responsibility for front-end stack choices and design.</p>
                </div>
                <ul class="tech px-0">
                    <li class="pr-2 pl-0">Vue</li>
                    <li>Nuxt</li>
                    <li>Express</li>
                    <li>BootstrapVue</li>
                    <li>Wordpress Api</li>
                </ul>
                <div class="col-12 px-0">
                    <a href="https://pbalerts.com" target="_blank" class="u-bounce">
                        <b-icon icon="arrow-up-right-circle-fill" class="icon mr-2"></b-icon>
                        Live Site
                    </a>
                </div>
            </div>
            <div class="col-md-6 col-12 second">
                <img src="https://i.imgur.com/b2MZlWk.png" class="rounded card-img shadow" />
            </div>
        </div>

        <!--Card 2-->
        <div class="row ml-auto my-5 d-flex flex-row align-items-center">
            <div class="col-md-6 col-12">
                <img src="https://i.imgur.com/YiF6EhV.jpg" class="rounded card-img shadow" />
            </div>
            <div class="col-md-6 col-12 text-light text-cont">
                <h6 class="small feat">Featured Project</h6>
                <h4 class="">Rest & Retire</h4>
                <div class="align-content-center d-flex py-2">
                    <p class="my-auto">I built the custom theme and email templating portions of this tri-monthly stock market newsletter service with Ghost CMS, NodeJS, and the MJML templating engine.</p>
                </div>
                <ul class="tech px-0">
                    <li class="pl-0">Node JS</li>
                    <li>Handlebars JS</li>
                    <li>MJML</li>
                    <li>Ghost CMS</li>
                    <li>CSS</li>
                </ul>
                <div class="col-12 px-0">
                    <a href="https://posts.restandretire.com" target="_blank" class="u-bounce">
                        <b-icon icon="arrow-up-right-circle-fill" class="icon mr-2"></b-icon>
                        Live Site
                    </a>
                </div>
            </div>
        </div>
        <!--Card 3-->
        <div class="row my-2 d-flex flex-row align-items-center">
            <div class="col-md-6 col-12 text-light text-cont first">
                <h6 class="small feat">Featured Project</h6>
                <h4 class="">Insider Trading Newsletter</h4>
                <div class="align-content-center d-flex py-2">
                    <p class="my-auto">Insider Trading is a tri-weekly email newsletter built by webscraping the highest value insider trades at regular intervals and formatting the data into an HTML email template.</p>
                </div>
                <ul class="tech px-0">
                    <li class="pr-2 pl-0">Express</li>
                    <li>MJML</li>
                    <li>Mailgun API</li>
                    <li>Cheerio JS</li>
                    <li>Node Cron</li>
                    <li>Azure</li>
                </ul>
                <div class="col-12 px-0">
                    <a href="https://try.pbalerts.com/insider-trading-abc/" target="_blank" class="u-bounce">
                        <b-icon icon="arrow-up-right-circle-fill" class="icon mr-2"></b-icon>
                        Live Site
                    </a>
                </div>
            </div>
            <div class="col-md-6 col-12 second">
                <img src="https://i.imgur.com/WoqHKEf.jpg" class="rounded card-img shadow" />
            </div>
        </div>
    </div>
</template>

<script>
    import { BIcon, BIconGlobe, BIconGithub, BIconArrowUpRightCircleFill } from 'bootstrap-vue';
    export default {
        name: 'ProjectsNew',

        components: {
            BIcon,
            BIconGlobe,
            BIconGithub,
            BIconArrowUpRightCircleFill
        },
    }
</script>

<style scoped>
* {
    position: relative;
}

h1 {
    font-size: 3rem;
    text-align: center;
}

.feat, .tech {
    color: #e0e0e0;
}

.card-header {
    background: var(--dark-blue);
}

.card {
    background: var(--dark-bg);
    color: var(--primary-light);
    border-radius: 10px;
}

.card ul {
    display: inline;
    text-align: left;
    display: inline-flex;
    flex-wrap: wrap;
    padding: 0 !important;
}

.card li {
    padding: 0 .5rem;
    text-align: left;
}

.img-link:after {
    display: none;
}

.icons * {
    color: var(--tea-green);
}

a {
    color: var(--tea-green);
    position: relative;
    text-decoration: none;
}

.text-cont {
    padding: 1rem;
}

li:last-of-type {
    padding-right: 0;
}
.row:nth-of-type(2) {
    margin-top: 4rem !important;
}

.row:nth-of-type(2) .text-cont ul {
    padding-left: 0;
}

img {
    transition: all ease .2s;
}

img:hover {
    transform: scale(1.02);
}

.icon {
    color: var(--tea-green);
}

@keyframes underline {
    0% {
        width: 20%;
    }

    50% {
        width: 90%;
    }

    75% {
        width: 70%;
    }

    100% {
        width: 80%;
    }
}

.first {
    order: 1;
}

.second {
    order: 2;
}

@media screen and (max-width: 531px) {
    .second {
        order: 1;
    }
    .first {
        order: 2;
    }
}

</style>