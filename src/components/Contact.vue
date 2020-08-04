<template>
  <div class="contact">
    <div class="contact__header">
      <p class="contact__title title">
        <span class="highlight">Contact</span>
        Me
      </p>
      <p
        class="contact__description"
      >Got a burning qustion? Fill in the form below, and I will respond back as quickly as possible.</p>
    </div>
    <form v-on:submit.prevent="onSubmit">
      <input
        v-model="contact.name"
        type="text"
        id="nameksljf"
        name="nameksljf"
        placeholder="Name:"
        required
        maxlength="100"
      />
      <input
        v-model="contact.email"
        type="email"
        id="emaillkjkl"
        name="emaillkjkl"
        placeholder="Email:"
        required
      />
      <textarea
        v-model="contact.message"
        type="text"
        id="messageksljf"
        name="messageksljf"
        placeholder="Message:"
        required
        maxlength="250"
      ></textarea>
      <input type="submit" value="Send" />
      <!-- ohnohoney -->
      <input
        v-model="contact.ohnohoney"
        class="ohnohoney"
        autocomplete="off"
        type="text"
        id="ohnohoney"
        name="ohnohoney"
      />
    </form>
  </div>
</template>

<script>
export default {
  name: "Contact",
  data: () => {
    return {
      contact: {},
    };
  },
  methods: {
    onSubmit: function () {
      console.log(this.contact);
    },
  },
};
</script>

<style scoped lang="scss">
.contact {
  &__header {
    margin-bottom: 2.5rem;
    text-align: center;
  }
  padding: 0 2.5rem;
}
</style>