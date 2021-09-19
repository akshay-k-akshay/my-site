<template>
  <section class="resume-section p-3 p-lg-5 d-flex flex-column" id="awards">
    <div class="row my-auto">
      <div class="col-12">
        <h2 class="text-center">Awards</h2>
        <div class="mb-5 heading-border"></div>
      </div>
      <div class="main-award" id="award-box">
        <div class="award" v-for="(award, index) in awards" :key="index">
          <div class="award-icon"></div>
          <div class="award-content">
            <span class="date">{{ award.date }}</span>
            <h5 class="title">{{ award.title }}</h5>
            <p class="description">
              {{ award.description }}
            </p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "Awards",
  computed: {
    awards() {
      return [
        {
          date: "Apr 2017 - Mar 2018",
          title: "Google Analytics Certified Developer",
          description: ` Lorem ipsum dolor sit amet, consectetur adipiscing elit.
              Vestibulum mattis felis vitae risus pulvinar tincidunt. Nam ac
              venenatis enim. Aenean hendrerit justo sed.`,
        },
        {
          date: "Apr 2018 - Mar 2019",
          title: "Mobile Web Specialist - Google Certification",
          description: ` Lorem ipsum dolor sit amet, consectetur adipiscing elit.
              Vestibulum mattis felis vitae risus pulvinar tincidunt. Nam ac
              venenatis enim. Aenean hendrerit justo sed.`,
        },
      ];
    },
  },
};
</script>