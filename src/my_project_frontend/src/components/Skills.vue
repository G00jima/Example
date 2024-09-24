<template>
    <section class="skills">
      <h2>Skills</h2>
      <div class="skill-list">
        <div class="skill" v-for="skill in skills" :key="skill">
          {{ skill }}
        </div>
      </div>
    </section>
  </template>
  
  <script>
  export default {
    name: "Skills",
    data() {
      return {
        skills: [
          "HTML",
          "CSS",
          "JavaScript",
          "Typescript",
          "Astro.js",
          "Vue.js",
          "Nuxt.js",
          "React",
          "Next",
        ],
      };
    },
  };
  </script>
  
  <style scoped>
  .skills {
    padding: 60px 20px;
    background: linear-gradient(to right, #ff0000, #ff0000);
    color: #000000;
    text-align: center;
    max-width: 1200px;
    width: 100%;
    border-radius: 8px;
  }
  .skill-list {
    display: flex;
    justify-content: center;
    flex-wrap: wrap;
  }
  .skill {
    background: #00000022;
    border: 1px solid #000000;
    padding: 10px 20px;
    margin: 10px;
    border-radius: 8px;
  }
  </style>