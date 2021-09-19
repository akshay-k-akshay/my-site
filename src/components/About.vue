<template>
  <section class="resume-section p-3 p-lg-5 d-flex d-column" id="about">
    <div class="my-auto">
      <h1 class="mb-0">
        {{ user.firstName }}
        <span class="text-primary">{{ user.lastName }}</span>
      </h1>
      <div class="subheading mb-5">WEB DEVELOPER</div>
      <p class="mb-5" style="max-width: 500px">
        {{ user.description }}
      </p>
      <ul class="list-inline list-social-icons mb-0">
        <li class="list-inline-item">
          <a :href="`${user.facebook}`" target="_blank">
            <span class="fa-stack fa-lg">
              <i class="fa fa-circle fa-stack-2x"></i>
              <i class="fa fa-facebook fa-stack-1x fa-inverse"></i>
            </span>
          </a>
        </li>
        <li class="list-inline-item">
          <a :href="`${user.linkedin}`" target="_blank">
            <span class="fa-stack fa-lg">
              <i class="fa fa-circle fa-stack-2x"></i>
              <i class="fa fa-linkedin fa-stack-1x fa-inverse"></i>
            </span>
          </a>
        </li>
        <li class="list-inline-item">
          <a :href="`${user.github}`" target="_blank">
            <span class="fa-stack fa-lg">
              <i class="fa fa-circle fa-stack-2x"></i>
              <i class="fa fa-github fa-stack-1x fa-inverse"></i>
            </span>
          </a>
        </li>
      </ul>
    </div>
  </section>
</template>

<script>
export default {
  name: "About",
  computed: {
    user() {
      return {
        firstName: "AKSHAY",
        lastName: "K",
        description: `I am experienced in leveraging agile frameworks to provide a robust
        synopsis for high level overviews. Iterative approaches to corporate
        strategy foster collaborative thinking to further the overall value
        proposition.`,
        facebook: "https://facebook.com",
        linkedin: "https://linkedin.com",
        github: "https://github.com",
      };
    },
  },
};
</script>