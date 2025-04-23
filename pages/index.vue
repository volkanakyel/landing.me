<template>
  <div class="bg-[#efefef] min-h-screen w-full text-[#333] p-0 m-0 overflow-x-hidden relative">
    <SportBackground />

    <div class="flex justify-center items-center py-8">
      <Motion
        :initial="{ opacity: 0, y: -20 }"
        :animate="{ opacity: 1, y: 0 }"
        :transition="{ duration: 0.5, ease: 'easeOut' }"
        class="flex items-center"
      >
        <div class="flex items-center">
          <div class="bg-[#e9e9e9] rounded-full p-3 -ml-16 mr-8">
            <Icon
              name="lucide:settings"
              class="h-5 w-5 text-gray-700"
            />
          </div>
          <div class="flex items-center gap-4 bg-[#e9e9e9] rounded-full px-12 py-3">
            <a
              href="#"
              class="text-[#666] font-medium hover:text-[#333] transition-colors duration-200"
              >Home</a
            >
            <a
              href="#"
              class="text-[#666] font-medium hover:text-[#333] transition-colors duration-200"
              >Lookbook</a
            >
            <a
              href="#"
              class="text-[#666] font-medium hover:text-[#333] transition-colors duration-200"
              >Favorite</a
            >
            <a
              href="#"
              class="text-[#666] font-medium hover:text-[#333] transition-colors duration-200"
              >Blog</a
            >
            <a
              href="#"
              class="text-[#666] font-medium hover:text-[#333] transition-colors duration-200"
              >About</a
            >
          </div>
        </div>
      </Motion>
    </div>

    <!-- Main Content -->
    <main class="max-w-[1400px] mx-auto mt-12 relative px-4 sm:px-6 lg:px-8">
      <!-- Hero Section -->
      <div class="min-h-[80vh] flex flex-col justify-center items-center relative">
        <!-- Heading Section -->
        <Motion
          :initial="{ opacity: 0, y: 20 }"
          :animate="{ opacity: 1, y: 0 }"
          :transition="{ duration: 0.7, ease: 'easeOut', delay: 0.3 }"
          class="text-center mb-8 sm:mb-16"
        >
          <h1
            class="text-4xl sm:text-5xl lg:text-6xl font-medium leading-tight text-[#333] tracking-tight"
          >
            Choose from the <br />
            <b>styles.</b>
          </h1>
          <p class="leading-relaxed text-[#666] max-w-[600px] mt-8 sm:mt-16 mx-auto">
            Whether you're searching for the perfect outfit for a special occasion or refreshing
            your everyday style, our team of experienced professional stylists is here to guide you
            every step of the way.
          </p>
        </Motion>

        <!-- Style Categories Section -->
        <div class="flex flex-col gap-3 sm:gap-6 justify-center w-full mb-8 sm:mb-16 px-4 sm:px-0">
          <!-- First row -->
          <div class="hidden sm:flex gap-6 justify-center w-full px-12">
            <Motion
              v-for="(category, index) in categories.slice(0, 3)"
              :key="category.name"
              :initial="{ opacity: 0, scale: 0.95, y: 20 }"
              :animate="{ opacity: 1, scale: 1, y: 0 }"
              :transition="{ duration: 0.7, ease: 'easeOut', delay: 1 + index * 0.15 }"
              :while-hover="{ scale: 1.05, y: -4, transition: { duration: 0.2 } }"
              :while-tap="{ scale: 0.95, transition: { duration: 0.1 } }"
              :in-view="{ opacity: 1, scale: 1, y: 0 }"
              :viewport="{ once: true, amount: 0.5 }"
              class="flex items-center bg-white cursor-pointer p-1 pl-4 pr-4 gap-2 rounded-full shadow-sm hover:shadow-md transition-all duration-200"
            >
              <div class="hover:scale-110 transition-transform duration-200">
                <img
                  :src="category.image"
                  :alt="category.name"
                  class="w-10 h-10 object-cover rounded-full"
                />
              </div>
              <span
                class="text-gray-800 font-medium whitespace-nowrap hover:text-black transition-colors duration-200"
              >
                {{ category.name }}
              </span>
            </Motion>
          </div>

          <!-- Second row desktop -->
          <div class="hidden sm:flex gap-4 justify-center w-full px-4">
            <Motion
              v-for="(category, index) in categories.slice(3, 7)"
              :key="category.name"
              :initial="{ opacity: 0, scale: 0.95, y: 20 }"
              :animate="{ opacity: 1, scale: 1, y: 0 }"
              :transition="{ duration: 0.7, ease: 'easeOut', delay: 1.3 + index * 0.15 }"
              :while-hover="{ scale: 1.05, y: -4, transition: { duration: 0.2 } }"
              :while-tap="{ scale: 0.95, transition: { duration: 0.1 } }"
              :in-view="{ opacity: 1, scale: 1, y: 0 }"
              :viewport="{ once: true, amount: 0.5 }"
              class="flex items-center bg-white cursor-pointer p-1 pl-4 pr-4 gap-2 rounded-full shadow-sm hover:shadow-md transition-all duration-200"
            >
              <div class="hover:scale-110 transition-transform duration-200">
                <img
                  :src="category.image"
                  :alt="category.name"
                  class="w-10 h-10 object-cover rounded-full"
                />
              </div>
              <span
                class="text-gray-800 font-medium whitespace-nowrap hover:text-black transition-colors duration-200"
              >
                {{ category.name }}
              </span>
            </Motion>
          </div>

          <div class="hidden sm:flex gap-6 justify-center w-full px-12">
            <Motion
              v-for="(category, index) in categories.slice(7)"
              :key="category.name"
              :initial="{ opacity: 0, scale: 0.95, y: 20 }"
              :animate="{ opacity: 1, scale: 1, y: 0 }"
              :transition="{ duration: 0.7, ease: 'easeOut', delay: 1.7 + index * 0.15 }"
              :while-hover="{ scale: 1.05, y: -4, transition: { duration: 0.2 } }"
              :while-tap="{ scale: 0.95, transition: { duration: 0.1 } }"
              :in-view="{ opacity: 1, scale: 1, y: 0 }"
              :viewport="{ once: true, amount: 0.5 }"
              class="flex items-center bg-white cursor-pointer p-1 pl-4 pr-4 gap-2 rounded-full shadow-sm hover:shadow-md transition-all duration-200"
            >
              <div class="hover:scale-110 transition-transform duration-200">
                <img
                  :src="category.image"
                  :alt="category.name"
                  class="w-10 h-10 object-cover rounded-full"
                />
              </div>
              <span
                class="text-gray-800 font-medium whitespace-nowrap hover:text-black transition-colors duration-200"
              >
                {{ category.name }}
              </span>
            </Motion>
          </div>

          <div class="flex sm:hidden gap-3 justify-center w-full">
            <Motion
              v-for="(category, index) in categories.slice(0, 3)"
              :key="category.name"
              :initial="{ opacity: 0, scale: 0.95, y: 20 }"
              :animate="{ opacity: 1, scale: 1, y: 0 }"
              :transition="{ duration: 0.7, ease: 'easeOut', delay: 1 + index * 0.15 }"
              :while-hover="{ scale: 1.05, y: -4, transition: { duration: 0.2 } }"
              :while-tap="{ scale: 0.95, transition: { duration: 0.1 } }"
              :in-view="{ opacity: 1, scale: 1, y: 0 }"
              :viewport="{ once: true, amount: 0.5 }"
              class="flex items-center bg-white cursor-pointer p-0.5 pl-2 pr-2 gap-1.5 rounded-full shadow-sm hover:shadow-md transition-all duration-200"
            >
              <div class="hover:scale-110 transition-transform duration-200">
                <img
                  :src="category.image"
                  :alt="category.name"
                  class="w-6 h-6 object-cover rounded-full"
                />
              </div>
              <span
                class="text-gray-800 font-medium text-[0.75rem] whitespace-nowrap hover:text-black transition-colors duration-200"
              >
                {{ category.name }}
              </span>
            </Motion>
          </div>

          <div class="flex sm:hidden gap-3 justify-center w-full">
            <Motion
              v-for="(category, index) in categories.slice(3, 5)"
              :key="category.name"
              :initial="{ opacity: 0, scale: 0.95, y: 20 }"
              :animate="{ opacity: 1, scale: 1, y: 0 }"
              :transition="{ duration: 0.7, ease: 'easeOut', delay: 1.3 + index * 0.15 }"
              :while-hover="{ scale: 1.05, y: -4, transition: { duration: 0.2 } }"
              :while-tap="{ scale: 0.95, transition: { duration: 0.1 } }"
              :in-view="{ opacity: 1, scale: 1, y: 0 }"
              :viewport="{ once: true, amount: 0.5 }"
              class="flex items-center bg-white cursor-pointer p-0.5 pl-2 pr-2 gap-1.5 rounded-full shadow-sm hover:shadow-md transition-all duration-200"
            >
              <div class="hover:scale-110 transition-transform duration-200">
                <img
                  :src="category.image"
                  :alt="category.name"
                  class="w-6 h-6 object-cover rounded-full"
                />
              </div>
              <span
                class="text-gray-800 font-medium text-[0.75rem] whitespace-nowrap hover:text-black transition-colors duration-200"
              >
                {{ category.name }}
              </span>
            </Motion>
          </div>

          <div class="flex sm:hidden gap-3 justify-center w-full">
            <Motion
              v-for="(category, index) in categories.slice(5, 8)"
              :key="category.name"
              :initial="{ opacity: 0, scale: 0.95, y: 20 }"
              :animate="{ opacity: 1, scale: 1, y: 0 }"
              :transition="{ duration: 0.7, ease: 'easeOut', delay: 1.5 + index * 0.15 }"
              :while-hover="{ scale: 1.05, y: -4, transition: { duration: 0.2 } }"
              :while-tap="{ scale: 0.95, transition: { duration: 0.1 } }"
              :in-view="{ opacity: 1, scale: 1, y: 0 }"
              :viewport="{ once: true, amount: 0.5 }"
              class="flex items-center bg-white cursor-pointer p-0.5 pl-2 pr-2 gap-1.5 rounded-full shadow-sm hover:shadow-md transition-all duration-200"
            >
              <div class="hover:scale-110 transition-transform duration-200">
                <img
                  :src="category.image"
                  :alt="category.name"
                  class="w-6 h-6 object-cover rounded-full"
                />
              </div>
              <span
                class="text-gray-800 font-medium text-[0.75rem] whitespace-nowrap hover:text-black transition-colors duration-200"
              >
                {{ category.name }}
              </span>
            </Motion>
          </div>

          <div class="flex sm:hidden gap-3 justify-center w-full">
            <Motion
              v-for="(category, index) in categories.slice(8)"
              :key="category.name"
              :initial="{ opacity: 0, scale: 0.95, y: 20 }"
              :animate="{ opacity: 1, scale: 1, y: 0 }"
              :transition="{ duration: 0.7, ease: 'easeOut', delay: 1.7 + index * 0.15 }"
              :while-hover="{ scale: 1.05, y: -4, transition: { duration: 0.2 } }"
              :while-tap="{ scale: 0.95, transition: { duration: 0.1 } }"
              :in-view="{ opacity: 1, scale: 1, y: 0 }"
              :viewport="{ once: true, amount: 0.5 }"
              class="flex items-center bg-white cursor-pointer p-0.5 pl-2 pr-2 gap-1.5 rounded-full shadow-sm hover:shadow-md transition-all duration-200"
            >
              <div class="hover:scale-110 transition-transform duration-200">
                <img
                  :src="category.image"
                  :alt="category.name"
                  class="w-6 h-6 object-cover rounded-full"
                />
              </div>
              <span
                class="text-gray-800 font-medium text-[0.75rem] whitespace-nowrap hover:text-black transition-colors duration-200"
              >
                {{ category.name }}
              </span>
            </Motion>
          </div>
        </div>
      </div>

      <div
        class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-4 sm:gap-6 lg:gap-8 mt-16 sm:mt-24 lg:mt-36 mb-16 sm:mb-24 lg:mb-72"
      >
        <Motion
          :initial="{ opacity: 0, y: 20 }"
          :in-view="{ opacity: 1, y: 0 }"
          :viewport="{ once: true, amount: 0.5 }"
          :transition="{ duration: 0.7, ease: 'easeOut' }"
          class="flex flex-col gap-4"
        >
          <div
            class="h-48 sm:h-56 rounded-3xl shadow-lg relative overflow-hidden bg-cover bg-center bg-no-repeat"
            style="
              background-image: url('https://images.unsplash.com/photo-1483721310020-03333e577078?q=80&w=3000&auto=format&fit=crop');
            "
          >
            <span class="absolute bottom-4 left-4 text-white font-medium z-10">Sportwear</span>
            <div class="absolute inset-0 bg-black/20" />
          </div>

          <div class="bg-[#4a4a4a] rounded-3xl p-4 flex items-center gap-4 min-h-16 sm:h-20">
            <div class="flex-shrink-0">
              <img
                src="https://images.unsplash.com/photo-1534528741775-53994a69daeb?q=80&w=3276&auto=format&fit=crop"
                alt="Avatar"
                class="w-12 h-12 rounded-xl object-cover"
              />
            </div>
            <div class="flex flex-col gap-1">
              <div
                class="text-sm text-gray-300 font-medium bg-white/10 px-3 py-0.5 rounded-xl inline-block w-fit"
              >
                24 July 10:00 PM
              </div>
              <div class="text-white text-lg font-semibold">Outfit trends of 2025</div>
            </div>
          </div>
        </Motion>

        <Motion
          :initial="{ opacity: 0, y: 20 }"
          :in-view="{ opacity: 1, y: 0 }"
          :viewport="{ once: true, amount: 0.5 }"
          :transition="{ duration: 0.7, ease: 'easeOut', delay: 0.2 }"
          class="relative overflow-hidden rounded-3xl p-4 sm:p-6 h-64 sm:h-80 flex flex-col self-end"
        >
          <div
            class="absolute inset-0 bg-cover bg-center bg-no-repeat"
            style="
              background-image: url('https://plus.unsplash.com/premium_photo-1685311281414-85d0ce8c5981?q=80&w=4740&auto=format&fit=crop');
            "
          />
          <div class="absolute inset-0 bg-black/40 backdrop-blur-sm" />
          <div class="relative z-10">
            <div class="flex items-center text-white/90 text-sm">
              <Icon
                name="lucide:calendar"
                class="w-4 h-4 mr-2 text-white/90"
              />
              upcoming session
            </div>
            <div class="flex items-center justify-between text-white font-medium mt-auto">
              <span>Indie style</span>
              <button
                class="bg-white rounded-full p-2 flex items-center justify-center transition-all duration-300 hover:bg-white/90 hover:translate-x-1 hover:scale-110 group"
              >
                <Icon
                  name="lucide:arrow-right"
                  class="w-4 h-4 text-gray-800 group-hover:translate-x-0.5 transition-transform duration-300"
                />
              </button>
            </div>
          </div>
        </Motion>

        <Motion
          :initial="{ opacity: 0, y: 20 }"
          :in-view="{ opacity: 1, y: 0 }"
          :viewport="{ once: true, amount: 0.5 }"
          :transition="{ duration: 0.7, ease: 'easeOut', delay: 0.4 }"
          class="bg-cover bg-center bg-no-repeat rounded-3xl overflow-hidden relative h-64 sm:h-auto"
          style="
            background-image: url('https://images.unsplash.com/photo-1616453616483-9d9ccfd830c4?q=80&w=2309&auto=format&fit=crop');
          "
        >
          <div class="absolute inset-0 bg-white/80 backdrop-blur-sm" />
          <div class="relative z-10 flex flex-col justify-center items-center gap-8 p-8 h-full">
            <p class="text-2xl font-medium leading-relaxed text-center text-gray-800">
              " We believe that style is<br />
              not just about clothing "
            </p>
            <div class="flex justify-center gap-2 mt-auto">
              <button
                class="w-10 h-10 rounded-full bg-white border border-gray-200 flex items-center justify-center cursor-pointer transition-all duration-300 hover:bg-gray-50 hover:border-gray-300 hover:scale-110 group"
              >
                <Icon
                  name="lucide:chevron-left"
                  class="group-hover:-translate-x-0.5 transition-transform duration-300"
                />
              </button>
              <button
                class="w-10 h-10 rounded-full bg-white border border-gray-200 flex items-center justify-center cursor-pointer transition-all duration-300 hover:bg-gray-50 hover:border-gray-300 hover:scale-110 group"
              >
                <Icon
                  name="lucide:chevron-right"
                  class="group-hover:translate-x-0.5 transition-transform duration-300"
                />
              </button>
            </div>
          </div>
        </Motion>

        <Motion
          :initial="{ opacity: 0, y: 20 }"
          :in-view="{ opacity: 1, y: 0 }"
          :viewport="{ once: true, amount: 0.5 }"
          :transition="{ duration: 0.7, ease: 'easeOut', delay: 0.6 }"
          class="bg-cover bg-center bg-no-repeat rounded-3xl shadow-lg relative overflow-hidden h-64 sm:h-[32rem] w-full self-end"
          style="
            background-image: url('https://images.unsplash.com/photo-1515886657613-9f3515b0c78f?q=80&w=2362&auto=format&fit=crop');
          "
        >
          <div class="absolute inset-0 bg-black/10" />
        </Motion>
      </div>
    </main>
  </div>
