<template>
    <div class="bg-orange-100 px-6 md:px-10 lg:px-20 py-20 xl:px-28">
      <div class="grid grid-cols-1 md:grid-cols-2 gap-20">
        <div>
          <p class="text-2xl text-orange-500">FAQ</p>
          <h1 class="text-5xl font-900 mt-5">Frequently Asked Questions</h1>
          <p class="w-5/6 mt-5">A digital agency is a business you hire to outsource your digital marketing efforts, instead of handling in-house.</p>
          <div class="mt-4">
            <button
              class="text-black bg-white shadow-2xl uppercase px-6 py-2 border-2 border-gray-500 rounded transition-all ease-in-out font-semibold hover:border-white hover:scale-110 duration-500 hover:bg-gray-900 hover:text-white">
              Contact Us
            </button>
          </div>
        </div>
        <div>
          <div id="accordion-collapse" data-accordion="collapse">
            <!-- Render FAQ items dynamically -->
            <div v-for="(faq, index) in faqs" :key="index">
              <h2 :id="'accordion-collapse-heading-' + (index + 1)">
                <button
                  type="button"
                  @click="toggleAccordion(index)"
                  :class="{'active': activeAccordion === index},
                   {'border-b' : index===3} ,
                   {'rounded-t-xl':index===0},
                   {'rounded-b-xl' : index===3}"
                  class="flex items-center  justify-between w-full p-5 font-medium rtl:text-right text-gray-900 border border-b-0 border-gray-500   dark:focus:ring-gray-800 dark:border-gray-700 dark:text-gray-400 hover:bg-gray-100 dark:hover:bg-gray-800 gap-3 "
                  :data-accordion-target="'#accordion-collapse-body-' + (index + 1)"
                  :aria-expanded="activeAccordion === index"
                  :aria-controls="'accordion-collapse-body-' + (index + 1)">
                  <span>{{ faq.question }}</span>
                  <svg
                    data-accordion-icon
                    :class="{'rotate-180': activeAccordion === index}"
                    class="w-3 h-3 shrink-0"
                    aria-hidden="true"
                    xmlns="http://www.w3.org/2000/svg"
                    fill="none"
                    viewBox="0 0 10 6">
                    <path stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 5 5 1 1 5" />
                  </svg>
                </button>
              </h2>
              <div
                :id="'accordion-collapse-body-' + (index + 1)"
                :class="{'hidden': activeAccordion !== index},
                {'border-b rounded-b-xl':index===3}"
                class="p-5 border border-b-0 border-gray-500 dark:border-gray-700 dark:bg-gray-900">
                <p class="mb-2 text-gray-900 dark:text-gray-400">{{ faq.answer }}</p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        faqs: [
          {
            question: "A digital agency is a business",
            answer: "Digital marketing efforts, instead of handling in-house. They can provide your business with a variety of digital solutions to promote your product or service online and help you hit your marketing goals and grow your business."
          },
          {
            question: "Hire to outsource your digital",
            answer: "Hire us to outsource your digital marketing needs. Boost your online presence, reach your target audience, and achieve business growth effortlessly. Contact us now!"
          },
          {
            question: "Marketing efforts",
            answer: "Outsource your marketing efforts to us! Our expertise drives results, expands your reach, and optimizes strategies for maximum impact. Contact us today for tailored solutions!"
          },
          {
            question: "Can provide your business",
            answer: "We provide your business with comprehensive digital marketing solutions. From strategy to execution, our team ensures growth, visibility, and success. Get in touch to elevate your brand!"
          }
        ],
        activeAccordion: null
      };
    },
    methods: {
      toggleAccordion(index) {
        this.activeAccordion = this.activeAccordion === index ? null : index;
      }
    }
  };
  </script>
  
  <style>
  /* Add your custom styles here */
  </style>
  