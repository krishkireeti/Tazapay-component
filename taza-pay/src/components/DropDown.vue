<template>
  <div class="dropdown">
   <v-select
    v-model="dropdown_langs_ids"
    :options=" dropdown_langs"
    label="name"
    multiple
    placeholder="Select"
    class="payment_methods__select2"
    :reduce="(dropdown_lang) => dropdown_lang.id">
   </v-select>
  </div>
</template>

<script>
import vSelect from "vue-select";
import "vue-select/dist/vue-select.css";
export default {
  name: "DropDown",
  components: {
    vSelect,
  },

  data() {
    return {
      dropdown_langs: [
        {
          id: 1,
          name: "Javascript",
        },
        {
          id: 2,
          name: "C++",
        },
        {
          id: 3,
          name: "Python",
        },
        {
          id: 4,
          name: "Ruby",
        },
        {
          id: 5,
          name: "PHP",
        },
        {
          id: 6,
          name: "Pascal",
        },
      ],
      dropdown_langs_ids: [],
    };
  },
};
</script>