</template>

<script setup lang="ts">
const categories = [
  {
    name: 'Fairy',
    image:
      'https://images.unsplash.com/photo-1562572159-4efc207f5aff?q=80&w=300&auto=format&fit=crop',
  },
  {
    name: 'Retro',
    image:
      'https://images.unsplash.com/photo-1445633629932-0029acc44e88?q=80&w=300&auto=format&fit=crop',
  },
  {
    name: 'Reworked',
    image:
      'https://images.unsplash.com/photo-1490481651871-ab68de25d43d?q=80&w=300&auto=format&fit=crop',
  },
  {
    name: 'Handmade',
    image:
      'https://images.unsplash.com/photo-1589451359791-f9c33af92239?q=80&w=300&auto=format&fit=crop',
  },
  {
    name: 'Indie',
    image:
      'https://images.unsplash.com/photo-1529139574466-a303027c1d8b?q=80&w=300&auto=format&fit=crop',
  },
  {
    name: 'Techwear',
    image:
      'https://images.unsplash.com/photo-1483721310020-03333e577078?q=80&w=300&auto=format&fit=crop',
  },
  {
    name: 'Glam',
    image:
      'https://images.unsplash.com/photo-1596993100471-c3905dafa78e?q=80&w=300&auto=format&fit=crop',
  },
  {
    name: 'Casual',
    image:
      'https://images.unsplash.com/photo-1515886657613-9f3515b0c78f?q=80&w=300&auto=format&fit=crop',
  },
  {
    name: 'Elegant',
    image:
      'https://images.unsplash.com/photo-1490725263030-1f0521cec8ec?q=80&w=300&auto=format&fit=crop',
  },
  {
    name: 'Streetwear',
    image:
      'https://images.unsplash.com/photo-1509631179647-0177331693ae?q=80&w=300&auto=format&fit=crop',
  },
]
</script>
