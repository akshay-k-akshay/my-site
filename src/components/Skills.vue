<template>
  <section class="d-flex flex-column" id="skills">
    <div class="p-lg-5 p-3 skill-cover">
      <h3 class="text-center text-white">Coding Skills</h3>
      <div class="row text-center my-auto">
        <div
          class="col-md-3 col-sm-6"
          v-for="(skill, index) in skills"
          :key="index"
        >
          <div class="skill-item">
            <!-- <i :class="`${skill.icon} fa-5x`"></i> -->
            <img :src="`${skill.icon}`" :style="`width: ${skill.width}`" />
            <h2>
              <span class="counter"> {{ skill.percentage }}</span
              ><span>%</span>
            </h2>
            <p>{{ skill.title }}</p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import skills from "../data/skills.json";

export default {
  name: "Contact",
  computed: {
    skills() {
      return skills;
    },
  },
};
</script>