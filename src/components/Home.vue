<template>
  <Navbar />

  <div class="container-fluid p-0">
    <About />
    <Experience />
    <Portfolio />
    <Skills />
    <Awards />
    <Contact />
  </div>
  <Modal />
</template>

<script>
import Navbar from "./Navbar.vue";
import About from "./About.vue";
import Experience from "./Experience.vue";
import Portfolio from "./Portfolio.vue";
import Skills from "./Skills.vue";
import Awards from "./Awards.vue";
import Contact from "./Contact.vue";
import Modal from "./Modal.vue";
export default {
  name: "Home",
  components: {
    Navbar,
    About,
    Experience,
    Portfolio,
    Skills,
    Awards,
    Contact,
    Modal,
  },
};
</script>