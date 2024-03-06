<template>
    <div>
        <div class="bg-orange-100 px-6 md:px-10 lg:px-20 py-12 xl:px-28">
            <div class="block md:flex justify-between ">
                <div>
                    <p class="font-900 text-4xl ">Newsletter</p>
                </div>
                <div>
                    <div class="block md:flex gap-10">
                        <div>
                            <input type="text" placeholder="Your Email"
                                class="border-orange-200 border-2  rounded-md  py-[10px] px-3 outline-none bg-white shadow-2xl">
                        </div>
                        <div>
                            <button
                                class="text-black bg-white shadow-2xl uppercase px-6 py-2 border-2 border-gray-500 rounded transition-all ease-in-out font-semibold hover:border-white hover:scale-110 duration-500 hover:bg-gray-900 hover:text-white">
                                Subscribe
                            </button>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <div class="bg-img-set ">
            <div
                class="grid grid-cols-1 md:grid-cols-2 gap-12 md:gap-10 lg:gap-20 px-6 md:px-10 lg:px-20 py-20 xl:px-28">
                <article class="bg-white shadow-2xl rounded-xl py-8 px-6">
                    <p class="text-2xl font-bold">Get In Touch</p>
                    <div class="mt-6">
                        <input type="text" class="w-full  py-3 px-4 border-2 border-orange-200 outline-none rounded-md"
                            placeholder="Your email ">
                    </div>
                    <div class="mt-6">
                        <select class=" border-2 outline-none border-orange-200 w-full py-3 px-4 rounded-md" name=""
                            id="">
                            <optgroup>
                                <option selected value="">Subject</option>
                                <option class="mt-3" value="">Option-1</option>
                                <option class="mt-3" value="">Option-2</option>
                                <option class="mt-3" value="">Option-3</option>
                            </optgroup>
                        </select>
                    </div>
                    <div class="mt-6">
                        <textarea class=" border-2 outline-none border-orange-200 w-full px-6 py-3" name="" id=""
                            cols="" rows="3" placeholder="Message"></textarea>
                    </div>
                </article>
                <div class="bg-white shadow-2xl rounded-xl py-8 px-6">
                    <p class="text-2xl font-bold">Get In Touch</p>
                    <p>Whether you have questions, feedback, or simply want to connect, we're here to assist you every
                        step of the way.</p>
                    <p>Feel free to reach out to us for:</p>
                    <ul class="list-disc ml-6 mt-3">
                        <li>Assistance from our knowledgeable support team</li>
                        <li>Inquiries about our products or services</li>
                        <li>Collaboration opportunities or partnership queries</li>
                        <li>Feedback on your experience with our platform</li>
                        <li>Customized solutions tailored to your needs</li>
                    </ul>
                    <p>We value your input and look forward to hearing from you!</p>
                </div>

            </div>
        </div>
    </div>
</template>

<script>
export default {
    // Your script logic
}
</script>

<style scoped>
.bg-img-set {
    background-image: url(src/assets/map.png);
    height: fit-content;
    background-position: center;
    background-size: cover;
}
</style>