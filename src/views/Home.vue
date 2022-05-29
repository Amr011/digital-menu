<script>
import socialMedia from '../components/social-media.vue'
import Header from '../components/header.vue'
import Footer from '../components/footer.vue'
import category from '../components/category.vue'
import item from '../components/item.vue'
export default {
  name: 'Home',
  components: { socialMedia, Header, category, item, Footer },

  data() {
    return {
      categories: 4,
      items: 4,
      data: {
        data: [
          {
            id: 1,
            title: 'Coffee And Green Tea Category',
            item: [
              {
                title: 'Coffee And Green Tea Category',
                price: 24,
                currency: '$',
                description:
                  'Coffee And Green Tea Category Tea Category Tea Category Tea Category Tea Category Tea Category Tea Category ',
              },
              {
                title: 'Coffee And Green Tea Category',
                price: 24,
                currency: '$',
                description:
                  'Coffee And Green Tea Category Tea Category Tea Category Tea Category Tea Category Tea Category Tea Category ',
              },
              {
                title: 'Coffee And Green Tea Category',
                price: 24,
                currency: '$',
                description:
                  'Coffee And Green Tea Category Tea Category Tea Category Tea Category Tea Category Tea Category Tea Category ',
              },
            ],
          },
          {
            id: 1,
            title: 'Coffee And Green Tea Category',
            item: [
              {
                title: 'Coffee And Green Tea Category',
                price: 30,
                currency: '$',
                description:
                  'Coffee And Green Tea Category Tea Category Tea Category Tea Category Tea Category Tea Category Tea Category ',
              },
              {
                title: 'Coffee And Green Tea Category',
                price: 24,
                currency: '$',
                description:
                  'Coffee And Green Tea Category Tea Category Tea Category Tea Category Tea Category Tea Category Tea Category ',
              },
              {
                title: 'Coffee And Green Tea Category',
                price: 24,
                currency: '$',
                description:
                  'Coffee And Green Tea Category Tea Category Tea Category Tea Category Tea Category Tea Category Tea Category ',
              },
              {
                title: 'Coffee And Green Tea Category',
                price: 12,
                currency: '$',
                description: 'Coffee And GreeTea Category Tea Category ',
              },
              {
                title: 'Coffee And Green Green Green Green Green Green Tea Category',
                price: 2400,
                currency: '$',
                description: 'Coffee And GreeTea Category Tea Category ',
              },
            ],
          },
          {
            id: 1,
            title: ' And Green Tea Category',
            item: [
              {
                title: 'HHHHHHH Coffee And Green Tea Category',
                price: 18,
                currency: '$',
                description:
                  'Coffee And Green Tea Category Tea Category Tea Category Tea Category Tea Category Tea Category Tea Category ',
              },
              {
                title: 'Coffee And Green Tea Category',
                price: 24,
                currency: '$',
                description:
                  'Coffee And Green Tea Category Tea Category Tea Category Tea Category Tea Category Tea Category Tea Category ',
              },
              {
                title: 'Coffee And Green Tea Category',
                price: 24,
                currency: '$',
                description: 'Coffee And GreeTea Category Tea Category ',
              },
            ],
          },
        ],
      },
    }
  },
}
</script>

<template>
  <div class="container mx-auto flex justify-center">
    <!-- Header Start -->
    <div class="py-6">
      <div class="bg-white py-4">
        <Header />
        <!-- Social Media Start -->
        <socialMedia />
      </div>

      <div class="container">
        <div class="my-6">
          <!-- Menu Category Item -->
          <div v-for="category in data.data" :key="category">
            <category :title="category.title" class="" />
            <div
              class="mb-2 grid max-w-4xl grid-cols-1 items-start gap-4 md:grid-cols-2 lg:grid-cols-2 xl:grid-cols-2"
            >
              <item
                v-for="item in category.item"
                :key="item"
                :title="item.title"
                :price="item.price"
                :currency="item.currency"
                :description="item.description"
              />
            </div>
            <hr class="mx-2 my-4 border-gray-300" />
          </div>
        </div>
      </div>
      <Footer />
    </div>
  </div>
</template>
<style></style>
