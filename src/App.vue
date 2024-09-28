<script setup>
import { ref } from 'vue';
import ButtonPrimary from '@/components/ButtonPrimary.vue';
import imageLogo from "@/assets/img/brand.png";

import BootcampQa from "@/assets/img/bootcamp-qa.png";
import BootcampPm from "@/assets/img/bootcamp-pm.png";
import BootcampDo from "@/assets/img/bootcamp-do.png";
import BootcampFull from "@/assets/img/bootcamp-full.png";
import FrameDummy from "@/assets/img/frame-dummy.png";
import FrameDummy1 from "@/assets/img/frame-dummy-1.png";
import FrameDummy2 from "@/assets/img/frame-dummy-2.png";
import FrameDummy3 from "@/assets/img/frame-dummy-3.png";
import Pfp1 from "@/assets/img/pfp-1.png";
import Pfp2 from "@/assets/img/pfp-2.png";
import Pfp3 from "@/assets/img/pfp-3.png";
import FooterIcon from "@/assets/img/footer-icon.png";
import IconTelp from "@/assets/img/telp.png";
import IconEmail from "@/assets/img/email.png";
import IconIg from "@/assets/img/instagram.png";


const isOpen = ref(false);

const openPopUp = () => {
  isOpen.value = !isOpen.value;
};
</script>

