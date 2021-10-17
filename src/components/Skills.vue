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
export default {
  name: "Contact",
  computed: {
    skills() {
      return [
        {
          title: "Node JS",
          percentage: 85,
          icon: "https://img.icons8.com/color/48/000000/nodejs.png",
          width: "5em",
        },
        // {
        //   title: "Javascript",
        //   percentage: 80,
        //   icon: "https://img.icons8.com/color/48/000000/javascript--v1.png",
        //   width: "5em",
        // },
        {
          title: "Typescript",
          percentage: 80,
          icon: "https://cdn.changelog.com/uploads/icons/topics/YXL/icon_large.png?v=63682389432",
          width: "5em",
        },
        {
          title: "Mongo DB",
          percentage: 85,
          icon: "https://img.icons8.com/color/50/000000/mongodb.png",
          width: "5em",
        },
        {
          title: "Dynamo DB",
          percentage: 75,
          icon: "/img/skills/dynamoDb.png",
          width: "4.4em",
        },
        {
          title: "HTML",
          percentage: 95,
          icon: "https://img.icons8.com/color/48/000000/html-5--v1.png",
          width: "5em",
        },
        {
          title: "Vue JS",
          percentage: 80,
          icon: "https://img.icons8.com/color/48/000000/vue-js.png",
          width: "5em",
        },
        {
          title: "React JS",
          percentage: 75,
          icon: "/img/skills/react.png",
          width: "9em",
        },
        {
          title: "Angular",
          percentage: 70,
          icon: "https://img.icons8.com/color/48/000000/angularjs.png",
          width: "5em",
        },
        {
          title: "GIT",
          percentage: 75,
          icon: "https://git-scm.com/images/logos/downloads/Git-Logo-2Color.png",
          width: "10em",
        },
        {
          title: "Firebase",
          percentage: 70,
          icon: "https://img.icons8.com/color/48/000000/firebase.png",
          width: "4em",
        },
      ];
    },
  },
};
</script>