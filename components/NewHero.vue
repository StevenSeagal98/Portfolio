<template>
<div class="wrapper container col-10 rounded d-flex p-1 my-auto">
    <div class="main col-12 rounded-lg d-flex align-content-center my-auto p-0">
        <div class="col-12 w-100 hero-main d-flex align-items-center justify-content-between">
            <div class="col-md-9 col-12 p-0 mx-auto">
                <h1>Hi, I'm Nate Orona 👋</h1>
                <p>I'm a web developer specialized in the front-end of the stack with a passion for creating unforgettable user experiences and 
                    helping organizations reach their full potential. I'm always interested in trying new technologies, 
                    working with new people, and implementing interesting design ideas!<br /><br />
                    Shoot me a message, let's talk about 
                    <span class="typed-text green">{{typeValue}}</span>
                    <span class="blinking-cursor green">|</span>
                    <span class="cursor green" :class="{ typing: typeStatus }">&nbsp;</span></p>
                <a class="btn shadow green-btn-two" href="mailto:nathaniel.orona98@gmail.com">Get In Touch</a>
                <nuxt-link to="/Projects" class="btn shadow green-btn">See my work</nuxt-link>
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
    }
</script>

<style scoped>
.wrapper {
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

@media (max-width: 767px) {

  * {
    overflow-y: scroll;

  
    }
}

</style>