<template>
  <header class="flex items-center justify-between px-3 lg:px-32 py-6">
    <img class="h-full" :src="imageLogo" alt="logo join sistem">
      <ul class="hidden lg:flex">
        <li class="mx-3">
          <a href="#">Home</a>
        </li>
        <li class="mx-3">
          <a href="#">Blog</a>
        </li>
        <li class="mx-3">
          <a href="#">About Us</a>
        </li>
        <li class="mx-3">
          <a href="#">Contact Us</a>
        </li>
      </ul>
    <button type="button" class="hidden lg:block bg-primary px-3 py-3 rounded-full text-white font-bold">
      Contact Us
    </button>

    <ButtonPrimary class="lg:hidden" @click="openPopUp">
      <img src="@/assets/img/menu-icon.png" class="w-6" alt="Menu Icon">
    </ButtonPrimary>
  </header>

  <div v-if="isOpen" class="fixed top-0 left-0 w-full h-full bg-black bg-opacity-50 z-10" @click="openPopUp">
    <div class="fixed top-0 right-0 w-3/4 h-full bg-white z-20 p-4" @click.stop>
      <ButtonPrimary @click="openPopUp">Close</ButtonPrimary>
      <ul class="mt-8">
        <li class="py-2">
          <a href="#">Home</a>
        </li>
        <li class="py-2">
          <a href="#">Blog</a>
        </li>
        <li class="py-2">
          <a href="#">About Us</a>
        </li>
        <li class="py-2">
          <a href="#">Contact Us</a>
        </li>
      </ul>
    </div>
  </div>

  <!-- Main ? -->
    <div class="mx-4 md:mx-20 my-10">
      <div class="container mx-auto px-4 py-16 flex flex-col md:flex-row items-center">
          <div class="md:w-1/2">
              <h2 class="text-yellow-500 text-sm font-bold mb-5">
                  CAREER ACCELERATE
              </h2>
              <h1 class="text-4xl font-bold text-gray-900 mb-5">
                  Meningkatkan Karir Anda di SISTEM Bootcamp
              </h1>
              <p class="text-gray-700 mb-8">
                  Pelajari dari ahli Teknik Perangkat Lunak yang berpengalaman di SEA dan mempercepat karir Anda sebagai Software Engineer.
              </p>
              <div class="flex flex-wrap space-x-4 mb-8 justify-center md:justify-start">
                <div class="flex items-center mb-4 w-full md:w-auto">
                    <img src="./assets/img/icon-1.png" alt="Icon 1" class="mr-3">
                    <p class="text-gray-900 font-bold">Build Community</p>
                </div>
                <div class="flex items-center mb-4 w-full md:w-auto">
                    <img src="./assets/img/icon-2.png" alt="Icon 2" class="mr-3">
                    <p class="text-gray-900 font-bold">Share Events</p>
                </div>
                <div class="flex items-center mb-4 w-full md:w-auto">
                    <img src="./assets/img/icon-3.png" alt="Icon 3" class="mr-3">
                    <p class="text-gray-900 font-bold">Get Information</p>
                </div>
            </div>
              <button class="bg-blue-500 text-white px-6 py-3 rounded-full font-bold">
                  Contact Us
              </button>
          </div>
          <div class="md:w-1/2 flex justify-center mt-8 md:mt-0">
              <img src="./assets/img/group.png" alt="Group of students" class="max-w-full h-auto" />
          </div>
      </div>
  </div>

  <div class="flex items-center justify-center" style="min-height: 50vh; background-color: white;">
    <div class="text-center">
      <h1 class="text-3xl font-bold text-gray-900 mb-10">Gabung Jadi Talenta Digital Terbaik<br>Bersama SISTEM</h1>
      <img src="./assets/img/frame-long.png" alt="">
    </div>
  </div>


  <!-- Jualan Kelas Open-->
    <div class="flex flex-col items-center px-4 py-5" id="app">
      <h1 class="text-3xl font-bold text-gray-900 mb-4">
        Cerita Sukses Peserta
      </h1>
      <p class="text-gray-500 mb-10 text-center">
        Cari berbagai macam event teknologi terbaik yang diadakan oleh komunitas dan di dukung oleh banyak perusahaan besar lainnya
      </p>
      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-6 mx-10">
        <!-- View Card 1 -->
        <div class="bg-white rounded-lg shadow-lg overflow-hidden">
          <img alt="Instructor for Quality Assurance Bootcamp" class="w-full object-cover" :src="BootcampQa" />
          <div class="p-6 bg-gray-50">
              <h3 class="text-2xl font-bold text-gray-800">
                  Quality Assurance
              </h3>
              <div class="flex items-center">
                  <p class="text-sm text-gray-600 mr-4">Live Class</p>
                  <p class="text-sm text-gray-600">3 Bulan</p>
              </div>
              <div class="flex items-center mt-4">
                  <img alt="Student 1" class="w-8 h-8 rounded-full" :src="FrameDummy1" />
                  <img alt="Student 2" class="w-8 h-8 rounded-full -ml-2" :src="FrameDummy2" />
                  <img alt="Student 3" class="w-8 h-8 rounded-full -ml-2" :src="FrameDummy3" />
                  <span class="ml-2 text-gray-600">3000 +</span>
              </div>
              <a class="mt-4 inline-block text-blue-600 font-semibold" href="#">
                  Daftar Sekarang →
              </a>
          </div>
        </div>
        <!-- View Card 2 -->
        <div class="bg-white rounded-lg shadow-lg overflow-hidden">
          <img alt="Instructor for Project Manager Bootcamp" class="w-full object-cover" :src="BootcampPm" />
          <div class="p-6 bg-gray-50">
              <h3 class="text-2xl font-bold text-gray-800">
                  Project Manager
              </h3>
              <div class="flex items-center">
                  <p class="text-sm text-gray-600 mr-4">Live Class</p>
                  <p class="text-sm text-gray-600">3 Bulan</p>
              </div>
              <div class="flex items-center mt-4">
                  <img alt="Student 1" class="w-8 h-8 rounded-full" :src="FrameDummy1" />
                  <img alt="Student 2" class="w-8 h-8 rounded-full -ml-2" :src="FrameDummy2" />
                  <img alt="Student 3" class="w-8 h-8 rounded-full -ml-2" :src="FrameDummy3" />
                  <span class="ml-2 text-gray-600">3000 +</span>
              </div>
              <a class="mt-4 inline-block text-blue-600 font-semibold" href="#">
                  Daftar Sekarang →
              </a>
          </div>
        </div>
        <!-- View Card 3 -->
        <div class="bg-white rounded-lg shadow-lg overflow-hidden">
          <img alt="Instructor for Dev-Op Bootcamp" class="w-full object-cover" :src="BootcampDo" />
          <div class="p-6 bg-gray-50">
              <h3 class="text-2xl font-bold text-gray-800">
                Development Operations
              </h3>
              <div class="flex items-center">
                  <p class="text-sm text-gray-600 mr-4">Live Class</p>
                  <p class="text-sm text-gray-600">3 Bulan</p>
              </div>
              <div class="flex items-center mt-4">
                  <img alt="Student 1" class="w-8 h-8 rounded-full" :src="FrameDummy1" />
                  <img alt="Student 2" class="w-8 h-8 rounded-full -ml-2" :src="FrameDummy2" />
                  <img alt="Student 3" class="w-8 h-8 rounded-full -ml-2" :src="FrameDummy3" />
                  <span class="ml-2 text-gray-600">3000 +</span>
              </div>
              <a class="mt-4 inline-block text-blue-600 font-semibold" href="#">
                  Daftar Sekarang →
              </a>
          </div>
        </div>
        <!-- View Card 4 -->
        <div class="bg-white rounded-lg shadow-lg overflow-hidden">
          <img alt="Instructor for Fullstack Developer Bootcamp" class="w-full object-cover" :src="BootcampFull" />
          <div class="p-6 bg-gray-50">
              <h3 class="text-2xl font-bold text-gray-800">
                Fullstack Developer
              </h3>
              <div class="flex items-center">
                  <p class="text-sm text-gray-600 mr-4">Live Class</p>
                  <p class="text-sm text-gray-600">3 Bulan</p>
              </div>
              <div class="flex items-center mt-4">
                  <img alt="Student 1" class="w-8 h-8 rounded-full" :src="FrameDummy1" />
                  <img alt="Student 2" class="w-8 h-8 rounded-full -ml-2" :src="FrameDummy2" />
                  <img alt="Student 3" class="w-8 h-8 rounded-full -ml-2" :src="FrameDummy3" />
                  <span class="ml-2 text-gray-600">3000 +</span>
              </div>
              <a class="mt-4 inline-block text-blue-600 font-semibold" href="#">
                  Daftar Sekarang →
              </a>
          </div>
        </div>
      </div>
    </div>
  <!-- Jualan Kelas Close-->


  <!-- Cerita Sukses Open-->
  <div class="font-inter">
    <div class="flex flex-col items-center mt-40 px-4" id="app">
      <h1 class="text-3xl font-semibold text-gray-800 mb-2">
        Cerita Sukses Peserta
      </h1>
      <p class="text-gray-500 mb-12 text-center">
        Cari berbagai macam event teknologi terbaik yang diadakan oleh komunitas dan di dukung oleh banyak perusahaan besar lainnya
      </p>
      <div class="flex flex-wrap justify-center gap-8">
        <div class="bg-white shadow-lg rounded-lg p-6 max-w-sm">
        <div class="flex items-center mb-4">
          <img alt="Profile picture of Syihabudin Ahmad" class="w-10 h-10 rounded-full mr-4" :src="Pfp1"/>
          <div>
          <h2 class="text-lg font-semibold text-gray-800">
            Syihabudin Ahmad
          </h2>
          <p class="text-sm text-gray-500">
            Project Manager Solutionlabs
          </p>
          </div>
        </div>
        <p class="text-gray-600">
          Sistem Top Markotop, selama belajar cara dan arahan mentor unik selain itu mentor juga membantu kami jika ada kesulitan.
        </p>
        </div>
        <div class="bg-white shadow-lg rounded-lg p-6 max-w-sm">
        <div class="flex items-center mb-4">
          <img alt="Profile picture of Annastasya KW" class="w-10 h-10 rounded-full mr-4" :src="Pfp2"/>
          <div>
          <h2 class="text-lg font-semibold text-gray-800">
            Annastasya KW
          </h2>
          <p class="text-sm text-gray-500">
            Project Manager Solutionlabs
          </p>
          </div>
        </div>
        <p class="text-gray-600">
          Dulu sebelum belajar tentang PM di SISTEM sering kesulitan buat manage project, setelah ikut bootcamp sistem jadi tau gimana biar project itu bisa selesai dan achive
        </p>
        </div>
        <div class="bg-white shadow-lg rounded-lg p-6 max-w-sm">
        <div class="flex items-center mb-4">
          <img alt="Profile picture of Tasya WA" class="w-10 h-10 rounded-full mr-4" :src="Pfp3"/>
          <div>
          <h2 class="text-lg font-semibold text-gray-800">
            Tasya WA
          </h2>
          <p class="text-sm text-gray-500">
            Quality Assurance Solutionlabs
          </p>
          </div>
        </div>
        <p class="text-gray-600">
          Kemarin waktu belajar coding disini enak banget, kita di kelas bener-bener dibimbing dari nol (0) sama mentor dan pembelajarannya juga gampang di pahami.
        </p>
        </div>
      </div>
    </div>
  </div>
  <!-- Cerita Sukses Close-->

  <!-- Gabung Sekarang Open -->
  <div class="flex items-center justify-center" style="min-height: 70vh; background-color: white;">
    <div class="text-center">
      <h1 class="text-3xl font-bold text-gray-900 mb-4">Gabung Jadi Talenta Digital Terbaik<br>Bersama SISTEM</h1>
      <p class="text-gray-500 mb-8">Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt.</p>
      <button class="bg-blue-600 text-white font-bold py-2 px-6 rounded">Daftar Sekarang</button>
    </div>
  </div>
  <!-- Gabung Sekarang Close -->

  <!-- Footer Open-->
  <div id="app" class="bg-blue-950 text-white py-10">
    <div class="container mx-auto px-16">
        <div class="grid grid-cols-1 md:grid-cols-4 gap-16">
            <div>
                <img :src="FooterIcon" alt="Footer Icon" class="mb-16" />
                <div class="my-5">
                    <h2 class="font-bold">Jogja Office</h2>
                    <p class="text-sm">Jl. Kresna, Gamping Kidul, Ambarketawang, Kec. Gamping, Kabupaten Sleman, DIY 55294</p>
                </div>
                <div class="my-10">
                    <h2 class="font-bold">Jakarta Office</h2>
                    <p class="text-sm">Cibis Nine Building Lantai 11 Jl. TB Simatupang No. 2 Jakarta Selatan</p>
                </div>
            </div>
            <div>
                <h2 class="text-xl font-bold mb-4">Bootcamp</h2>
                <ul>
                    <li class="my-5">DevOps</li>
                    <li class="my-5">Quality Assurance</li>
                    <li class="my-5">Full Stack Developer</li>
                    <li class="my-5">Project Manager</li>
                </ul>
            </div>
            <div>
                <h2 class="text-xl font-bold mb-4">SISTEM</h2>
                <ul>
                    <li class="mb-2">Tentang Kami</li>
                    <li class="mb-2">Events</li>
                    <li>FAQ</li>
                </ul>
            </div>
            <div>
                <h2 class="text-xl font-bold mb-4">Ikuti Kami</h2>
                <div class="flex items-center mb-2">
                  <img :src="IconIg" alt="Icon Instagram">
                </div>
                <div class="flex items-center mb-2">
                    <img :src="IconTelp" alt="Icon Telp" class="mr-2">
                    <span>+62 811-269-086</span>
                </div>
                <div class="flex items-center mb-2">
                    <img :src="IconEmail" alt="Icon Email" class="mr-2">
                    <span>putro@solutionlabs.id</span>
                </div>
            </div>
        </div>
    </div>
  </div>
  <!-- Footer Close-->

</template>
