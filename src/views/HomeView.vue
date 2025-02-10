<template>
  <section id="home">
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
      <a href="https://mrshane06.github.io/personal-portfolio-images/Keegan%20niekerk%20CV.pdf" target="_blank"><button class="CV"> View My CV </button></a>
    </div>

  </section>
    <br><br>
    <hr id="about">
  <section>
        <h1 id="about1">Learn a bit more about me:</h1>
          <div id="about_info">
            <div>
              <!-- <h2 class="aboutHead">Learn a bit more about me:</h2> -->
              <section v-for="about in aboutData()" :key="about" data-aos="zoom-in">
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
                        <div>
                          <h2>Soft Skills :</h2>
                          <h4>Computer Literacy , Adaptability</h4>
                          <h4>Team Work , Attention To Detail</h4>
                          <h4>Communication</h4>
                        </div>
              </section>
            </div>
            <div class="meep">
              <div>
                <h2 class="whoop">Technical Skills</h2>
              </div>
              <div class="bottom">
                  <section v-for="skills in skillsData()" :key="skills" data-aos="zoom-in">
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
                  <h2 class="">Badges & Achievements</h2>
              </div>
              <div class="bottom3">
                <section v-for="ach in achievementsData()" :key="ach" data-aos="zoom-in">
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

     <br>
     <hr id="Edu">
     <br>

     <section  data-aos="zoom-in">
          <div>
            <div>
                <h2 class="eduhead">Education</h2>
            </div>
            <div class="edu">
                <section  class="ed" v-for="education in educationData()" :key="education">
                    <education-comp>
                        <template #education>
                        <h3>{{education.education}}</h3>
                        </template>
                        <br>
                        <template #image>
                            <img :src='education.image' class="eduImg">
                        </template>
                        <br>
                        <template #eduDesc>
                            <h4>{{ education.eduDesc }}</h4>
                        </template>
                        <br>
                        <template #years>
                            <h4>{{education.years}}</h4>
                        </template>
                    </education-comp>
                </section>
            </div>
            <div class="expHead">
                <h2>Experiences</h2>
            </div>
            <div class="exp">
                <section v-for="exp in experienceData()" :key="exp"  data-aos="zoom-in">
                    <experience-comp>
                        <template #company>
                            <h3>{{exp.company}}</h3>
                        </template>
                        <br>
                        <template #image>
                            <img :src='exp.image' class="eduImg">
                        </template>
                        <br>
                        <template #position>
                            <h4>{{ exp.position }}</h4>
                        </template>
                        <br>
                        <template #jobDes>
                            <h4>{{ exp.jobDes }}</h4>
                        </template>
                        <br>
                        <template #years>
                            <h4> {{exp.years}}</h4>
                        </template>
                    </experience-comp>
                </section>
            </div>
        </div>
     </section>
     <br>
     <hr id="project">
     <br>

     <section>
      <div>
        <div>
            <h2 class="projectsHead">Previous Projects</h2>
        </div>
        <div class="projects">
            <section id="proj-card" v-for="projects in projectsData()" :key="projects" data-aos="zoom-in">
              <projects-comp>
                <template #Pimage>
                    <img :src="projects.Pimage" class="project-image" >
                </template>
                <template #Pname>
                    <h3 class="project-title">{{ projects.Pname }}</h3>
                </template>
                <template #description>
                    <h5 class="project-text">{{ projects.description }}</h5>
                </template>
                <template #github>
                    <button class="project-btn1"><a :href="projects.github" target="_blank">Github</a></button>
                </template>
                <template #live>
                    <button class="project-btn2"><a :href="projects.live" target="_blank">Hosted</a></button>
                </template>
                </projects-comp>
          </section>
        </div>
      </div>
     </section>

     <br>
     <hr>
     <br>

     <section id="contacts">
      <div>
        <div class="contact-head">
            <h2>Lets Get In Touch</h2>
        </div>
        <div id="whoop">
            <div class="links" data-aos="zoom-in">
                <img src="https://mrshane06.github.io/personal-portfolio-images/logos/Logo2.png" id="logo2">
                <p><img src="https://mrshane06.github.io/personal-portfolio-images/logos/gmail_icon.png" id="gmail">niekerkkeegan007@gmail.com</p>
                <p><img src="https://mrshane06.github.io/personal-portfolio-images/logos/location_icon.png" id="location">Bonteheuwel , Cape Town</p>
                <p><img src="https://mrshane06.github.io/personal-portfolio-images/logos/phone_icon.png" id="phone">081 421 4195</p>
                <p><img src="https://cdn-icons-png.flaticon.com/512/4926/4926624.png" id="git"><a href="https://github.com/mrshane06" target="_blank" class="git">github</a></p>
                <p><img src="https://cdn-icons-png.flaticon.com/512/1384/1384014.png" id="git"><a href="https://www.linkedin.com/in/keegan-niekerk-bb1278309/" target="_blank" class="git">linkedin</a></p>
            </div>
            <section id="bam" data-aos="zoom-in">
                <div class="col-lg-8 mt-5 mt-lg-0 mt-md-0 mt-sm-0">
                  <form
                    action="https://formspree.io/f/manyyavl"
                    method="POST"
                  >
                    <div class="row">
                        <div class="col-md-6 form-group">
                        <input type="text" name="name" class="form-control" id="name" placeholder="Your Name" required>
                        </div>
                        <div class="col-md-6 form-group mt-3 mt-md-0">
                        <input type="email" class="form-control" name="email" id="surname" placeholder="Your Email" required>
                        </div>
                    </div>
                    <div class="form-group mt-3">
                        <textarea class="form-control" name="comments" rows="5" placeholder="Comments" required></textarea>
                    </div>
                    <div class="text-center mt-4 send"><button id="sub" type="submit">Submit</button></div>
                    </form>
                </div>
            </section>
        </div>
    </div>
     </section>
