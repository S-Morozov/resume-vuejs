<script>
import navbar from "@/components/navbar.vue";
import Navbar from "@/components/navbar.vue";



export default {
  name: 'Resume',
  components: {Navbar},
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
  <navbar/>

  <div class="resume">
    <section class="header">
      <h1>{{ fullName }}</h1>
      <p>{{ title }}</p>
    </section>
    <section class="contact">
      <h2>Contact Information</h2>
      <ul>
        <li>Email: {{ email }}</li>
        <li>Phone: {{ phone }}</li>
        <li>Website: {{ website }}</li>
      </ul>
    </section>
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
  padding: 20px;
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
