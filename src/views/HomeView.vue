<template>
  <section>
    <div id="animate">
      <img src="https://mrshane06.github.io/personal-portfolio-images/logos/Logo2.png" id="logo">
    </div>
    <bod class="bod">
      <div>
        <div class="wave"></div>
        <div class="wave"></div>
        <div class="wave"></div>
      </div>
    </bod>
    <div>
      <h2 class="greetings">Hello there , my name is Keegan Niekerk: <br> and I am an Aspiring Fullstack Developer.</h2>
      <br>
      <div id="links">
        <p><a href="https://github.com/mrshane06" target="_blank"><img src="https://mrshane06.github.io/vue-portfolio-images/logos/github%20logo.png"  class="git1" ></a></p>
        <p><a href="https://www.linkedin.com/in/keegan-niekerk-bb1278309/" target="_blank"><img src="https://mrshane06.github.io/vue-portfolio-images/logos/linkedin.png"  class="linkedin" ></a></p>
      </div>
      <a href="/" target="_blank"><button class="CV"> View My CV </button></a>
    </div>
    <br><br>
    <hr>
  </section>

  <section id="about">
        <h1 id="gun">About</h1>
          <div id="about_info">
            <div>
              <h2 class="aboutHead">A little bit about me:</h2>
              <section v-for="about in aboutData()" :key="about">
                        <about-comp>
                            <template #about>
                              <img :src='about.me' id="me">
                            </template>
                        </about-comp>
                        <about-comp>
                            <template #about>
                              <h4 class="aboutText">{{about.about}}</h4>
                            </template>
                        </about-comp>
              </section>
            </div>
            <div class="meep">
              <div>
                <h2 class="whoop">Technical Skills</h2>
              </div>
              <div class="bottom">
                  <section v-for="skills in skillsData()" :key="skills">
                          <skills-comp>
                              <template #img>
                                <img :src='skills.img' id="skill">
                              </template>
                              <template #skill>
                                <h4 class="skillText">{{skills.skill}}</h4>
                              </template>
                          </skills-comp>
                  </section>
              </div>
              <div>
                  <h2 class="whoop1">Soft Skills</h2>
              </div>
              <div class="bottom2">
                <section v-for="soft in softSkillsData()" :key="soft">
                  <soft-skills-comp>
                    <template #softImg>
                      <img :src='soft.softImg' id="skill">
                    </template>
                    <template #soft>
                      <h4 class="skillText">{{soft.soft}}</h4> 
                    </template>
                  </soft-skills-comp>
                </section>
              </div>
              <div>
                  <h2 class="">Badges & Achievements</h2>
              </div>
              <div class="bottom3">
                <section v-for="ach in achievementsData()" :key="ach">
                  <achievements-comp>
                    <template #badges>
                      <img :src='ach.badges' id="achieve">
                    </template>
                    <template #name>
                      <h4 class="skillText">{{ach.name}}</h4> 
                    </template>
                  </achievements-comp>
                </section>
              </div>
            </div>
        </div>
     </section>

</template>

<script>
import AboutComp from '@/components/AboutComp.vue'
import SkillsComp from '@/components/SkillsComp.vue';
import SoftSkillsComp from '@/components/SoftSkillsComp.vue';
import AchievementsComp from '@/components/AchievementsComp.vue';
export default {
  components:{
    AboutComp,
    SkillsComp,
    SoftSkillsComp,
    AchievementsComp
  },
  methods:{
        aboutData(){
            return this.$store.state.about
        },
        skillsData(){
            return this.$store.state.skills
        },
        softSkillsData(){
            return this.$store.state.softSkills
        },
        achievementsData(){
            return this.$store.state.achievements
        },
    },
    computed:{
        getData(){
            return this.$store.dispatch ('getData')
        }
    },
    mounted(){
        this.getData
    }
}
</script>

<style scoped>

.bod {
    margin: auto;
    font-family: -apple-system, BlinkMacSystemFont, sans-serif;
    overflow: auto;
    background: linear-gradient(315deg, rgba(101,0,94,1) 3%, rgba(60,132,206,1) 38%, rgba(48,238,226,1) 68%, rgba(255,25,25,1) 98%);
    animation: gradient 15s ease infinite;
    background-size: 400% 400%;
    background-attachment: fixed;
}

@keyframes gradient {
    0% {
        background-position: 0% 0%;
    }
    50% {
        background-position: 100% 100%;
    }
    100% {
        background-position: 0% 0%;
    }
}

.wave {
    background: #b3cf99;
    border-radius: 1000% 1000% 0 0;
    position: fixed;
    width: 200%;
    height: 12em;
    animation: wave 10s -3s linear infinite;
    transform: translate3d(0, 0, 0);
    opacity: 0.8;
    bottom: 0;
    left: 0;
    z-index: -1;
}

.wave:nth-of-type(2) {
    bottom: -1.25em;
    animation: wave 18s linear reverse infinite;
    opacity: 0.8;
}

.wave:nth-of-type(3) {
    bottom: -2.5em;
    animation: wave 20s -1s reverse infinite;
    opacity: 0.9;
}

@keyframes wave {
    2% {
        transform: translateX(1);
    }

    25% {
        transform: translateX(-25%);
    }

    50% {
        transform: translateX(-50%);
    }

    75% {
        transform: translateX(-25%);
    }

    100% {
        transform: translateX(1);
    }
}

/* home */
@keyframes rotate{
100% {transform: rotate(360deg);}
}

#logo{
margin-top: 280px;
height: 185px;
width: 185px;
animation: rotate 5s infinite ease;
}
.greetings{
  margin-bottom: 0;
}
#links{
  display: flex;
  justify-content:center;
  gap: 1em;
}
.linkedin{
  width: 50px;
  height: 50px;
  border-radius: 100%;
}
.git1{
  width: 50px;
  height: 50px;
  border-radius: 100%;
}
button{
  background-color: #ccd8c1;
  color: #2c3e50;
  font-family:Cambria, Cochin, Georgia, Times, 'Times New Roman', serif;
  width: 100px;
  height: 30px;
  border-radius: 10px;
}
button:hover{
  box-shadow: 1px 1px 1px;
}
.CV{
  margin-bottom: 100px;
}
hr{
  margin-top: 68px;
}

/* Media Queries */

/* 840px */

@media only screen and (max-width:840px){
#logo{
  margin-top: 50px;
}
#links{
  margin-top: 50px;
  margin-left: 90%;
}
#logo{
  height: 325px;
  width: 325px;
  padding: 20px;
  animation: rotate 5s infinite ease;
}
h2{
  padding-top: 40px;
}
button{
  margin: 30px;
}
}

/* 400px */

@media only screen and (max-width:400px){
#logo{
  margin-top: 0px;
}
button{
  margin-left: 30px;
  margin-right: 30px;
}
#links{
  margin-top: 0px;
  margin-left: 85%;
}
h2{
  padding-top: 0px;
}
#logo{
height: 200px;
width: 200px;
padding: 0px;
animation: rotate 5s infinite ease;
}
}
</style>
