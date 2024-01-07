<template>
  <div class="text-center text-xl bg-[#00102e] pb-8">
    <TitresH2>Contact</TitresH2>
    <p class="text-[#f5f5f5]">Remplissez le formulaire pour nous contacter</p>
  </div>
  <!-- component -->
  <div
    class=" flex items-top justify-center  bg-white sm:items-center sm:pt-0"
  >
    <div class="max-w-6xl mx-auto sm:px-6 lg:px-8">
      <div class="mt-8 overflow-hidden">
        <div class="grid grid-cols-1 md:grid-cols-2">
          <div class="p-6 mr-2 bg-gray-100 dark:bg-[#00102e] sm:rounded-lg">
            <h1
              class="text-4xl sm:text-5xl text-gray-800 dark:text-white font-extrabold tracking-tight"
            >
              Get in touch
            </h1>
            <p
              class="text-normal text-lg sm:text-2xl font-medium  dark:text-[#FFFFFF] mt-2"
            >
              Fill in the form to start a conversation
            </p>

            <div
              class="flex items-center mt-8 text-gray-600 dark:text-[#FFFFFF]"
            >
              <svg
                fill="none"
                stroke="currentColor"
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="1.5"
                viewBox="0 0 24 24"
                class="w-8 h-8 text-[#e75a36]"
              >
                <path
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  stroke-width="1.5"
                  d="M17.657 16.657L13.414 20.9a1.998 1.998 0 01-2.827 0l-4.244-4.243a8 8 0 1111.314 0z"
                />
                <path
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  stroke-width="1.5"
                  d="M15 11a3 3 0 11-6 0 3 3 0 016 0z"
                />
              </svg>
              <div class="ml-4 text-md tracking-wide font-semibold w-40">
                Rue des potiers, 3, 1330 Rixensart
              </div>
            </div>

            <div
              class="flex items-center mt-4 text-gray-600 dark:text-[#ffffff]"
            >
              <svg
                fill="none"
                stroke="currentColor"
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="1.5"
                viewBox="0 0 24 24"
                class="w-8 h-8 text-[#e75a36]"
              >
                <path
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  stroke-width="1.5"
                  d="M3 5a2 2 0 012-2h3.28a1 1 0 01.948.684l1.498 4.493a1 1 0 01-.502 1.21l-2.257 1.13a11.042 11.042 0 005.516 5.516l1.13-2.257a1 1 0 011.21-.502l4.493 1.498a1 1 0 01.684.949V19a2 2 0 01-2 2h-1C9.716 21 3 14.284 3 6V5z"
                />
              </svg>
              <div class="ml-4 text-md tracking-wide font-semibold w-40">
                +32 457 854 624
              </div>
            </div>

            <div
              class="flex items-center mt-2 text-gray-600 dark:text-[#ffffff]"
            >
              <svg
                fill="none"
                stroke="currentColor"
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="1.5"
                viewBox="0 0 24 24"
                class="w-8 h-8 text-[#e75a36]"
              >
                <path
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  stroke-width="1.5"
                  d="M3 8l7.89 5.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z"
                />
              </svg>
              <div class="ml-4 text-md tracking-wide font-semibold w-40">
                info@recycraft.com
              </div>
            </div>
          </div>

          <form class="p-6 flex flex-col justify-center">
            <div class="flex flex-col">
              <label for="name" class="hidden">Nom complet</label>
              <input
                type="name"
                name="name"
                id="name"
                placeholder="Nom complet"
                class="w-100 mt-2 py-3 px-3 rounded-lg  border border-[#00102e] dark:border-[#00102e] text-[#00102e] font-semibold focus:border-[#e75a36] focus:outline-none"
              />
            </div>

            <div class="flex flex-col mt-2">
              <label for="email" class="hidden">Votre adresse email</label>
              <input
                type="email"
                name="email"
                id="email"
                placeholder="Votre adresse email"
                class="w-100 mt-2 py-3 px-3 rounded-lg  border border-[#00102e] dark:border-[#00102e] text-[#00102e] font-semibold focus:border-[#e75a36] focus:outline-none"
              />
            </div>

            <div class="flex flex-col mt-2">
              <label for="sujet" class="hidden">Sujet</label>
              <input
                type="sujet"
                name="sujet"
                id="sujet"
                placeholder="Sujet"
                class="w-100 mt-2 py-3 px-3 rounded-lg bg-white dark:bg-[white] border border-[#00102e] dark:border-[#00102e] text-gray-800 font-semibold focus:border-[#e75a36] focus:outline-none"
              />
            </div>
  <div class="flex flex-col mt-2">
    <label for="message" class="hidden">Votre message</label>
    <textarea
      name="message"
      id="message"
      placeholder="Votre message"
      class="w-100 mt-2 py-3 px-3 rounded-lg bg-white  border border-[#00102e] dark:border-gray-700 text-[#00102e] font-semibold focus:border-[#e75a36] focus:outline-none"
    ></textarea></div>
            <button
              type="submit"
              class=" md:w-32 bg-[#00102e] hover:bg-white text-[white] border border-[#00102e] font-bold py-3 px-6 rounded-lg mt-3 hover:text-[#00102e] transition ease-in-out duration-300"
            >
              Envoyer
            </button>

          </form>
          <iframe class="mt-8 mb-8" src="https://www.google.com/maps/embed?pb=!1m16!1m12!1m3!1d1263.226158494583!2d4.52116261441138!3d50.71154720521629!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!2m1!1sRue%20des%20potiers%2C%203%2C%201330%20Rixensart!5e0!3m2!1sfr!2sbe!4v1704629125447!5m2!1sfr!2sbe" width="1080" height="450" style="border:0;" allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
        </div>
      </div>
    </div>
  </div>
</template>
