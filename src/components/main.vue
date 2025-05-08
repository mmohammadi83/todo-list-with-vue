<script setup>
import { ref } from "vue";
import navbar from "./navbar.vue";
let notes = ref([
  "In veniam nostrud est velit anim irure do aute ullamco nostrud. Nostrud sunt mollit aute officia consequat et laborum proident. In minim id dolor nulla culpa occaecat anim id ex mollit id. Voluptate tempor nostrud aute laborum culpa ea amet sunt exercitation nostrud. Et commodo sint irure occaecat occaecat nisi et pariatur. Pariatur veniam enim qui id tempor labore aute consequat minim dolore amet deserunt.",
]);
</script>
<template>
  <navbar />
  <div class="search_box">
    <input type="text" placeholder="shearch" />
    <button>
      <svg
        xmlns="http://www.w3.org/2000/svg"
        width="35"
        height="35"
        viewBox="0 0 24 24"
      >
        <path
          fill="none"
          stroke="#007200ff"
          stroke-linecap="round"
          stroke-linejoin="round"
          stroke-width="2"
          d="M3 10a7 7 0 1 0 14 0a7 7 0 1 0-14 0m18 11l-6-6"
        />
      </svg>
    </button>
  </div>
  <div class="body">
    <div class="notes_menu">
      <div v-for="note of notes" class="note">
        <div class="text">
          {{ note }}
        </div>
        <div class="button_box">
          <button class="butt edit">
            <svg
              xmlns="http://www.w3.org/2000/svg"
              width="40"
              height="40"
              viewBox="0 0 24 24"
            >
              <path
                fill="none"
                stroke="#055705"
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="1.3"
                d="m5 16l-1 4l4-1L19.586 7.414a2 2 0 0 0 0-2.828l-.172-.172a2 2 0 0 0-2.828 0zM15 6l3 3m-5 11h8"
              />
            </svg>
          </button>
          <button class="butt delete">
            <svg
              xmlns="http://www.w3.org/2000/svg"
              width="40"
              height="40"
              viewBox="0 0 24 24"
            >
              <path
                fill="#FF0000"
                d="M7.616 20q-.667 0-1.141-.475T6 18.386V6h-.5q-.213 0-.356-.144T5 5.499t.144-.356T5.5 5H9q0-.31.23-.54t.54-.23h4.46q.31 0 .54.23T15 5h3.5q.213 0 .356.144t.144.357t-.144.356T18.5 6H18v12.385q0 .666-.475 1.14t-1.14.475zM17 6H7v12.385q0 .269.173.442t.443.173h8.769q.269 0 .442-.173t.173-.442zm-6.692 11q.213 0 .357-.144t.143-.356v-8q0-.213-.144-.356T10.307 8t-.356.144t-.143.356v8q0 .213.144.356q.144.144.356.144m3.385 0q.213 0 .356-.144t.143-.356v-8q0-.213-.144-.356Q13.904 8 13.692 8q-.213 0-.357.144t-.143.356v8q0 .213.144.356t.357.144M7 6v13z"
              />
            </svg>
          </button>
        </div>
      </div>
    </div>
  </div>
</template>
