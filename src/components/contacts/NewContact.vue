<template>
  <div>
    <h2>Nuevo contato</h2>
    <v-form v-model="valid">
      <v-container>
        <v-row>
          <v-col cols="12" md="3">
            <v-text-field
              v-model="name"
              :rules="nameRules"
              :counter="10"
              label="Name"
              required
            ></v-text-field>
          </v-col>

          <v-col cols="12" md="3">
            <v-text-field
              v-model="email"
              :rules="emailRules"
              :counter="10"
              label="Email"
              required
            ></v-text-field>
          </v-col>

          <v-col cols="12" md="3">
            <v-text-field
              v-model="phone"
              :counter="10"
              label="Phone"
              required
            ></v-text-field>
          </v-col>

          <v-col cols="12" md="3">
            <v-checkbox v-model="isFavorite" label="Favorito"></v-checkbox>
          </v-col>
          <v-col cols="12" md="3">
            <v-btn @click="save" depressed elevation="2" plain raised tile
              >Enviar</v-btn
            >
          </v-col>
        </v-row>
      </v-container>
    </v-form>
  </div>
</template>

<script>
export default {
  data: () => ({
    valid: false,
    name: "",
    nameRules: [
      (v) => !!v || "Name is required",
      (v) => v.length <= 10 || "Name must be less than 10 characters",
    ],
    email: "",
    emailRules: [(v) => !!v || "E-mail is required"],
    phone: "",
    isFavorite: false
  }),
  methods: {
    save() {
      const newItem = {
        name: this.name,
        email: this.email,
        phone: this.phone,
        isFavorite: this.isFavorite
      }
      this.$emit("guardado", newItem);
    },
  },
};
</script>