<template>
    <div class="container-fluid p-0 m-0">
        <Navbar />
        <div class="container py-4">
            <h1>About Me</h1>
            <p class="p-lg">Web Developer ◦ Student ◦ Creative</p>
            <p class="my-2">
                I strive to always keep passion and a solution based mindset
                at the forefront of my work. Anyone can throw together a website, 
                my goal is to create the most streamlined, user friendly
                experiences possible. <br/><br/>I'm 24 years old and currently 
                employed full time by Virtus Media as a Digital Media 
                Manager, which has broadened my skill set considerably and 
                afforded me an intimate look into the link between web 
                development, product creation and marketing. In addition to 
                this experience, I'm also currently pursuing a degree in Software 
                Development and plan to continue working full time to build my 
                experience while in school.
                </p>
                <div class="d-flex flex-column mt-4">
                    <h5>
                        Technologies I Work With
                    </h5>
                    <p>These are some of the languages and tools I've used to build applications and websites in production and that I feel comfortable jumping into a new codebase or project with.</p>
                    <ul class="align-items-center d-flex tech">
                        <li>HTML</li>
                        <li>CSS</li>
                        <li>Javascript</li>
                        <li>PHP</li>
                        <li>MySQL</li>
                        <li>VueJS</li>
                        <li>Nuxt</li>
                        <li>Node</li>
                        <li>Express</li>
                        <li>WordPress</li>
                        <li>Azure</li>
                        <li>HandlebarsJS</li>
                        <li>Ghost</li>
                        <li>MJML</li>
                        <li>Python</li>
                        <li>Postgres</li>
                        <li>Stripe API</li>
                        <li>Sendgrid API</li>
                        <li>Git / Github</li>
                    </ul>
                </div>
                <div class="d-flex flex-column mt-2">
                    <h5>
                        Technologies I've Dabbled With
                    </h5>
                    <p>These are some things I've played around with either creating applications for school or in small personal projects, and that I'd love a chance to dive deeper into.</p>
                    <ul class="tech align-items-center d-flex">
                        <li>React</li>
                        <li>MySQL</li>
                        <li>Django</li>
                        <li>Flask</li>
                        <li>Laravel</li>
                        <li>Kotlin</li>
                        <li>Discord API</li>
                    </ul>
                </div>
            <div class="d-flex my-2 align-items-center flex-row justify-content-around">

            </div>
            <h2 class="colored-text">Experience</h2>
            <div class="col-12 shadow round justify-content-start py-2">
                <div class="d-flex flex-row flex-wrap">
                    <div class="col-md-1 col-4 d-flex align-items-center justify-content-end py-2 h-100">
                        <img src="https://i.imgur.com/iy1RRUt.jpg" alt="Virtus Media Logo" class="w-100 rounded-circle" />
                    </div>
                    <div class="d-flex flex-column justify-content-end pb-0 mb-0 text-light">
                        <h5>Web Developer</h5>
                        <h6>Virtus Media</h6>
                        <h6>March 2021 - Current</h6>
                    </div>
                    <ul class="col-11 justify-self-end d-flex">
                        <li>Refactored existing codebase of main PB Alerts web application with two backend engineers in NuxtJS and Node with Express to increase performance and greatly reduce code redundancy/clashing package dependencies.</li>
                        <li>Built a web scraping application in Node and express to populate dynamic, hand coded email templates.</li>
                        <li>Contributed to PHP WordPress themes for various media partners.</li>
                        <li>Created a variety of new products under the direction of the CEO and COO with various technologies.</li>
                        <li>Improved community engagement by creating email system from the ground up with ExpressJS, Postgres, and the Sendgrid API.</li>
                    </ul>
                </div>
            </div>
        </div>
        <Footer />
    </div>
</template>

<script>
    export default {
        name: 'AboutPage',

        transition: 'default',
    }
</script>

<style scoped>
    * {
        color: var(--primary-light);
    }

    .p-lg {
        font-size: 1.3em;
        font-weight: 600;
        letter-spacing: 1.2px;
    }

    .bold {
        font-weight: 600;
    }

    .round {
        border-radius: 10px;
        border: 1px solid rgba(255, 255, 255, .3);
        background: linear-gradient(145deg, rgba(255, 255, 255, .3), rgba(255, 255, 255, 0));
    }

    .round ul {
        display: flex;
        flex-direction: column;
    }

    .round li {
        margin: .5rem;
    }
</style>
