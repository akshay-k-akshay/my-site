<template>
  <section class="resume-section p-3 p-lg-5 d-flex flex-column">
    <div class="row my-auto" id="contact">
      <div class="col-md-8">
        <div class="contact-cont">
          <h3>CONTACT</h3>
          <div class="heading-border-light"></div>
          <p>
            It is a long established fact that a reader will be distracted by
            the readable content of a page when looking at its layout. The point
            of using Lorem Ipsum is that it has a more-or-less normal
            distribution of letters, as opposed to using Content here.
          </p>
        </div>
        <div class="row con-form">
          <div class="col-md-12">
            <input
              type="text"
              name="full-name"
              placeholder="Full Name"
              class="form-control"
            />
          </div>
          <div class="col-md-12">
            <input
              type="text"
              name="email"
              placeholder="Email Id"
              class="form-control"
            />
          </div>
          <div class="col-md-12">
            <input
              type="text"
              name="subject"
              placeholder="Subject"
              class="form-control"
            />
          </div>
          <div class="col-md-12"><textarea name="" id=""></textarea></div>
          <div class="col-md-12 sub-but">
            <button class="btn btn-general btn-white" role="button">
              Send
            </button>
          </div>
        </div>
      </div>
      <div class="col-md-4 col-sm-12 mt-5">
        <div class="contact-cont2">
          <div class="contact-add contact-box-desc">
            <h3><i class="fa fa-map-marker cl-atlantis fa-2x"></i> Address</h3>
            <p>
              Kailas Palukachippara <br />
              Kanhileri(po) Mattannur<br />
              Kannur kerala
            </p>
          </div>
          <div class="contact-phone contact-side-desc contact-box-desc">
            <h3><i class="fa fa-phone cl-atlantis fa-2x"></i> Phone</h3>
            <p>
              <a href="tel:+919567520687">+91 9567520687</a> <br />
              <a href="tel:+919400358030">+91 9400358030</a>
            </p>
          </div>
          <div class="contact-mail contact-side-desc contact-box-desc">
            <h3><i class="fa fa-envelope-o cl-atlantis fa-2x"></i> Email</h3>
            <address class="address-details-f">
              Email:
              <a href="mailto:akshayk.info01@gmail.com" class=""
                >akshayk.info01@gmail.com</a
              >
            </address>
            <!-- <ul class="list-inline social-icon-f top-data">
              <li>
                <a href="#" target="_blank"
                  ><i
                    class="fa top-social fa-facebook"
                    style="color: #4267b2; border-color: #4267b2"
                  ></i
                ></a>
              </li>
              <li>
                <a href="#" target="_blank"
                  ><i
                    class="fa top-social fa-twitter"
                    style="color: #4ab3f4; border-color: #4ab3f4"
                  ></i
                ></a>
              </li>
              <li>
                <a href="#" target="_blank"
                  ><i
                    class="fa top-social fa-google-plus"
                    style="color: #e24343; border-color: #e24343"
                  ></i
                ></a>
              </li>
            </ul> -->
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "Contact",
};
</script>