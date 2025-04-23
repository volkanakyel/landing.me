<template>
  <div class="absolute inset-0 overflow-hidden pointer-events-none">
    <svg
      class="w-full h-full"
      viewBox="0 0 100 100"
      xmlns="http://www.w3.org/2000/svg"
    >
      <!-- Running Shoe Print Pattern Definition -->
      <defs>
        <path
          id="shoePrint"
          d="M10,0 c1,0 2,0.5 3,1 c1.5,0.5 3,0 4,-0.5 c1,-0.5 2,0 3,0.5 c1,0.5 2,0 3,-0.5 c0.5,1 0,2 -0.5,3 l-0.5,2 l1,1 l-0.5,2 l1,1 l-0.5,2 l1,1 l-1,3 l-1,2 l-2,2 l-2,1 l-2,0 l-2,-1 l-2,-2 l-1,-2 c-0.5,-1 0,-2 0.5,-3 l0.5,-2 l-1,-1 l0.5,-2 l-1,-1 l0.5,-2 l-1,-1 l1,-2 c0.5,-1 1,-1.5 2,-1.5 z M10,7.5 l1.5,1.5 l-3,0 l1.5,-1.5 M10,11 l2,2 l-4,0 l2,-2 M10,15 l2.5,2.5 l-5,0 l2.5,-2.5 M10,20 l2,2 l-4,0 l2,-2 M10,25 l3,3 l-6,0 l3,-3"
          fill="#333333"
          fill-opacity="0.15"
        />
      </defs>

      <!-- Scattered Shoe Prints -->
      <g class="prints-group">
        <use
          href="#shoePrint"
          transform="translate(10,10) rotate(30) scale(2)"
        />
        <use
          href="#shoePrint"
          transform="translate(30,15) rotate(-15) scale(2)"
        />
        <use
          href="#shoePrint"
          transform="translate(50,20) rotate(45) scale(2)"
        />
        <use
          href="#shoePrint"
          transform="translate(70,25) rotate(-30) scale(2)"
        />
        <use
          href="#shoePrint"
          transform="translate(20,40) rotate(15) scale(2)"
        />
        <use
          href="#shoePrint"
          transform="translate(40,45) rotate(-45) scale(2)"
        />
        <use
          href="#shoePrint"
          transform="translate(60,50) rotate(20) scale(2)"
        />
        <use
          href="#shoePrint"
          transform="translate(15,30) rotate(35) scale(2)"
        />
        <use
          href="#shoePrint"
          transform="translate(15,20) rotate(-20) scale(2)"
        />
        <use
          href="#shoePrint"
          transform="translate(35,25) rotate(25) scale(2)"
        />
        <use
          href="#shoePrint"
          transform="translate(55,30) rotate(-35) scale(2)"
        />
        <use
          href="#shoePrint"
          transform="translate(75,35) rotate(40) scale(2)"
        />
        <use
          href="#shoePrint"
          transform="translate(25,60) rotate(-10) scale(2)"
        />
        <use
          href="#shoePrint"
          transform="translate(45,65) rotate(35) scale(2)"
        />
        <use
          href="#shoePrint"
          transform="translate(25,45) rotate(25) scale(2)"
        />
        <use
          href="#shoePrint"
          transform="translate(55,50) rotate(-30) scale(2)"
        />
        <use
          href="#shoePrint"
          transform="translate(20,30) rotate(10) scale(2)"
        />
        <use
          href="#shoePrint"
          transform="translate(40,35) rotate(-30) scale(2)"
        />
        <use
          href="#shoePrint"
          transform="translate(60,40) rotate(25) scale(2)"
        />
        <use
          href="#shoePrint"
          transform="translate(80,45) rotate(-15) scale(2)"
        />
        <use
          href="#shoePrint"
          transform="translate(30,70) rotate(30) scale(2)"
        />
        <use
          href="#shoePrint"
          transform="translate(50,75) rotate(-20) scale(2)"
        />
        <use
          href="#shoePrint"
          transform="translate(35,55) rotate(20) scale(2)"
        />
        <use
          href="#shoePrint"
          transform="translate(65,60) rotate(-35) scale(2)"
        />
      </g>
    </svg>
  </div>
</template>

<style scoped>
.prints-group {
  opacity: 0.15;
}

.prints-group use {
  transform-origin: center;
}
</style>
