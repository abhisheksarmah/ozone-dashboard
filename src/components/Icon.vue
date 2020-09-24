<template>
  <svg
    v-if="name == 'hamburger'"
    xmlns="http://www.w3.org/2000/svg"
    class="text-gray-600"
    width="24"
    height="24"
    viewBox="0 0 24 24"
    stroke-width="2"
    stroke="currentColor"
    fill="none"
    stroke-linecap="round"
    stroke-linejoin="round"
  >
    <rect x="0" y="0" width="24" height="24" stroke="none"></rect>
    <line x1="4" y1="6" x2="20" y2="6" />
    <line x1="4" y1="12" x2="20" y2="12" />
    <line x1="4" y1="18" x2="20" y2="18" />
  </svg>
  <svg
    v-else-if="name == 'dashboard'"
    xmlns="http://www.w3.org/2000/svg"
    width="24"
    height="24"
    viewBox="0 0 24 24"
    stroke-width="2"
    stroke="currentColor"
    fill="none"
    stroke-linecap="round"
    stroke-linejoin="round"
  >
    <rect x="0" y="0" width="24" height="24" stroke="none"></rect>
    <rect x="4" y="4" width="6" height="6" rx="1" />
    <rect x="14" y="4" width="6" height="6" rx="1" />
    <rect x="4" y="14" width="6" height="6" rx="1" />
    <rect x="14" y="14" width="6" height="6" rx="1" />
  </svg>
  <svg
    v-else-if="name == 'analytics'"
    xmlns="http://www.w3.org/2000/svg"
    width="24"
    height="24"
    viewBox="0 0 24 24"
    stroke-width="2"
    stroke="currentColor"
    fill="none"
    stroke-linecap="round"
    stroke-linejoin="round"
  >
    <rect x="0" y="0" width="24" height="24" stroke="none"></rect>
    <line x1="4" y1="19" x2="20" y2="19" />
    <polyline points="4 15 8 9 12 11 16 6 20 10" />
  </svg>
  <svg
    v-else-if="name == 'invoice'"
    xmlns="http://www.w3.org/2000/svg"
    width="24"
    height="24"
    viewBox="0 0 24 24"
    stroke-width="2"
    stroke="currentColor"
    fill="none"
    stroke-linecap="round"
    stroke-linejoin="round"
  >
    <rect x="0" y="0" width="24" height="24" stroke="none"></rect>
    <polyline points="14 3 14 8 19 8" />
    <path
      d="M17 21H7a2 2 0 0 1 -2 -2V5a2 2 0 0 1 2 -2h7l5 5v11a2 2 0 0 1 -2 2z"
    />
    <line x1="9" y1="9" x2="10" y2="9" />
    <line x1="9" y1="13" x2="15" y2="13" />
    <line x1="9" y1="17" x2="15" y2="17" />
  </svg>
  <svg
    v-else-if="name == 'tracking'"
    xmlns="http://www.w3.org/2000/svg"
    width="24"
    height="24"
    viewBox="0 0 24 24"
    stroke-width="2"
    stroke="currentColor"
    fill="none"
    stroke-linecap="round"
    stroke-linejoin="round"
  >
    <rect x="0" y="0" width="24" height="24" stroke="none"></rect>
    <circle cx="12" cy="12" r="9" />
    <polyline points="12 7 12 12 9 15" />
  </svg>
  <svg
    v-else-if="name == 'history'"
    xmlns="http://www.w3.org/2000/svg"
    width="24"
    height="24"
    viewBox="0 0 24 24"
    stroke-width="2"
    stroke="currentColor"
    fill="none"
    stroke-linecap="round"
    stroke-linejoin="round"
  >
    <rect x="0" y="0" width="24" height="24" stroke="none"></rect>
    <path
      d="M16 6h3a 1 1 0 011 1v11a2 2 0 0 1 -4 0v-13a1 1 0 0 0 -1 -1h-10a1 1 0 0 0 -1 1v12a3 3 0 0 0 3 3h11"
    />
    <line x1="8" y1="8" x2="12" y2="8" />
    <line x1="8" y1="12" x2="12" y2="12" />
    <line x1="8" y1="16" x2="12" y2="16" />
  </svg>
  <svg
    v-else-if="name == 'settings'"
    xmlns="http://www.w3.org/2000/svg"
    width="24"
    height="24"
    viewBox="0 0 24 24"
    stroke-width="2"
    stroke="currentColor"
    fill="none"
    stroke-linecap="round"
    stroke-linejoin="round"
  >
    <rect x="0" y="0" width="24" height="24" stroke="none"></rect>
    <path
      d="M10.325 4.317c.426-1.756 2.924-1.756 3.35 0a1.724 1.724 0 0 0 2.573 1.066c1.543-.94 3.31.826 2.37 2.37a1.724 1.724 0 0 0 1.065 2.572c1.756.426 1.756 2.924 0 3.35a1.724 1.724 0 0 0 -1.066 2.573c.94 1.543-.826 3.31-2.37 2.37a1.724 1.724 0 0 0 -2.572 1.065c-.426 1.756-2.924 1.756-3.35 0a1.724 1.724 0 0 0 -2.573 -1.066c-1.543.94-3.31-.826-2.37-2.37a1.724 1.724 0 0 0 -1.065 -2.572c-1.756-.426-1.756-2.924 0-3.35a1.724 1.724 0 0 0 1.066 -2.573c-.94-1.543.826-3.31 2.37-2.37.996.608 2.296.07 2.572-1.065z"
    />
    <circle cx="12" cy="12" r="3" />
  </svg>
  <svg
    v-else-if="name == 'alert'"
    xmlns="http://www.w3.org/2000/svg"
    width="24"
    height="24"
    viewBox="0 0 24 24"
    stroke-width="2"
    stroke="currentColor"
    fill="none"
    stroke-linecap="round"
    stroke-linejoin="round"
  >
    <rect x="0" y="0" width="24" height="24" stroke="none"></rect>
    <path
      d="M10 5a2 2 0 0 1 4 0a7 7 0 0 1 4 6v3a4 4 0 0 0 2 3h-16a4 4 0 0 0 2 -3v-3a7 7 0 0 1 4 -6"
    />
    <path d="M9 17v1a3 3 0 0 0 6 0v-1" />
  </svg>
  <svg
    v-else-if="name == 'world'"
    xmlns="http://www.w3.org/2000/svg"
    width="24"
    height="24"
    class="icon icon-tabler icon-tabler-world"
    viewBox="0 0 24 24"
    stroke-width="2"
    stroke="currentColor"
    fill="none"
    stroke-linecap="round"
    stroke-linejoin="round"
  >
    <rect x="0" y="0" width="24" height="24" stroke="none"></rect>
    <circle cx="12" cy="12" r="9"></circle>
    <line x1="3" y1="12" x2="21" y2="12"></line>
    <path d="M12 3a12 12 0 0 0 0 18"></path>
    <path d="M12 3a12 12 0 0 1 0 18"></path>
  </svg>
</template>

<script>
export default {
  props: ["name"],
};
</script>

<style lang="scss" scoped></style>
