<template>
<div class="wrapper container col-10 rounded d-flex p-1 my-auto">
    <div class="main col-12 rounded-lg d-flex align-content-center my-auto p-0">
        <div class="col-12 w-100 hero-main d-flex align-items-center justify-content-between">
        <!--<div class="col-1 stagger-cont">
            <div class="col-10 border staggering-grid">
                <div class="row">
                    <div class="el el-bl"></div>
                    <div class="el el-bl-two"></div>
                    <div class="el el-bl-three"></div>
                    <div class="el el-bl-four"></div>
                    <div class="el el-bl-five"></div>
                </div>
                <div class="row">
                    <div class="el el-bl-two"></div>
                    <div class="el el-bl-three"></div>
                    <div class="el el-bl-four"></div>
                    <div class="el el-bl-five"></div>
                    <div class="el"></div>
                </div>
                <div class="row">
                    <div class="el el-bl-three"></div>
                    <div class="el el-bl-four"></div>
                    <div class="el"></div>
                    <div class="el"></div>
                    <div class="el"></div>
                </div>
                <div class="row">
                    <div class="el el-bl-four"></div>
                    <div class="el el-bl-five"></div>
                    <div class="el"></div>
                    <div class="el"></div>
                    <div class="el"></div>
                </div>
                <div class="row">
                    <div class="el el-bl-five"></div>
                    <div class="el"></div>
                    <div class="el"></div>
                    <div class="el"></div>
                    <div class="el"></div>
                </div>
            </div>
        </div>-->
            <div class="col-md-9 col-12 mx-auto">
                <h1 class="">Hi, I'm Nate Orona 👋</h1>
                <p class="p-0">I'm a web developer specialized in the front-end of the stack with a passion for creating unforgettable user experiences and 
                    helping organizations reach their full potential. I'm always interested in trying new technologies, 
                    working with new people, and implementing interesting design ideas!<br /><br />
                    Shoot me a message <a class="green u-bounce" href="mailto:nathaniel.orona98@gmail.com">here</a>, let's talk about 
                    <span class="typed-text green">{{typeValue}}</span>
                    <span class="blinking-cursor green">|</span>
                    <span class="cursor green" :class="{ typing: typeStatus }">&nbsp;</span></p>
                <nuxt-link to="/Projects"><button class="btn shadow green-btn">See my work</button></nuxt-link>
                <button class="btn shadow green-btn-two" ref="contact-btn">Get In Touch</button>
            </div>
        </div>
    </div>
</div>
</template>

<script>
    export default {
        name: 'Hero',

        data() {
            return {
                typeValue: '',
                typeStatus: false,
                displayTextArray: ['design.', 'Vue.', 'Nuxt.js.', 'Express.', 'Wordpress.'],
                typingSpeed: 100,
                erasingSpeed: 100,
                newTextDelay: 2000,
                displayTextArrayIndex: 0,
                charIndex: 0,

                projectSection: document.getElementById('projects')
            };
        },

        methods: {
            animatedBox() {
                this.$anime({
                    targets: '.staggering-grid .el',
                    scale: [
                        {value: .1, easing: 'easeOutSine', duration: 500},
                        {value: 1, easing: 'easeInOutQuad', duration: 1200}
                    ],
                    delay: this.$anime.stagger(300, {grid: [5, 5], from: 'center'}),
                    loop: true,
                });
            },

            typeText() {
                if (this.charIndex < this.displayTextArray[this.displayTextArrayIndex].length) {
                    if (!this.typeStatus) this.typeStatus = true;
                    this.typeValue += this.displayTextArray[this.displayTextArrayIndex].charAt(
                    this.charIndex
                    );
                    this.charIndex += 1;
                    setTimeout(this.typeText, this.typingSpeed);
                } else {
                    this.typeStatus = false;
                    setTimeout(this.eraseText, this.newTextDelay);
                }
            },

            eraseText() {
                if (this.charIndex > 0) {
                    if (!this.typeStatus) this.typeStatus = true;
                    this.typeValue = this.displayTextArray[this.displayTextArrayIndex].substring(
                    0,
                    this.charIndex - 1
                    );
                    this.charIndex -= 1;
                    setTimeout(this.eraseText, this.erasingSpeed);
                } else {
                    this.typeStatus = false;
                    this.displayTextArrayIndex += 1;
                    if (this.displayTextArrayIndex >= this.displayTextArray.length)
                    this.displayTextArrayIndex = 0;
                    setTimeout(this.typeText, this.typingSpeed + 1000);
                }
            },
            scrollProj() {document.querySelector('#projects').scrollIntoView({behavior:'smooth'})}
        },

        created() {
            setTimeout(this.typeText, this.newTextDelay + 200);
        },

        mounted() {
            this.animatedBox();
        }
    }
</script>

<style scoped>
.wrapper {
    min-height: 85vh;
    max-height: 80vh;
    
    display: flex;
    justify-content: center;
    color: #e5e5e5;
}

h1 {
  font-size: 4.5rem;
  font-weight: 600;
  background-image: linear-gradient(to right, var(--light-purple), #bb48bf, #f67e4d);
  background-clip: text;
  background-attachment: cover;
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}

.blinking-cursor {
  font-size: 1rem;
  color: #2c3e50;
  -webkit-animation: 1s blink step-end infinite;
  -moz-animation: 1s blink step-end infinite;
  -ms-animation: 1s blink step-end infinite;
  -o-animation: 1s blink step-end infinite;
  animation: 1s blink step-end infinite;
}

/*Hero and stagger*/
p {
    font-size: 1.2rem;
}

a {
    text-decoration: none;
}

a:hover {
    color: var(--tea-green);
}

.green-btn {
    border: 2px solid var(--tea-green);
    color: var(--secondary-light);
}

.green-btn:hover {
    background: rgba(12, 245, 116, .6);
    color: var(--dark-blue);
}
.green-btn-two {
    background: var(--tea-green);
    color: var(--dark-blue);
}

.green-btn-two:hover {
    background: rgba(12, 245, 116, .6);
    border: 2px solid var(--tea-green);
}

@keyframes blink {
  from,
  to {
    color: transparent;
  }
  50% {
    color: slategray;
  }
}

</style>