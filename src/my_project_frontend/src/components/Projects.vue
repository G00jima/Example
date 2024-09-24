<template>
    <section class="projects">
      <h2>Projects</h2>
      <div class="project-list">
        <div class="project-card" v-for="project in projects" :key="project.title">
          <h3>{{ project.title }}</h3>
          <p>{{ project.description }}</p>
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
          { title: 'Gitara', description: 'Gram na gitarze.' },
          { title: 'Muzyka', description: 'Słucham dużo muzyki rock i metal.' },
          { title: 'Gram w gry', description: 'Gry takie jak: Dark Souls 1,2 i 3, Elden Ring, 7 Days to Die, Cała seria fallout, Cała seria Wolfenstein.' }
        ]
      };
    }
  }
  </script>

  <style scoped>
  .projects {
    padding: 35px 20px;
    background: #000000;
    color: #ff0000;
    max-width: 1200px;
    width: 100%;
    border-radius: 8px;
  }
  .projects h2 {
    margin-left: 25px;
  }
  .project-list {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-around;
  }
  .project-card {
    background: rgba(255, 255, 255, 0.1);
    border: 1px solid rgb(124, 0, 0);
    padding: 20px;
    margin: 10px;
    width: 300px;
    border-radius: 8px;
    transition: ease-in-out all 0.2s;
  }
  .project-card:hover {
    transform: translateY(-5px);
    border-color: #f39c12;
    transition: ease-in-out all 0.2s;
  }
  </style>