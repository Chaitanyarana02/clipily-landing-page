<template>
  <div class="landing-page h-100">
    <section class="main-content">
      <div class="inner-container h-100">
        <header class="d-flex align-items-center">
          <img
            src="@/assets/logo-clipily.svg"
            alt="logo"
            class="logo mr-auto"
          />
          <button class="outline-btn mr-3">Sign in</button>
          <button class="primary-btn d-none d-md-block">Get Started</button>
        </header>
        <button class="primary-btn d-block d-md-none w-100 mt-5">
          Get Started
        </button>
        <img class="d-block d-md-none w-100 mt-5" src="@/assets/Group 88.png" />
        <div class="content text-center">
          <p class="heading">
            You <strong>Click.</strong> We <strong>Create.</strong>
          </p>
          <p class="sub-heading">
            Get all your graphic needs done with Clipily. <br />
            <strong class="font-weight-bold"
              >Pay by project - not per hour</strong
            >
          </p>
          <p class="sub-heading-two">
            Discover how we can transform your ideas into groundbreaking designs
            that <br />captivate your audience and propel your brand forward -
            <strong class="font-weight-bold">Always for a fixed price.</strong>
          </p>
          <div class="d-flex justify-content-center flex-sm-row flex-column">
            <div class="search-box"></div>
            <input
              type="text"
              name=""
              id=""
              placeholder="What do you need done?"
              class="mr-3"
            />
            <button class="coral-btn">Order Job</button>
          </div>
          <div
            class="d-flex tags-container align-items-center justify-content-center flex-column flex-md-row"
          >
            <span>Popular Searches:</span>
            <div class="d-flex align-items-center justify-content-center">
              <div class="tags">Web Design</div>
              <div class="tags">Social Media Design</div>
              <div class="tags">Logo design</div>
            </div>
          </div>
          <div class="box-parent">
            <div
              class="box-container d-flex align-items-center justify-content-center flex-wrap"
            >
              <div class="box">
                <img src="@/assets/Frame.svg" alt="" />
                <p>Fixed Prices starting at $49</p>
              </div>
              <div class="box">
                <img src="@/assets/Frame (1).svg" alt="" />
                <p>24 Hour Express Delivery</p>
              </div>
              <div class="box star">
                <img src="@/assets/Frame (2).svg" alt="" />
                <p>Unlimited Revisions</p>
              </div>
              <div class="box">
                <img src="@/assets/Frame (3).svg" alt="" />
                <p>Vetted specialists & 24/7 Support</p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
    <section class="trusted-business">
      <div class="inner-container">
        <p class="heading">Trusted by 10K+ Businesses Worldwide</p>
        <div
          class="company-images d-flex align-items-center justify-content-center flex-wrap"
        >
          <img src="@/assets/tiga.svg" alt="tiga" />
          <img src="@/assets/3m.svg" alt="3m" />
          <img src="@/assets/electro.svg" alt="electro" />
          <img src="@/assets/mercedes.svg" alt="mercedes" />
        </div>
        <div class="what-we-do">
          <p class="heading-common">What we do</p>
          <div class="d-block d-sm-none">
            <carousel
              :per-page="1"
              :pagination-enabled="true"
              paginationColor="#d3d3d3"
              paginationActiveColor="#ffa877"
            >
              <!-- Use v-for to loop through each slide -->
              <slide
                v-for="(slideBoxes, slideIndex) in slideData"
                :key="slideIndex"
              >
                <!-- Loop through and render the boxes for each slide -->
                <div
                  class="box-container d-flex align-items-start flex-column mb-0"
                >
                  <div
                    v-for="(box, boxIndex) in slideBoxes"
                    :key="boxIndex"
                    class="boxes d-flex align-items-start"
                  >
                    <img :src="require(`@/assets/${box.imageSrc}`)" alt="" />
                    <div class="w-100">
                      <p>{{ box.title }}</p>
                      <p>
                        <small class="vertical-middle">FROM </small>${{
                          box.price
                        }}
                      </p>
                    </div>
                  </div>
                </div>
              </slide>
            </carousel>
          </div>
          <div
            class="box-container align-items-center justify-content-center flex-wrap d-none d-sm-flex"
          >
            <div class="boxes d-flex align-items-start">
              <img src="@/assets/what-we-do/Rectangle 15-7.png" alt="" />
              <div class="w-100">
                <p>Logo Design</p>
                <p><small class="vertical-middle">FROM </small>$0.99</p>
              </div>
            </div>
            <div class="boxes d-flex align-items-start">
              <img src="@/assets/what-we-do/Rectangle 15.png" alt="" />
              <div class="w-100">
                <p>Brand Style Guides</p>
                <p><small class="vertical-middle">FROM </small>$0.99</p>
              </div>
            </div>
            <div class="boxes d-flex align-items-start">
              <img src="@/assets/what-we-do/Rectangle 15-8.png" alt="" />
              <div class="w-100">
                <p>Illustrations</p>
                <p><small class="vertical-middle">FROM </small>$0.99</p>
              </div>
            </div>
            <div class="boxes d-flex align-items-start">
              <img src="@/assets/what-we-do/Rectangle 15-6.png" alt="" />
              <div class="w-100">
                <p>Web Design</p>
                <p><small class="vertical-middle">FROM </small>$0.99</p>
              </div>
            </div>
            <div class="boxes d-flex align-items-start">
              <img src="@/assets/what-we-do/Rectangle 15-3.png" alt="" />
              <div class="w-100">
                <p>Print Design</p>
                <p><small class="vertical-middle">FROM </small>$0.99</p>
              </div>
            </div>
            <div class="boxes d-flex align-items-start">
              <img src="@/assets/what-we-do/Rectangle 15-1.png" alt="" />
              <div class="w-100">
                <p>Social Media Graphics</p>
                <p><small class="vertical-middle">FROM </small>$0.99</p>
              </div>
            </div>
            <div class="boxes d-flex align-items-start">
              <img src="@/assets/what-we-do/Rectangle 15-5.png" alt="" />
              <div class="w-100">
                <p>Packaging & Labels</p>
                <p><small class="vertical-middle">FROM </small>$0.99</p>
              </div>
            </div>
            <div class="boxes d-flex align-items-start">
              <img src="@/assets/what-we-do/Rectangle 15-4.png" alt="" />
              <div class="w-100">
                <p>Architecture & Landscape Design</p>
                <p><small class="vertical-middle">FROM </small>$0.99</p>
              </div>
            </div>
            <div class="boxes d-flex align-items-start">
              <img src="@/assets/what-we-do/Rectangle 15-2.png" alt="" />
              <div class="w-100">
                <p>Product & Character Design</p>
                <p><small class="vertical-middle">FROM </small>$0.99</p>
              </div>
            </div>
          </div>
          <div class="text-center">
            <button class="primary-btn dark mt-5 mt-sm-0">
              See Full List of Services
            </button>
          </div>
        </div>
        <div class="why-use">
          <p class="heading-common">Why use Clipily?</p>
          <div class="row align-items-center">
            <div class="col-sm-12 col-md-12 col-lg-6">
              <img
                src="@/assets/why-use.png"
                alt="why-use"
                class="w-100 h-100 mb-5 mb-md-0"
              />
            </div>
            <div class="col-sm-12 col-md-12 col-lg-6">
              <div class="content">
                <div class="points">
                  <p>Stick to your budget: Start your journey affordably.</p>
                  <p>
                    Find the right service for every price point. No hourly
                    rates, just project-based pricing.
                  </p>
                </div>
                <div class="points">
                  <p>Rapid Turnaround: 24-Hour Express Delivery</p>
                  <p>
                    In the fast-paced world of business, we deliver top-notch
                    designs right to your doorstep in just 24 hours.
                  </p>
                </div>
                <div class="points">
                  <p>Pay when you're happy: Unlimited Revisions</p>
                  <p>
                    We won't stop until your vision is realized perfectly -
                    enjoy unlimited revisions until you're 100% satisfied.
                  </p>
                </div>
                <div class="points">
                  <p>Expertise You Can Trust: Vetted Specialists</p>
                  <p>
                    Our vetted specialists have the expertise to translate your
                    ideas into captivating designs, ensuring quality with every
                    project.
                  </p>
                </div>
                <div class="points">
                  <p>Round-The-Clock Assistance: 24/7 Live Chat Support</p>
                  <p>
                    We're here for you anytime you need us - enjoy 24/7 live
                    chat support with our dedicated team.
                  </p>
                </div>
              </div>
            </div>
          </div>
        </div>
        <div class="teams">
          <div class="row align-items-center">
            <div class="col-sm-12 col-md-12 col-lg-6 order-1 order-md-0">
              <p class="main-heading">Teams Devoted, Dreams Delivered.</p>
              <p class="designation">Dedicated project manager</p>
              <p class="description">
                We blend state-of-the-art technology and a global team of expert
                creatives to deliver on-demand, high-quality work. Enjoy access
                to a dedicated project manager and a versatile creative team,
                encompassing branding, motion graphics, illustrations,
                presentations, UX, UI, 3D design, image editing, and more - all
                the expertise your business needs to thrive.
              </p>
            </div>
            <div class="col-sm-12 col-md-12 col-lg-6">
              <img src="@/assets/teams.png" alt="team" class="w-100 h-100" />
            </div>
          </div>
        </div>
        <div class="take-theirs">
          <p class="text-center main-heading">
            Don’t take our word for it. <br />
            <strong>Take theirs</strong>
          </p>
          <div class="row align-items-center">
            <div class="col-sm-12 col-md-12 col-lg-6">
              <img
                src="@/assets/service-2.png"
                alt="team"
                class="w-100 h-100"
              />
            </div>
            <div class="col-sm-12 col-md-12 col-lg-6">
              <p class="service">
                Clipily's services have proven to be not only efficient but also
                incredibly reliable. Their speed and precision are a hit among
                my team members - we simply love it!
              </p>
              <p class="name-title">
                <strong>Name, Credential</strong> <br />
                03 August, 2022
              </p>
            </div>
          </div>
          <div class="row align-items-center mt-cust">
            <div class="col-sm-12 col-md-12 col-lg-6 order-1 order-md-0">
              <p class="service">
                “Clipily's graphic design services have supercharged our firm's
                productivity, saving us heaps of time.”
              </p>
              <p class="name-title">
                <strong>Name, Credential</strong> <br />
                03 August, 2022
              </p>
            </div>
            <div class="col-sm-12 col-md-12 col-lg-6">
              <img
                src="@/assets/service-1.png"
                alt="team"
                class="w-100 h-100"
              />
            </div>
          </div>
        </div>
      </div>
    </section>
    <section class="schedule d-flex align-items-center justify-content-center">
      <img src="@/assets/flower.png" alt="flower" />
      <p>
        <strong> Curious but not convinced?</strong> <br />
        We’re here to help you with your <br />
        design needs.
      </p>
      <button class="coral-btn">Schedule A Call</button>
    </section>
    <section class="contact-us">
      <p class="heading-common">Contact Us</p>
      <div class="forms">
        <div class="row w-100 m-0">
          <div
            class="col-sm-12 col-md-12 col-lg-6 pl-0 pr-lg-2 pr-0 mb-4 mb-lg-0"
          >
            <input type="text" name="" id="" placeholder="Name" />
          </div>
          <div class="col-sm-12 col-md-12 col-lg-6 pr-0 pl-lg-2 pl-0">
            <input type="text" name="" id="" placeholder="Email" />
          </div>
        </div>
        <textarea name="" id="" placeholder="Message"></textarea>
      </div>
      <div class="text-center">
        <button class="primary-btn dark">Send</button>
      </div>
    </section>
    <footer>
      <div class="text-center light-bg">
        <p>
          The services you need. <br />
          The flexibility you want.
        </p>
        <button class="coral-btn">Schedule A Call</button>
      </div>
      <div class="last-footer">
        <div
          class="inner-container d-flex align-items-center justify-content-between"
        >
          <p>Privacy Policy</p>
          <p>© 2023 Clipily</p>
          <p>Do Not Sell My Data</p>
        </div>
      </div>
    </footer>
  </div>
