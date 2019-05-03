<template>
  <v-container grid-list-md>
    <v-layout row wrap>
      <v-flex v-for="product in products" :key="product.id" md3 sm4 xs6>
        <v-card flat>
          <v-img src="https://picsum.photos/400"/>
          <v-card-title>
            <div>
              <span class="grey--text">category</span>
              <br>
              <span>Lorem ipsum</span>
              <br>
              <span>₩1,000</span>
            </div>
          </v-card-title>
          <v-card-actions>
            <v-spacer></v-spacer>
            <v-btn icon>
              <v-icon>favorite</v-icon>
            </v-btn>
            <v-btn icon>
              <v-icon>share</v-icon>
            </v-btn>
          </v-card-actions>
        </v-card>
      </v-flex>
    </v-layout>
  </v-container>
</template>

<script>
export default {
  data() {
    return {
      products: [
        { text: 'item1' },
        { text: 'item1' },
        { text: 'item1' },
        { text: 'item1' },
        { text: 'item1' },
        { text: 'item1' },
        { text: 'item1' },
        { text: 'item1' },
        { text: 'item1' },
        { text: 'item1' },
        { text: 'item1' },
        { text: 'item1' },
        { text: 'item1' }
      ]
    }
  }
}
</script>
