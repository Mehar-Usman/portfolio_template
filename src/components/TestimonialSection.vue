<template>
    <div class="bg-orange-100 py-20">
      <p class="text-center text-orange-500 uppercase text-2xl">Testimonial</p>
      <p class="text-4xl font-900 text-center mt-4">What Our <br> Clients Saying</p>
      <div class="grid grid-cols-1 md:grid-cols-2 px-6 md:px-10 lg:px-20 pt-20 xl:px-28 gap-10 md:gap-0">
        <div v-for="(testimonial, index) in testimonials" :key="index">
          <article class="px-8 py-10 border border-gray-500 h-full"
                   :class="{ 'border md:border-b-0 rounded-lg md:rounded-tl-lg md:rounded-tr-none md:rounded-b-none bg-white': index === 0 },
                           { 'border md:border-l-0 md:border-b-0 rounded-lg md:rounded-tl-none md:rounded-b-none md:rounded-tr-lg ': index === 1 },
                           { 'border md:border-r-0 rounded-lg md:rounded-br-none md:rounded-t-none md:rounded-bl-lg': index === 2 },
                           { 'rounded-lg md:rounded-bl-none md:rounded-t-none md:rounded-br-lg ': index === 3 }">
            <div class="flex">
              <img v-for="star in 5" :key="star" src="../assets/star.svg" alt="Star">
            </div>
            <div class="mt-5">
              <p>{{ testimonial.content }}</p>
            </div>
            <div class="flex gap-3 items-center mt-5">
              <div>
                <img :src="getImagePath(index)" alt="User Image">
              </div>
              <div>
                <h1>{{ testimonial.name }}</h1>
                <p>{{ testimonial.company }}</p>
              </div>
            </div>
          </article>
        </div>
      </div>
      <div class="flex justify-center mt-10">
        <button class="mt-5 text-black bg-white shadow-2xl uppercase px-6 py-2 border-2 border-gray-500 rounded transition-all ease-in-out font-semibold hover:border-white hover:scale-110 duration-500 hover:bg-gray-900 hover:text-white">See All</button>
      </div>
    </div>
  </template>
  
  <script setup>
  const testimonials = [
    {
      content: "A digital agency is a business you hire to outsource your digital marketing efforts, instead of handling in-house. They can provide your business with a variety of digital solutions to promote your product or service online and help you.",
      name: "Alan Martí",
      company: "Meta Inc."
    },
    {
      content: "Outsource your digital marketing efforts, instead of handling in-house. They can provide your business with a variety.",
      name: "Maria Trofimova",
      company: "Whochat"
    },
    {
      content: "Provide your business with a variety of digital solutions to promote your product or service online.",
      name: "Richardo Kann",
      company: "Photographer"
    },
    {
      content: "Promote your product or service online and help you hit your marketing goals and grow your business.",
      name: "Graham Griffiths",
      company: "Twitor"
    }
  ];
  
  const getImagePath = (index) => {
    // Assuming images are located in a static folder named "assets"
    const imageNames = ['testimonial-img-1.png', 'testimonial-img-2.png', 'testimonial-img-3.png', 'testimonial-img-4.png'];
    return `src/assets/${imageNames[index]}`;
  };
  </script>
  
  <style></style>
  