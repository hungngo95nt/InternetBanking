<template>
  <div>
    <label for="message">Tin nhắn</label>
    <textarea
      id="message"
      name="message"
      autocomplete="off"
      class="my-custom my-text-area"
      @keyup="handleChange($event)"
      :value="getDataSendingMyMessage"
    />
  </div>
</template>

<script>
import { mapGetters } from "vuex";
export default {
  props: ["data"],
  data() {
    return {
      value: ""
    };
  },
  methods: {
    handleChange(event) {
      this.$store.dispatch('updateDataSendingMyMessage', event.target.value);
    }
  },
  computed: {
    ...mapGetters(["getDataSendingMyMessage"])
  }
};
</script>

<style scoped src="@/assets/css/send_money_page.css"></style>