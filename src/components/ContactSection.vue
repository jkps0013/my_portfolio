<template>
  <section class="text-white mt-20" id="contact">
    <h2 class="text-4xl font-bold text-white text-left mb-4 px-4 xl:pl-16">
      Let's Connect
    </h2>
    <div
      class="grid md:grid-cols-2 gap-4 relative px-4 xl:px-16 mt-8"
      data-aos="zoom-in-up"
    >
      <div>
        <p class="text-[#adb7be]">
          Looking to collaborate, discuss opportunities, or just say hello? Feel
          free to reach out! Whether it’s about sharing ideas, exploring
          partnerships, or discussing future projects, I’m always excited to
          connect and hear from you. Let’s create something amazing together!
        </p>
        <div class="col-lg-4 col-md-4 mb-lg-0 mt-5">
          <div class="flex mb-10 items-center">
            <div
              class="p-2"
              style="
                background: #111a3e;
                width: 50px;
                height: 46px;
                display: flex;
                justify-content: center;
                border-radius: 50%;
                overflow: hidden;
                border: 1px solid#111a3e;
                backdrop-filter: blur(9px);
                -webkit-backdrop-filter: blur(9px);
              "
            >
              <img
                src="https://img.icons8.com/metro/50/ffffff/new-post.png"
                alt="new-post"
                class="w-6"
              />
            </div>
            <div class="ml-5 text-white">
              <h4>Email</h4>
              <p>jayakrishnan6901@gmail.com</p>
            </div>
          </div>
          <div class="flex mb-10 items-center">
            <div
              class="p-2"
              style="
                background: #111a3e;
                width: 50px;
                height: 46px;
                display: flex;
                justify-content: center;
                border-radius: 50%;
                overflow: hidden;
                border: 1px solid#111a3e;
                backdrop-filter: blur(9px);
                -webkit-backdrop-filter: blur(9px);
              "
            >
              <img
                src="https://img.icons8.com/?size=100&id=32309&format=png&color=FFFFFF"
                alt="new-post"
                class="w-6"
              />
            </div>
            <div class="ml-5 text-white">
              <h4>Instagram</h4>
              <a href="https://www.instagram.com/jk_ps_0013?igsh=MXNiOTI1NjliZHY0eA==">jk_ps_0013</a>
            </div>
          </div>
          <div class="flex mb-10 items-center">
            <div
              class="p-2"
              style="
                background: #111a3e;
                width: 50px;
                height: 46px;
                display: flex;
                justify-content: center;
                border-radius: 50%;
                overflow: hidden;
                border: 1px solid#111a3e;
                backdrop-filter: blur(9px);
                -webkit-backdrop-filter: blur(9px);
              "
            >
              <img
                src="https://img.icons8.com/ios-filled/50/ffffff/phone.png"
                alt="phone"
                class="w-6"
              />
            </div>
            <div class="ml-5 text-white">
              <h4>Phone</h4>
              <p>+91 9207072030</p>
            </div>
          </div>
          <div class="flex mb-10 items-center">
            <div
              class="p-2"
              style="
                background: #111a3e;
                width: 50px;
                height: 46px;
                display: flex;
                justify-content: center;
                border-radius: 50%;
                overflow: hidden;
                border: 1px solid#111a3e;
                backdrop-filter: blur(9px);
                -webkit-backdrop-filter: blur(9px);
              "
            >
              <img
                src="https://img.icons8.com/ios-filled/50/ffffff/linkedin.png"
                alt="linkedin"
                class="w-6"
              />
            </div>
            <div class="ml-5 text-white">
              <h4>LinkedIn</h4>
              <a href="https://linkedin.com/in/jayakrishnan-ps-949502190"
                >linkedin.com/in/jayakrishnan-ps-949502190</a
              >
            </div>
          </div>
        </div>
      </div>
      <div
        style="
          background: #111a3e;
          width: 100%;
          height: 100%;
          border-radius: 20px;
          overflow: hidden;
          border: 1px solid #111a3e;
          backdrop-filter: blur(9px);
          -webkit-backdrop-filter: blur(9px);
        "
      >
        <form
          class="flex flex-col p-2"
          data-aos="zoom-in-up"
          @submit.prevent="handleSubmit"
        >
          <div class="mb-8">
            <label for="email" class="text-white block mb-2 text-sm font-medium"
              >email</label
            >
            <input
              type="email"
              id="email"
              class="bg-[#111827] placeholder:[#9CA2A9] text-gray-100 text-sm rounded-lg block w-full p-2.5"
              placeholder="email@gmail.com"
              name="email"
              v-model="mail.email"
            />
          </div>
          <div class="mb-8">
            <label
              for="subject"
              class="text-white block mb-2 text-sm font-medium"
              >Subject</label
            >
            <input
              type="subject"
              id="subject"
              class="bg-[#111827] placeholder:[#9CA2A9] text-gray-100 text-sm rounded-lg block w-full p-2.5"
              placeholder="subject"
              name="subject"
              v-model="mail.subject"
            />
          </div>
          <div class="mb-10">
            <label
              for="message"
              class="text-white block mb-2 text-sm font-medium"
              >Message</label
            >
            <textarea
              id="Message"
              class="bg-[#111827] placeholder:[#9CA2A9] text-gray-100 text-sm rounded-lg block w-full p-2.5"
              placeholder="Let's talk about ... "
              name="Message"
              v-model="mail.message"
            ></textarea>
          </div>
          <button
            class="z-1 w-[100%!important] px-6 md:px-7 py-3 rounded-full sm:w-max flex justify-center text-white bg-primary border-2 border-transparent"
            type="submit"
          >
            Send Message
          </button>
        </form>
      </div>
      <div
        class="bg-gradient-to-tr opacity-25 from-[#570cac] to-primary blur-2xl h-20 w-80 z-0 absolute -top-1/2 -left-4 transform -translate-x-2/3 -translate-1/2"
      ></div>
    </div>
  </section>
</template>
<script setup>
import { reactive, toRefs } from "vue";
import emailjs from "emailjs-com";
import Swal from "sweetalert2";
const mail = reactive({
  email: "",
  subject: "",
  message: "",
});
const { email, subject, message } = toRefs(mail);
const handleSubmit = async () => {

  const templateParams = {
    from_name: email.value,
    subject: subject.value,
    message: message.value,
  };
  console.log(templateParams);
  try {
    const response = await emailjs.send(
      import.meta.env.VITE_EMAILJS_SERVICE_ID,
      import.meta.env.VITE_EMAILJS_TEMPLATE_ID,
      templateParams,
      import.meta.env.VITE_EMAILJS_USER_ID
    );
  
    Swal.fire({
      icon: "success",
      title: "Email sent successfully!",
      toast: true,
      position: "top-end",
      showConfirmButton: false,
      timer: 2000,
      timerProgressBar: true,
    });
    mail.email = "";
    mail.subject = "";
    mail.message = "";
  } catch (error) {
    console.log(error);
    Swal.fire({
      icon: "error",
      title: "Email sending failed!",
      toast: true,
      position: "top-end",
      showConfirmButton: false,
      timer: 2000,
      timerProgressBar: true,
    });
  }
};
</script>
