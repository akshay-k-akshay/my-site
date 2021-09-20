<template>
  <section class="resume-section p-3 p-lg-5 d-flex flex-column" id="portfolio">
    <div class="row my-auto">
      <div class="col-12">
        <h2 class="text-center">Portfolio</h2>
        <div class="mb-5 heading-border"></div>
      </div>
      <!-- <div class="col-md-12">
        <div class="port-head-cont">
          <button class="btn btn-general btn-green filter-b" data-filter="all">
            All
          </button>
          <button
            class="btn btn-general btn-green filter-b"
            data-filter="consulting"
          >
            Web Design
          </button>
          <button
            class="btn btn-general btn-green filter-b"
            data-filter="finance"
          >
            Mobile Apps
          </button>
          <button
            class="btn btn-general btn-green filter-b"
            data-filter="marketing"
          >
            Graphics Design
          </button>
        </div>
      </div> -->
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
          <img class="img-fluid" :src="`${project.image}`" alt="" />
        </a>
      </div>
    </div>
  </section>
  <Modal
    :id="id"
    :description="description"
    :title="title"
    :image="image"
    :link="link"
  />
</template>

<script>
import Modal from "./Modal.vue";
export default {
  name: "Portfolio",
  components: {
    Modal,
  },
  computed: {
    projects() {
      return [
        {
          id: "1",
          title: "Test Project 1",
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
          image: "img/portfolio/p-1.jpg",
          link: "#",
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
          image: "img/portfolio/p-2.jpg",
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
          image: "img/portfolio/p-3.jpg",
          link: "#",
        },
        {
          id: "4",
          title: "Test Project 4",
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
          image: "img/portfolio/p-4.jpg",
          link: "#",
        },
        {
          id: "5",
          title: "Test Project 5",
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
          image: "img/portfolio/p-5.jpg",
          link: "#",
        },
        {
          id: "6",
          title: "Test Project 6",
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
          image: "img/portfolio/p-6.jpg",
          link: "#",
        },
      ];
    },
  },
  data() {
    return {
      id: null,
      title: null,
      image: null,
      description: null,
      link: null,
    };
  },
  methods: {
    openModal(project) {
      this.id = project.id;
      this.title = project.title;
      this.image = project.image;
      this.description = project.description;
      this.link = project.link;
    },
  },
};
</script>