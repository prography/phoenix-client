<template>
  <v-container>
    <v-layout row wrap>
      <v-flex md4 sm6 xs12>
        <v-card>
          <v-card-title class="headline pb-0">Profile</v-card-title>
          <v-card-text>
            <v-text-field type="email" label="Email" prepend-icon="email"/>
            <v-text-field type="password" label="Password" prepend-icon="lock"/>
          </v-card-text>
          <v-card-actions>
            <v-spacer/>
            <v-btn color="primary" flat>save</v-btn>
          </v-card-actions>
        </v-card>
      </v-flex>
    </v-layout>
  </v-container>
</template>
