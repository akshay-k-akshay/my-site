<template>
  <section class="resume-section p-3 p-lg-5 d-flex d-column" id="about">
    <div class="my-auto">
      <h1 class="mb-0">
        {{ user.firstName }}
        <span class="text-primary">{{ user.lastName }}</span>
      </h1>
      <div class="subheading mb-5">
        FULL STACK DEVELOPER ( MEAN, MERN, MEVN )
      </div>
      <p class="mb-5" style="max-width: 500px">
        {{ user.description }}
      </p>
      <ul class="list-inline list-social-icons mb-0">
        <!-- <li class="list-inline-item">
          <a :href="`${user.facebook}`" target="_blank">
            <span class="fa-stack fa-lg">
              <i class="fa fa-circle fa-stack-2x"></i>
              <i class="fa fa-facebook fa-stack-1x fa-inverse"></i>
            </span>
          </a>
        </li> -->
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
      <div class="col-md-12 mt-5">
        <a
          download="Akshay_CV"
          style="text-decoration: none; color: black"
          href="/Akshay_Resume.pdf"
          class="btn btn-secondary"
          ><svg
            xmlns="http://www.w3.org/2000/svg"
            width="16"
            height="16"
            fill="currentColor"
            class="bi bi-download"
            viewBox="0 0 16 16"
          >
            <path
              d="M.5 9.9a.5.5 0 0 1 .5.5v2.5a1 1 0 0 0 1 1h12a1 1 0 0 0 1-1v-2.5a.5.5 0 0 1 1 0v2.5a2 2 0 0 1-2 2H2a2 2 0 0 1-2-2v-2.5a.5.5 0 0 1 .5-.5z"
            />
            <path
              d="M7.646 11.854a.5.5 0 0 0 .708 0l3-3a.5.5 0 0 0-.708-.708L8.5 10.293V1.5a.5.5 0 0 0-1 0v8.793L5.354 8.146a.5.5 0 1 0-.708.708l3 3z"
            />
          </svg>
          Download CV</a
        >
      </div>
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
        description: `I am a self taught developer ( MERN, MEVN, MEAN ) open to challenges. 
        I have seen the worst and best of things which strengthened me as a developer. 
        So I am capable of solving any problem that comes in my way. 
        I would like to play with code.`,
        // facebook: "https://facebook.com",
        linkedin: "https://www.linkedin.com/in/akshay--k/",
        github: "https://github.com/akshay-k-akshay",
      };
    },
  },
};
</script>