</template>

<script>
import AboutComp from '@/components/AboutComp.vue'
import SkillsComp from '@/components/SkillsComp.vue';
import AchievementsComp from '@/components/AchievementsComp.vue';
import EducationComp from '@/components/EducationComp.vue';
import ExperienceComp from '@/components/ExperienceComp.vue';
import ProjectsComp from '@/components/ProjectsComp.vue';
export default {
  components:{
    AboutComp,
    SkillsComp,
    AchievementsComp,
    EducationComp,
    ExperienceComp,
    ProjectsComp
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
        educationData(){
            return this.$store.state.education
        },
        experienceData(){
            return this.$store.state.experiences
        },
        projectsData(){
            return this.$store.state.projects
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

/* Headers */

#about1{
  margin-top: 60px;
}

.eduhead{
  margin-bottom: 40px;
}



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
  width: 35px;
  height: 35px;
  border-radius: 100%;
}
.git1{
  width: 35px;
  height: 35px;
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
  margin: 0;
  margin-top: 10px;
  /* margin-bottom: 30px; */
  margin-left: 30px;
  margin-right: 30px;
}
#links{
  margin-top: 0px;
  margin-left: 0%;
}
h2{
  padding-top: 0px;
}
#logo{
margin-top: 155px;
height: 200px;
width: 200px;
padding: 0px;
animation: rotate 5s infinite ease;
}
}

/* 360px */

@media only screen and (max-width:360px){
#logo{
  margin-top: 0px;
}
button{
  margin: 0;
  margin-top: 10px;
  margin-left: 30px;
  margin-right: 30px;
}
#links{
  margin-top: 0px;
  margin-left: 0%;
}
h2{
  padding-top: 0px;
}
#logo{
margin-top: 155px;
height: 200px;
width: 200px;
padding: 0px;
animation: rotate 5s infinite ease;
}
}

/* education */
h2{
        margin-top: 40px;
    }
    .eduImg{
        width: 80px;
        height: 80px;
        border-radius: 20px;
    }
    .eduImg:hover{
    transform: scale(1.2);
    transition: 1s ease-in-out;
  }
    .ed{
        width: 340px;
        padding-left: 85px;
    }
    .edu{
        display: grid;
        grid-template-columns: repeat(3 ,1fr);
    }
    /* experience */
    .expHead{
        margin-top: 0;
    }
    .exp{
        width: 340px;
        padding-left: 85px;
        margin-left: 495px;
    }
    /* media queries */

    /* 840px */

    @media only screen and (max-width:840px){
    /* education */
    .ed{
        padding-left: 18px;
    }
    .edu{
        display: grid;
        grid-template-columns: repeat(2 ,1fr);
    }
    /* experience */
    .exp{
        margin-left: 150px;
    }
}

    /* 400px */

    @media only screen and (max-width:400px){
    /* education */
    h2{
        margin-top: 35px;
    }
    .ed{
        width: 340px;
        padding-left: 18px;
    }
    .edu{
        display: grid;
        grid-template-columns: repeat(1 ,1fr);
    }
    /* experience */
    .expHead{
        margin-top: 0;
    }
    .exp{
        width: 340px;
        padding-left: 0px;
        margin-left: 18px;
    }
}

    /* 360px */

    @media only screen and (max-width:360px){
    .ed{
        padding-left: 0px;
    }
    /* experience */
    .exp{
        margin-left: 0px;
    }
}

    /* 320px */

    @media only screen and (max-width:320px){
    /* education */
    .ed{
        width: 300px;
    }
    /* experience */
    .exp{
        width: 300px;
    }
}

