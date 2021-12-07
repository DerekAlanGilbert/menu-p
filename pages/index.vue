<template>
  <div class="w-screen h-full">
    <div class="w-full py-4 text-center bg-gray-200">
      <h1 class="text-3xl">Title Of Company</h1>
    </div>
    <div class="w-auto mt-4">
      <h2 class="pl-4 text-xl">Specials</h2>
      <ul class="flex flex-row w-full space-x-2 overflow-y-scroll">
        <li
          v-for="(item, index) in 5"
          :key="index"
          style="min-width: 22rem"
          class="h-56 text-blue-900 bg-blue-400 rounded-lg shadow-lg"
        >
          <div class="p-4">
            {{ item }}
          </div>
        </li>
      </ul>
    </div>
    <div class="w-auto mt-4">
      <h2 class="pl-4 text-xl">Menu</h2>
      <div class="space-y-2">
        <div
          v-for="(menuItem, index) in menuItems"
          :key="index"
          class="flex flex-col"
        >
          <Disclosure>
            <DisclosureButton class="w-full p-4 text-blue-900 bg-blue-400">
              <h1>{{ menuItem.name }}</h1>
            </DisclosureButton>
            <DisclosurePanel class="py-4 text-center text-gray-500">
              <a
                target="_bank"
                href="http://www.facebook.com/share.php?u= 14947 s ox cart lane"
              >
                post to facebook
              </a>
              {{ '<-------- menu items go here -------->' }}
            </DisclosurePanel>
          </Disclosure>
        </div>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import { Disclosure, DisclosureButton, DisclosurePanel } from '@headlessui/vue'
const menuItems = [
  { name: 'Appetizers' },

  { name: 'Entrees' },
  { name: 'Desserts' },
  { name: 'Drinks' },
]
export default {
  components: {
    Disclosure,
    DisclosureButton,
    DisclosurePanel,
  },
  data() {
    return {
      menuItems,
    }
  },
}
</script>
