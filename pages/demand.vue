<template>
  <v-container>
    <h1>수요조사 폼</h1>
    <v-container grid-list-sm fluid>
      <v-layout row wrap>
        <v-flex v-for="img in productImages" :key="img" xs4 d-flex>
          <v-card flat tile class="d-flex">
            <v-img :src="img" :lazy-src="img" aspect-ratio="1" class="grey lighten-2">
              <template v-slot:placeholder>
                <v-layout fill-height align-center justify-center ma-0>
                  <v-progress-circular indeterminate color="grey lighten-5"></v-progress-circular>
                </v-layout>
              </template>
            </v-img>
          </v-card>
        </v-flex>
      </v-layout>
    </v-container>
    <v-layout row wrap>
      <v-flex sm6 xs12>
        <v-text-field label="수요조사 기간"/>
        <v-data-table :headers="headers" :items="products">
          <template v-slot:items="props">
            <td>{{ props.item.name }}</td>
            <td>{{ props.item.price }}</td>
            <td>
              <v-edit-dialog
                :return-value.sync="props.item.amount"
                large
                lazy
                persistent
                @save="save"
                @cancel="cancel"
                @open="open"
                @close="close"
              >
                <div>{{ props.item.amount }}</div>
                <template v-slot:input>
                  <div class="mt-3 title">Amount</div>
                </template>
                <template v-slot:input>
                  <v-text-field
                    v-model="props.item.amount"
                    label="Edit"
                    single-line
                    counter
                    autofocus
                  ></v-text-field>
                </template>
              </v-edit-dialog>
            </td>
          </template>
        </v-data-table>

        <v-snackbar v-model="snack" :timeout="3000" :color="snackColor">
          {{ snackText }}
          <v-btn flat @click="snack = false">Close</v-btn>
        </v-snackbar>
        <v-text-field label="알림 받을 곳(E-mail)"/>
        <v-text-field label="트위터 계정 (선택)"/>
        <v-textarea label="이거 사실거에요?(선택)"/>
        <v-btn color="primary">제출</v-btn>
      </v-flex>
    </v-layout>
  </v-container>
</template>

<script>
export default {
  data() {
    return {
      productImages: ['https://picsum.photos/400', 'https://picsum.photos/400', 'https://picsum.photos/400'],
      headers: [
        { text: 'Name', value: 'name' },
        { text: 'Price', value: 'price' },
        { text: 'Amount', value: 'amount' }
      ],
      products: [
        {
          name: 'A',
          price: 1000,
          amount: 0
        },
        {
          name: 'A',
          price: 1000,
          amount: 0
        },
        {
          name: 'A',
          price: 1000,
          amount: 0
        }
      ]
    }
  }
}
</script>