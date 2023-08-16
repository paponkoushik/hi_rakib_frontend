<template>
  <div>
    <div class="bg-black2">
      <div class="container d-flex align-items-center header" id="header">
        <h1 class="site-title"><span>hirakib</span>.me</h1>
        <nav class="navi-bar d-md-block">
          <ul class="navi-list">
            <li><a class="navi-link active-menu" href="#">Home</a></li>
            <li><a class="navi-link" href="#case-study">Case study</a></li>
            <li><a class="navi-link" href="#process">Working process</a></li>
            <li><a class="navi-link" href="#blogs">Blogs</a></li>
          </ul>
        </nav>
        <button class="ms-auto btn-primary-rounded d-none d-lg-block"
                onclick="window.location.href=window.location.pathname+'#contact'">Get in touch
        </button>
        <div class="ms-auto mb-menu d-md-none" id="menu">
          <img class="menu-icon" src="../layouts/assets/menu-icon.svg">
          <img class="menu-close" src="../layouts/assets/menu-close.svg">
        </div>
      </div>
    </div>
    <div class="container">
      <div class="row hs-padding">
        <div class="col-md-4 col-lg-3 imgg">
          <img src="../layouts/assets/rakib.png" class="w-100" alt="Rakibul islam">
        </div>
        <div class="col-md-8 col-lg-9 mt-3 mt-md-0">
          <h2 class="hs-name">
            Hey I'm Rakibul islam
          </h2>
          <h1 class="text-gradient1 hs-heading d-md-none">UX Designer</h1>
          <vue-typed-js
            :strings="['User Experience Designer', 'Product Designer', 'User interface Designer']"
            :loop="true"
            :typeSpeed="100"
            :backSpeed="80"
            :smartBackspace="true"
            :cursorChar="''"
          >
            <h1 class="typing text-gradient1 hs-heading d-none d-md-block"></h1>
            <!-- f-heading d-none d-lg-block -->
          </vue-typed-js>
          <!-- <div class=""> -->
          <p class="hs-paragraph">Helping startups and enterprise businesses by producing
            design solutions. designing software, websites, web apps, mobile apps, and SAAS
            products. Specilize in usable, engaging, beautiful products with amazing accessibility and efficiency.
          </p>
          <!-- </div> -->
          <div class="mt-4 d-md-block">
            <button class="btn-primary-rounded"
                    onclick="window.location.href=window.location.pathname+'#contact'">Get in touch</button>
            <button class="btn-primary-rounded-outline ms-3">Download CV</button>
          </div>
        </div>
      </div>
    </div>

    <div class="container" id="case-study">
      <div class="cs-container">
        <h1 class="section-title">
          Case Study
        </h1>
        <template v-for="(caseStudy, index) in caseStudies">
          <div class="cs-card">
            <div class="cs-thumb-container">
              <img class="cs-thumb" :src="getImage(caseStudy.thumbnail)" />
              <img class="cs-arrow" src="../layouts/assets/right-arrow.svg">
            </div>
          </div>
          <h2 class="cs-title">{{caseStudy.title}}</h2>
          <p class="cs-paragraph">{{caseStudy.description}}</p>
          <nuxt-link class="cs-link" :to="`${'/case/'+caseStudy.id}`" target="_blank">View <span class="d-md-none">case study</span></nuxt-link>
        </template>
      </div>
    </div>

    <div class="container" id="process">
      <h1 class="section-title">My design process</h1>
      <p class="section-details">I follow to a set of processes that enable me to assure both user-friendly design
        and business success.
        My
        typical method is outlined here, however it may vary depending on the needs of the project.</p>

      <div class="timeline">
        <div class="diagram">
          <img class="ite ite1" src="../layouts/assets/process/ite1.svg">
          <img class="ite ite2" src="../layouts/assets/process/ite2.svg">
          <img class="ite ite3" src="../layouts/assets/process/ite3.svg">
          <img class="ite ite4" src="../layouts/assets/process/ite4.svg">
          <img class="ite ite5" src="../layouts/assets/process/ite5.svg">
          <img class="ite ite6" src="../layouts/assets/process/ite6.svg">

          <div class="step-container">
            <img class="step" src="../layouts/assets/process/s1.svg">
            <div class="step-text step-right">
              <h4 class="step-title">Empathise</h4>
              <p>In first stage, I get clear about who actual user is, what they want, and which
                challenges
                and problems they facing. In addition business goals, and technical obstacles.</p>
            </div>
          </div>

          <img class="step-arrow" src="../layouts/assets/process/step-arrow.svg">

          <div class="step-container">
            <img class="step" src="../layouts/assets/process/s2.svg">
            <div class="step-text step-left">
              <h4 class="step-title">Define actual problem</h4>
              <p>Using previous research findings and business requirements, I identify the actual
                problems. It is important to define the actual problem before starting to design a
                solution.</p>
            </div>
          </div>

          <img class="step-arrow" src="../layouts/assets/process/step-arrow.svg">

          <div class="step-container">
            <img class="step" src="../layouts/assets/process/s3.svg">
            <div class="step-text step-right">
              <h4 class="step-title">Design to produce solutions</h4>
              <p>Once the problems is identified the I jump into make multiple solutions to achieve goals.
                Sometimes its lo-fi wireframe sometimes mid or high-fi wireframe. </p>
            </div>
          </div>

          <img class="step-arrow" src="../layouts/assets/process/step-arrow.svg">

          <div class="step-container">
            <img class="step" src="../layouts/assets/process/s4.svg">
            <div class="step-text step-left">
              <h4 class="step-title">Prototype</h4>
              <p>A prototype is a working model of a product or system that is used to test and refine the
                design. create a prototype to show stakeholders how it will work in real time.</p>
            </div>
          </div>

          <img class="step-arrow" src="../layouts/assets/process/step-arrow.svg">

          <div class="step-container">
            <img class="step" src="../layouts/assets/process/s5.svg">
            <div class="step-text step-right">
              <h4 class="step-title">Test against requirements</h4>
              <p>I test the design to ensure that it meets the needs of the end users as well as the
                business requirements.</p>
            </div>
          </div>
        </div>
      </div>
      <p class="process-summary">It’s a non-linear iterative process until all is right. So I go back-and-forth
        between the different steps till I'm satisfied.</p>
    </div>

    <div class="bg-black2">
      <div class="container">
        <div class="tm-container">
          <div class="tm-card">
            <h1 class="section-title">Testimonials</h1>
            <p class="fw-3">Here are some statements from previous clients and colleagues. You can see what
              kind
              of
              service I offer.</p>
          </div>
          <div class="tm-card">
            <img class="tm-logo" src="../layouts/assets/tm-logo.png">
            <p class="tm-comment">Rakib is a amazing UX designer with a keen eye for detail. He is always
              willing
              to go the extra mile to ensure that his designs are user-friendly and effective. I would
              highly
              recommend him to anyone looking for a top-notch UX designer.</p>
            <div class="d-flex align-items-center">
              <img class="tm-photo" src="../layouts/assets/tm-photo.png">
              <h3 class="tm-name">Andress Tan</h3>
              <h4 class="tm-position">CEO, Tanpool Inc.</h4>
            </div>
          </div>
          <div class="tm-card">
            <img class="tm-logo" src="../layouts/assets/tm-logo.png">
            <p class="tm-comment">Rakib is a amazing UX designer with a keen eye for detail. He is always
              willing
              to go the extra mile to ensure that his designs are user-friendly and effective. I would
              highly
              recommend him to anyone looking for a top-notch UX designer.</p>
            <div class="horizontal-center">
              <img class="tm-photo" src="../layouts/assets/tm-photo.png">
              <h3 class="tm-name">Andress Tan</h3>
              <h4 class="tm-position">CEO, Tanpool Inc.</h4>
            </div>
          </div>
          <div class="tm-card">
            <img class="tm-logo" src="../layouts/assets/tm-logo.png">
            <p class="tm-comment">Rakib is a amazing UX designer with a keen eye for detail. He is always
              willing
              to go the extra mile to ensure that his designs are user-friendly and effective. I would
              highly
              recommend him to anyone looking for a top-notch UX designer.</p>
            <div class="horizontal-center">
              <img class="tm-photo" src="../layouts/assets/tm-photo.png">
              <h3 class="tm-name">Andress Tan</h3>
              <h4 class="tm-position">CEO, Tanpool Inc.</h4>
            </div>
          </div>
          <div class="tm-card">
            <img class="tm-logo" src="../layouts/assets/tm-logo.png">
            <p class="tm-comment">Rakib is a amazing UX designer with a keen eye for detail. He is always
              willing
              to go the extra mile to ensure that his designs are user-friendly and effective. I would
              highly
              recommend him to anyone looking for a top-notch UX designer.</p>
            <div class="horizontal-center">
              <img class="tm-photo" src="../layouts/assets/tm-photo.png">
              <h3 class="tm-name">Andress Tan</h3>
              <h4 class="tm-position">CEO, Tanpool Inc.</h4>
            </div>
          </div>
        </div>
      </div>
    </div>

    <div class="container" id="blogs">
      <h1 class="section-title">Blogs</h1>
      <div class="blog-container row row-cols-1 row-cols-sm-2 row-cols-md-3 row-cols-lg-4 g-4">
        <template v-for="(blog, index) in blogs">
          <div class="blog-card">
            <div class="blog-holder">
              <img class="blog-thumb" :src="getImage(blog.thumbnail)">
              <div class="blog-details-holder">
                <h1 class="blog-title">{{blog.title}}</h1>
                <p class="blog-summary">{{blog.description}}
                </p>
                <nuxt-link class="blog-link" :to="`${'/blogs/'+blog.id}`" target="_blank">Read <span class="d-sm-none">blog</span></nuxt-link>
              </div>
            </div>
          </div>
        </template>
      </div>
    </div>

    <div id="contact">
      <div class="container-md">
        <div class="f-container">
          <div class="container sec-1">
            <h2 class="fo-que">Are you looking for a</h2>
            <h1 class="text-gradient1 f-heading d-lg-none">UX Designer</h1>

            <vue-typed-js
              :strings="['User Experience Designer', 'Product Designer', 'User interface Designer']"
              :loop="true"
              :typeSpeed="100"
              :backSpeed="80"
              :smartBackspace="true"
              :cursorChar="''"
            >
              <h1 class="typing text-gradient1 f-heading d-none d-lg-block"></h1>
            </vue-typed-js>
            <h2 class="f-sub-heading">Why not me</h2>
            <p class="fo-sub">Just fill-up this form or email me, I’ll contact you soon to discuss about
              your
              dream project.
            </p>
          </div>
          <div class="bg-black2 p-3 sec-2">
            <form class="container" action="#">
              <div class="py-3">
                <label class="form-label1" for="name">Your name <span class="required">*</span></label>
                <input class="form-control1" type="text">
              </div>
              <div class="py-3">
                <label class="form-label1" for="name">Your email <span class="required">*</span></label>
                <input class="form-control1" type="text">
              </div>
              <div class="py-3">
                <label class="form-label1" for="name">Company name (Optional)</label>
                <input class="form-control1" type="text">
              </div>
              <div class="py-3">
                <label class="form-label1" for="name">Tell me abount your project/offer <span
                  class="required">*</span></label>
                <input class="form-control1" type="text">
              </div>
              <div class="py-3">
                <button class="btn-primary-square-rounded" type="submit">Submit</button>
              </div>
            </form>
          </div>
          <div class="container sec-3">
            <p class="fw-bold">Find me on</p>
            <div class="social-container">
              <a class="s-link" href="#">FACEBOOK<img src="../layouts/assets/arrow-top-right.svg"></a>
              <a class="s-link" href="#">FACEBOOK<img src="../layouts/assets/arrow-top-right.svg"></a>
              <a class="s-link" href="#">FACEBOOK<img src="../layouts/assets/arrow-top-right.svg"></a>
              <a class="s-link" href="#">FACEBOOK<img src="../layouts/assets/arrow-top-right.svg"></a>
              <a class="s-link" href="#">FACEBOOK<img src="../layouts/assets/arrow-top-right.svg"></a>
            </div>
            <p class="fw-bold mt-5">Contact</p>
            <p class="fs-5 m-0 text-black">e.rakib@gmail.com</p>
            <p class="fs-5 m-0 text-black">+880 1710 451430</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import axios from 'axios'
export default {
  name: 'IndexPage',
  head() {
    return {
      title: 'Rakib'
    }
  },
  data() {
    return {
      caseStudies: [],
      blogs: [],
      backendUrl: 'http://127.0.0.1:8000'
    }
  },

  created() {
    this.getCaseStudies()
    this.getBlogs()
  },

  methods: {
    async getCaseStudies() {
      let caseStudy = await axios.get(this.backendUrl + '/api/case-study')
        .then(({data}) => {

          this.caseStudies = data.data
        }).catch(err => {
          console.log('case study error')
        })
    },
    async getBlogs() {
      let blogs = await axios.get(this.backendUrl + '/api/blog')
        .then(({data}) => {
          this.blogs = data.data
        }).catch(err => {
          console.log('blogs error')
        })
    },
    getImage(imageLink) {
      return this.backendUrl + imageLink;
    }
  }
}
</script>
