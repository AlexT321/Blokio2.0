<template>
  <div
    class="absolute bottom-0 left-4 h-64 w-44 rounded-xl bg-zinc-600 flex flex-col justify-start items-center gap-5 pt-4"
    :style="{display: chat_overlay_vis}"
  >
    <div class="h-20 w-32 flex flex-col justify-start gap-1">
      <h2 class="text-white">Chat Size</h2>
      <div
        class="h-11 w-32 bg-zinc-500 flex justify-center items-center gap-2 rounded-xl"
      >
        <button
          class="h-10 w-10 rounded-full bg-zinc-400 text-white hover:bg-zinc-300"
        >
          +
        </button>
        <button
          class="h-10 w-10 rounded-full bg-zinc-400 text-white hover:bg-zinc-300"
        >
          -
        </button>
      </div>
    </div>
    <div class="h-10 w-40 flex flex-row justify-center items-center gap-2">
      <div class="h-10 w-10 bg-zinc-500 flex justify-center items-center">
        <svg
          class="w-8 h-8 fill-zinc-400"
          xmlns="http://www.w3.org/2000/svg"
          viewBox="0 0 232.322 232.322"
          xmlns:v="https://vecta.io/nano"
        >
          <path
            d="M224.822 23.935H7.5a7.5 7.5 0 0 0-7.5 7.5v169.451a7.5 7.5 0 0 0 7.5 7.5h217.322a7.5 7.5 0 0 0 7.5-7.5V31.435a7.5 7.5 0 0 0-7.5-7.5zm-7.5 15.001v143.091l-59.995-63.799a7.5 7.5 0 0 0-5.462-2.362c-2.069 0-4.045.855-5.463 2.36l-25.62 27.227-34.349-45.291a7.5 7.5 0 0 0-11.959.01L15 178.861V38.936h202.322zm-9.907 154.451H22.824l57.643-76.269 33.722 44.465a7.5 7.5 0 0 0 5.578 2.957c2.201.11 4.348-.742 5.86-2.35l26.234-27.879 55.554 59.076zm-52.178-91.705c13.597 0 24.658-11.061 24.658-24.656s-11.061-24.658-24.658-24.658-24.656 11.062-24.656 24.658 11.061 24.656 24.656 24.656zm0-34.315a9.67 9.67 0 0 1 9.658 9.658 9.67 9.67 0 0 1-9.658 9.656 9.67 9.67 0 0 1-9.656-9.656 9.67 9.67 0 0 1 9.656-9.658z"
          />
        </svg>
      </div>
      <button
        class="h-10 w-28 bg-zinc-500 flex justify-center items-center text-white hover:bg-zinc-400"
      >
        Upload image
      </button>
    </div>
    <div class="h-10 w-36 flex flex-row justify-center items-center gap-2">
      <button
        class="h-10 w-10 rounded-full bg-zinc-500 text-white flex justify-center items-center text-lg hover:bg-zinc-400"
      >
        +
      </button>
      <p class="text-white">Invite to Chat</p>
    </div>
  </div>
</template>

<script lang="ts">
import { overlayVisibility } from '~~/store';
import { mapState } from 'pinia';

const store = overlayVisibility();

export default {
  name: "Chat_overlay",
  computed: {
    ...mapState(overlayVisibility, ['chat_overlay_vis'])
  }
};
</script>

<style scoped></style>