</template>

<script>
import { Carousel, Slide } from "vue-carousel";
export default {
  name: "LandingPage",
  components: {
    Carousel,
    Slide,
  },
  props: {
    msg: String,
  },
  data() {
    return {
      slideData: [
        [
          {
            imageSrc: "what-we-do/Rectangle 15.png",
            title: "Brand Style Guides",
            price: 0.99,
          },
          {
            imageSrc: "what-we-do/Rectangle 15-8.png",
            title: "Illustrations",
            price: 0.99,
          },
          {
            imageSrc: "what-we-do/Rectangle 15-6.png",
            title: "Web Design",
            price: 0.99,
          },
        ],
        [
          {
            imageSrc: "what-we-do/Rectangle 15-3.png",
            title: "Print Design",
            price: 0.99,
          },
          {
            imageSrc: "what-we-do/Rectangle 15-1.png",
            title: "Social Media Graphics",
            price: 0.99,
          },
          {
            imageSrc: "what-we-do/Rectangle 15-5.png",
            title: "Packaging & Labels",
            price: 0.99,
          },
        ],
        [
          {
            imageSrc: "what-we-do/Rectangle 15-4.png",
            title: "Architecture & Landscape Design",
            price: 0.99,
          },
          {
            imageSrc: "what-we-do/Rectangle 15-2.png",
            title: "Product & Character Design",
            price: 0.99,
          },
          // Add more data objects as needed
        ],
      ],
    };
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
@import "./LandingPage.scss";
</style>
