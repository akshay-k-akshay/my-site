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
import projects from "../data/projects.json";
export default {
  name: "Portfolio",
  components: {
    Modal,
    ImageSlider,
  },
  computed: {
    projects() {
      return projects;
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