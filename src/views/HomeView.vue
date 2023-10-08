<template>
  <div class="wrapper">
    <div class="info">
      <img src="src/assets/profile.jpeg" class="profile"/>
      <div class="links">
      <div class="social-links">
        <div class="social" @click="navigateToMail"> <p>M</p> </div>
        <div class="social" @click="navigateToGithub"> <p>G</p> </div>
        <div class="social" @click="navigateToX"> <p>X</p> </div>
      </div>
      <div class="resume" @click="downloadResume"> <p>Resume</p> </div>
    </div>
    </div>
    <div class="bio">
      <h2 class="title">About Me</h2>
      <p class="text">Born in Haiti, I’ve always loved figuring out how things worked. This put me at a crossroads with my parents as I would break down many of the gadgets/toys I was interested in around the house.
My parents moved to the United States in 2005, and in 2010 my little brother and I joined them in Connecticut.
I had my first exposure to a desktop computer then, my parents did not know how to set it up. So, I took it apart and then put it back together. And ever since, I knew that I wanted to be a computer scientist.
I started working on video games early on, I was the engineer, and my little brother was the artist. I then took an AP computer science class at my school; this reinforced my drive to dive deeper into computer science.
I graduated from Brigham Young University with a Bachelor of Science in computer science. I worked on many projects and even participated in computer vision research. I am grateful and learned much. I love computer science; however, I am deeply involved in machine learning, deep learning, systems engineering, mobile development, and software engineering.
I speak 5 languages, and I love working on cars.</p>
    </div>
  </div>
</template>

<script setup lang="ts">
function navigateToMail() {
  document.location = 'mailto:joeljordanjoseph@gmail.com'
}

function navigateToGithub() {
  window.location = 'https://github.com/NokoAnubis'
}

function navigateToX() {
  window.location = 'https://twitter.com/josephjoeljo'
}

function downloadResume() {
  window.open('src/assets/Resume.pdf')
}
</script>

<style scoped>
.wrapper {
  display: flex;
  flex-direction: row;
  margin: 5rem 0rem;
}
.info {
  display: flex;
  flex-direction: column;
  margin-left: 5rem;
  align-items: center;

  .profile {
    width: 25rem;
    height: 30rem;
    object-fit: cover;
  }
  
  .links {
    width: 90%;
    display: flex;
    flex-direction: column;
    justify-content: center;
  }

  .social-links {
    display: flex;
    flex-direction: row;
    margin-top: 3rem;
    justify-content: space-around;
  }

  .social {
    width: 5rem;
    height: 4rem;
    display: flex;
    cursor: grab;
    justify-content: center;
    align-items: center;
    justify-content: center;
    vertical-align: middle;
    border: 0.5px solid white;
  }

  .resume {
    width: 90%;
    margin-top: 2rem;
    height: 4rem;
    cursor: grab;
    align-self: center;
    display: flex;
    justify-content: center;
    align-items: center;
    border: 0.5px solid white;
  }
}

.bio {
  display: flex;
  flex-direction: column;
  margin-left: 5rem;
  .title {
    text-decoration: underline;
  }
  .text {
    width: 60%;
    margin-top: 2rem;
  }
}

@media (max-width: 1200px) {
  .bio {
    .text {
      width: 85%;
    }
  }
}

@media (max-width: 950px) {
  .wrapper {
    flex-direction: column;
    align-items: center;
  }
  .info {
    align-items: center;
    margin: 0;
  }
  .links {
    width: 20rem;
    display: flex;
    flex-direction: column;
    justify-content: center;
  }
  .social-links {
    display: flex;
    flex-direction: row;
    margin-top: 3rem;
    justify-content: space-around;
  }
  .social {
    width: 5rem;
    height: 4rem;
    display: flex;
    cursor: grab;
    justify-content: center;
    align-items: center;
    justify-content: center;
    vertical-align: middle;
    border: 0.5px solid white;
  }
  .resume {
    width: 90%;
    margin-top: 2rem;
    height: 4rem;
    cursor: grab;
    align-self: center;
    display: flex;
    justify-content: center;
    align-items: center;
    border: 0.5px solid white;
  }
  .bio {
    align-items: center;
    margin: 0;
    width: 80%;
    text-align: center;
  }
  .title {
    margin-top: 2rem;
  }
}
</style>
