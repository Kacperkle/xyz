<template>
    <section class="projects">
      <div class="border">
        <h2>Projects</h2>
        <div class="project-list">
          <div class="project-card" v-for="project in projects" :key="project.title" @click="goToProject(project.route)">
            <h3>{{ project.title }}</h3>
            <p>{{ project.description }}</p>
          </div>
        </div>
      </div>
    </section>
  </template>

  <script>
  export default {
    name: 'Projects',
    data() {
      return {
        projects: [
          { title: 'Project One', description: 'Description of project one.', route: '/Blender' },
          { title: 'Project Two', description: 'Description of project two.', route: '/C++' },
          { title: 'Project Three', description: 'Description of project three.', route: '/Html' },
          { title: 'Project Three', description: 'Description of project three.', route: '/Java' }
        ]
      };
    },
    methods: {
      goToProject(route) {
        this.$router.push(route);
      }
    }
  }
  </script>

  <style scoped>
  .projects {
    padding: 10px 10px;
    background: #1c1c1e;
    color: #ffffff;
    max-width: 60%;
    width: 100%;
    border-radius: 8px;
  }
  .border h2 {
    margin-left: 25px;
  }
  .project-list {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-around;
  }
  .project-card {
    background: rgba(255, 255, 255, 0.1);
    border: 1px solid #A3CFFF;
    padding: 20px;
    margin: 10px;
    width: 300px;
    border-radius: 8px;
    transition: ease-in-out all 0.2s;
  }
  .project-card:hover {
    transform: translateY(-5px);
    border-color: rgba(104, 255, 42, 1);
    transition: ease-in-out all 0.2s;
  }
  .border{
    padding: 35px 20px;
    border: solid  rgba(104, 255, 42, 1) 5px;
    border-radius: 10px;
  }
  </style>