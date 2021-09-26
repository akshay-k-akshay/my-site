<template>
  <section class="resume-section p-3 p-lg-5 d-flex flex-column" id="portfolio">
    <div class="row my-auto">
      <div class="col-12">
        <h2 class="text-center">Portfolio</h2>
        <div class="mb-5 heading-border"></div>
      </div>
    </div>
    <div class="row my-auto">
      <div
        class="col-sm-4 portfolio-item"
        v-for="project in projects"
        :key="project.id"
      >
        <a
          class="portfolio-link"
          v-on:click="openModal(project)"
          :href="`#${project.id}`"
          data-toggle="modal"
        >
          <div class="caption-port">
            <div class="caption-port-content">
              <i class="fa fa-search-plus fa-3x"></i>
            </div>
          </div>
          <ImageSlider :images="project.images" />
        </a>
      </div>
    </div>
  </section>
  <Modal
    :id="id"
    :description="description"
    :title="title"
    :images="images"
    :link="link"
  />
</template>

<script>
import Modal from "./Modal.vue";
import ImageSlider from "./ImageSlider.vue";
export default {
  name: "Portfolio",
  components: {
    Modal,
    ImageSlider,
  },
  computed: {
    projects() {
      return [
        {
          id: "1",
          title: "SHOPPING CART",
          description: `
          Simple shopping cart with React js. 
          Automatic deployment and test like formatting and lint is implemented using Github Actions<br /><br />
          <span>Technology used</span><br />
          <ul>
          <li>React js </li>
          <li>Firebase
           <ul>
          <li>Storage</li>
          <li>Hosting </li>
          <li>Authentication </li>
          <li>Firestore ( Firebase Database )</li>
          </ul>
          </li>
          <li>Github Actions </li>
          </ul>`,
          images: [
            "/img/portfolio/1/1.png",
            "/img/portfolio/1/2.png",
            "/img/portfolio/1/3.png",
            "/img/portfolio/1/4.png",
          ],
          link: "https://github.com/akshay-k-akshay/supermarket",
        },
        {
          id: "2",
          title: "Test Project 2",
          description: `Our new Project every processes had become fragmented;
                    meaning quality and service were inconsistent. This lack of
                    standardization was adversely impacting operating costs,
                    productivity and customer satisfaction. For several years
                    now Payfast has worked strategically with innovations as a
                    means of developing new solutions, products and services. In
                    line with this vision, Success was approached to find new
                    payments solutions to offer Payfast customers on their
                    website, including open invoice and partial payments
                    options.`,
          images: ["img/portfolio/p-2.jpg"],
          link: "#",
        },
        {
          id: "3",
          title: "Test Project 3",
          description: `Our new Project every processes had become fragmented;
                    meaning quality and service were inconsistent. This lack of
                    standardization was adversely impacting operating costs,
                    productivity and customer satisfaction. For several years
                    now Payfast has worked strategically with innovations as a
                    means of developing new solutions, products and services. In
                    line with this vision, Success was approached to find new
                    payments solutions to offer Payfast customers on their
                    website, including open invoice and partial payments
                    options.`,
          images: ["img/portfolio/p-3.jpg"],
          link: "#",
        },
      ];
    },
  },
  data() {
    return {
      id: null,
      title: null,
      images: null,
      description: null,
      link: null,
    };
  },
  methods: {
    openModal(project) {
      this.id = project.id;
      this.title = project.title;
      this.images = project.images;
      this.description = project.description;
      this.link = project.link;
    },
  },
};
</script>