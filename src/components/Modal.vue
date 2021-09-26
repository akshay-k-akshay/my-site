<template>
  <div
    class="portfolio-modal modal fade"
    :id="id"
    tabindex="-1"
    role="dialog"
    aria-hidden="true"
  >
    <div class="modal-dialog" role="document">
      <div class="modal-content">
        <div class="close-modal" data-dismiss="modal">
          <div class="lr">
            <div class="rl"></div>
          </div>
        </div>
        <div class="container">
          <div class="row">
            <div class="modal-body">
              <div class="title-bar">
                <div class="col-md-12">
                  <h2 class="text-center">{{ title }}</h2>
                  <div class="heading-border"></div>
                </div>
              </div>
              <div class="row">
                <div class="col-md-6">
                  <ImageSlider :images="images" customStyle="img-centered" />
                </div>
                <div class="col-md-6">
                  <p v-html="description"></p>
                  <ul class="list-inline item-details">
                    <li>
                      <strong v-if="link">
                        <a :href="`${link}`" target="_blank">Source Code</a>
                      </strong>
                    </li>
                    <!--    <li>
                      Date:
                      <strong>
                        <a href="#">April 2018</a>
                      </strong>
                    </li>
                    <li>
                      Service:
                      <strong>
                        <a href="#">Web Development</a>
                      </strong>
                    </li> -->
                  </ul>
                </div>
              </div>
            </div>
          </div>
        </div>
        <div class="col-md-12 mb-0">
          <button
            class="modal-close-btn btn btn-general btn-white float-right"
            type="button"
            data-dismiss="modal"
          >
            <i class="fa fa-times"></i> Close
          </button>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import ImageSlider from "./ImageSlider.vue";
export default {
  name: "Modal",
  components: {
    ImageSlider,
  },
  props: ["id", "title", "images", "description", "link"],
};
</script>