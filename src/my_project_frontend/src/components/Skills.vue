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
        "C++",
        "JAVA",
        "Blender 3D"
      ],
    };
  },
};
</script>

<style scoped>
.skills {
  padding: 60px 20px;
  background-image: linear-gradient(301deg, rgba(104, 255, 42, 1) 0%, rgba(18, 18, 18, 1) 95%);
  color: #ffffff;
  font-size: 17px;
  text-align: center;
  max-width: 60%;
  width: 100%;
  border-radius: 8px;
}
.skill-list {
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
}
.skill {
  background: #ffffff22;
  border: 3px solid #a3cfff;
  padding: 10px 20px;
  margin: 10px;
  border-radius: 8px;
}
</style>