/* Contacts */

/* head */
#whoop{
    display: flex;
}
.contact-head{
    width: 260px;
    padding-bottom: 30px;
    margin-left: 40px;
}
@keyframes rotate{
  100% {transform: rotate(360deg);}
}
#logo2{
  height: 80px;
  width: 80px;
  padding: 26px;
  animation: rotate 5s infinite ease;
}
/* links */
.links{
    border: 2px solid rgb(0, 0, 0);
    background-color: #ffffff;
    width: 18.5rem;
    height: 22rem;
    margin-bottom: 130px;
    margin-left: 100px;
    border-radius: 10px;
    margin-top: 10px;
    padding: 10px;
    text-decoration: none;
    color: rgb(0, 0, 0);
}
#gmail{
    width: 20px;
    height: 20px;
    margin-right: 10px;
}
#location{
    width: 20px;
    height: 20px;
    margin-right: 10px;
}
#git{
    width: 20px;
    height: 20px;
    margin-right: 10px;
    text-decoration: none;
    color: rgb(0, 0, 0);
}
#phone{
    width: 20px;
    height: 20px;
    margin-right: 10px;
}
.git{
    text-decoration: none;
    color: rgb(0, 0, 0);
}
/* contacts */
#bam{
    font-family:Impact, Haettenschweiler, 'Arial Narrow Bold', sans-serif;
    display: flex;
    justify-content: center;
    padding: 20px;
}
#sub{
    width: 70px;
    margin-top: 10px;
    height: 30px;
    border-radius: 60px;
    color: rgb(0, 0, 0);
    background-color: #ffffff;
    margin-left: 80px;
}
input{
  background-color: white;
  border:rgb(77, 73, 73) 2px solid;
  width: 600px;
  height: 30px;
  border-radius: 10px;
  margin: 10px;
  padding: 5px;
  margin-left: 110px;
}
textarea{
  background-color: white;
  border: rgb(77, 73, 73) 2px solid;
  width: 605px;
  height: 180px;
  margin-left: 100px;
  margin-top: 10px;
  margin-bottom: 10px;
  border-radius: 10px;
}
.button{
  background-color: white;
  border: rgb(77, 73, 73) 2px solid;
  margin-bottom: 91px;
}

    /* media queries */

    /* 840px */

@media only screen and (max-width:840px){
  .contact-head{
    padding-top: 40px;
    padding-bottom: 40px;
    width: 400px;
  }
  #whoop{
    display: block;
  }
    /* links */
  .links{
    border: 2px solid black;
    height: 340px;
    margin-left: 100px;
    margin-right: 110px;
    margin-top: 0px;
    padding: 0px;
  }
    input{
        width: 600px;
        margin-top: 10px;
        margin-left: 0px;
        padding: 5px;
        margin-left: 0px;
    }
    textarea{
        width: 605px;
        height: 180px;
        margin-left: 0px;
        margin-right: 5px;
    }
    #sub{
        margin-left: 0px;
    }
}

    /* 400px */

@media only screen and (max-width:400px){
  .contact-head{
    padding: 0px;
    padding-bottom: 30px;
    width: 400px;
  }
  #whoop{
    display: block;
  }
  .contact-head{
    width: 260px;
    padding-top: 30px;
  }
    /* links */
  .links{
    border: 2px solid black;
    width: 18.5rem;
    height: 22rem;
    margin-bottom: 50px;
    margin-left: 20px;
    border-radius: 10px;
    margin-top: 0px;
    padding: 0px;
  }
    input{
        width: 295px;
        margin-top: 10px;
        margin-left: 0px;
        padding: 5px;
        margin-left: 0px;
    }
    textarea{
        width: 300px;
        height: 200px;
        margin-left: 0px;
        margin-right: 5px;
    }
    #sub{
        margin-left: 40px;
    }
}
</style>
