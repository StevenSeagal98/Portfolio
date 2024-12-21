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
                experiences possible. <br/><br/>I'm currently 
                employed full time by Virtus Media as a Full Stack Web Developer, which has broadened my skill set considerably and 
                afforded me an intimate look into the link between web 
                development, product creation and marketing. In addition to 
                this experience, I have an AS in Software Development and am currently working towards a BS in Computer Science.
                </p>
                <div class="d-flex flex-column mt-4">
                    <h5>
                        Technologies I Work With
                    </h5>
                    <p>These are some of the languages and tools I've used to build applications and websites in production and that I feel comfortable jumping into a new codebase or project with.</p>
                    <ul class="align-items-center d-flex tech">
                        <li>Javascript</li>
                        <li>PHP</li>
                        <li>Java</li>
                        <li>Tailwind</li>
                        <li>Spring Boot</li>
                        <li>Kotlin</li>
                        <li>Postgresql</li>
                        <li>VueJS</li>
                        <li>Express</li>
                        <li>WordPress</li>
                        <li>Azure</li>
                        <li>Python</li>
                        <li>MongoDB</li>
                        <li>Git / Github</li>
                    </ul>
                </div>
            <h2 class="colored-text">Experience</h2>
            <div class="col-12 shadow round justify-content-start py-2">
                <div class="d-flex flex-row flex-wrap">
                    <div class="col-md-1 col-4 d-flex align-items-center justify-content-end py-2 h-100">
                        <img src="https://i.imgur.com/iy1RRUt.jpg" alt="Virtus Media Logo" class="w-100 rounded-circle" />
                    </div>
                    <div class="d-flex flex-column justify-content-end pb-0 mb-0 text-light">
                        <h5>Full Stack Web Developer</h5>
                        <h6>Virtus Media</h6>
                        <h6>March 2021 - Current</h6>
                    </div>
                    <ul class="col-11 justify-self-end d-flex">
                        <li>Refactored legacy .NET web application in Vue, Node, and Postgresql to increase performance and eliminate security vulnerabilities.</li>
                        <li>Reduced build times significantly by minimizing dependencies, modernizing tooling, and streamlining build pipelines with Github Actions and Azure.</li>
                        <li>Designed and implemented a procedural email marketing and paid newsletter management service with NodeJS and Sendgrid.</li>
                        <li>Contributed to PHP WordPress themes and built custom plugins for various media partners.</li>
                        <li>Created a variety of new products under the direction of the CEO and COO with various technologies.</li>
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
