<script>



export default {
  name: 'Resume',
  data() {
    return {
      fullName: 'Semen Morozov',
      title: 'Front-end developer',
      email: 'you@example.com',
      phone: '123-456-7890',
      website: 'https://www.yourwebsite.com',
      experience: [
        {
          id: 1,
          position: 'Frontend Developer',
          company: 'ABC Inc.',
          duration: 'June 2020 - Present',
          tasks: ['Developed and maintained web applications', 'Implemented responsive designs']
        },
        // Add more job experiences here
      ],
      education: [
        {
          id: 1,
          degree: 'Bachelor of Science in Computer Science',
          school: 'XYZ University',
          graduationYear: 'May 2019'
        },
        // Add more education details here
      ],
      skills: ['Vue.js', 'JavaScript', 'HTML', 'CSS', 'Responsive Design', 'Git']
    };
  }
};
</script>

<template>
  <div class="resume">
    <div class = "left-side">
      <div>
        <img class = "profile-img" src="./assets/IMG_1962-removebg-preview.png"/>
      </div>
      <section class="header">
        <h1>{{ fullName }}</h1>
        <p>{{ title }}</p>
      </section>

    <section class="title-info">
      <p>Hello! It's my resume based on Vue.Js</p>
    </section>

      <div class="line"></div>

      <section class="contact">

        <ul>
          <li> <img class="icon-env" src="../src/components/icons/envelope-icon.png">Email: {{ email }}</li>
          <li>Phone: {{ phone }}</li>
          <li>Website: {{ website }}</li>
        </ul>

      </section>
    </div>





    <section class="experience">
      <h2>Work Experience</h2>
      <ul>
        <li v-for="job in experience" :key="job.id">
          <h3>{{ job.position }}</h3>
          <p>{{ job.company }}</p>
          <p>{{ job.duration }}</p>
          <ul>
            <li v-for="task in job.tasks" :key="task">{{ task }}</li>
          </ul>
        </li>
      </ul>
    </section>
    <section class="education">
      <h2>Education</h2>
      <ul>
        <li v-for="edu in education" :key="edu.id">
          <h3>{{ edu.degree }}</h3>
          <p>{{ edu.school }}</p>
          <p>{{ edu.graduationYear }}</p>
        </li>
      </ul>
    </section>
    <section class="skills">
      <h2>Skills</h2>
      <ul>
        <li v-for="skill in skills" :key="skill">{{ skill }}</li>
      </ul>
    </section>



  </div>
</template>



<style scoped>

.resume {
  background: linear-gradient(180deg, #1A173F 0%, rgba(156, 88, 104, 0.92) 47.19%, rgba(15, 33, 124, 0.89) 100%);
  box-shadow: 0 9px 50px 0 rgba(112, 112, 112, 0.20);

}

.header h1 {
  color: rgba(183, 175, 205, 0.41);
  font-family: Open Sans,serif;
  font-size: 20px;
  font-style: normal;
  font-weight: 600;
  line-height: 27px; /* 135% */
  overflow: hidden;
}

.header p {
  color: #72C5D8;
  text-shadow: 4px 4px 4px rgba(0, 0, 0, 0.30);
  font-family: PT Serif Caption,sans-serif;
  font-size: 20px;
  font-style: normal;
  font-weight: 400;
  line-height: normal;
}

.left-side {
  width: 250px;
  height: 842px;
  flex-shrink: 0;
  background: linear-gradient(90deg, rgba(158, 223, 243, 0.00) 0%, rgba(141, 180, 192, 0.27) 100%);
  backdrop-filter: blur(5px);
}

.profile-img{
  margin: 30px;
  width: 180px;
  height: 220px;
  flex-shrink: 0;
}

.title-info {

  margin: 21px 19px 16px 37px;
  width: 135px;
  color: #DEE0DE;
  font-family: Public Sans,sans-serif;
  font-size: 12px;
  font-style: normal;
  font-weight: 500;
  line-height: 20px; /* 166.667% */
  text-align: center;
}

.line {
  width: 147px;
  height: 1px;
  margin-left: 27px;
  margin-right: 16px;
  background: rgba(221, 226, 237, 0.20);
}

.icon-env {
  width: 36px;
  height: 26px;
  flex-shrink: 0;
}

.navbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  background-color: #333;
  color: #fff;
  padding: 10px 20px;
}

.nav-left {
  font-size: 24px;
}

.nav-right {
  display: flex;
  gap: 20px;
}

.nav-right a {
  color: #fff;
  text-decoration: none;
  font-size: 16px;
}

.header {
  color: #fff;
  text-align: center;
}

.header h1 {
  font-size: 32px;
  margin-bottom: 10px;
}

.header p {
  font-size: 18px;
  margin-bottom: 0;
}









.logo {
  display: block;
  margin: 0 auto 2rem;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style>
