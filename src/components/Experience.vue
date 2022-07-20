<template>
  <section class="resume-section p-3 p-lg-5" id="experience">
    <div class="row my-auto">
      <div class="col-12">
        <h2 class="text-center">Experience</h2>
        <div class="mb-5 heading-border"></div>
      </div>
      <div
        class="resume-item col-md-6 col-sm-12"
        v-for="(experience, index) in experiences"
        :key="index"
      >
        <div
          class="card mx-0 p-4 mb-5"
          style="
            border-color: #17a2b8;
            box-shadow: 2px 2px 2px rgba(0, 0, 0, 0.21);
          "
        >
          <div class="resume-content mr-auto">
            <h4 class="mb-3">
              <!-- <i class="fa fa-globe mr-3 text-info"></i> -->
              {{ experience.title }}
            </h4>
            <p v-html="experience.description"></p>
          </div>
          <div class="resume-date text-md-right">
            <span class="text-primary">{{ experience.period }}</span>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import experiences from "../data/experiences.json";

export default {
  name: "Experience",
  computed: {
    experiences() {
      return experiences;
    },
  },
};
</script>