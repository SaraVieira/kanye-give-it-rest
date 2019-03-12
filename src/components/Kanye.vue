<template>
  <div class="hello">
    <h2>{{ quote || "Getting them quote" }}</h2>
    <button @click="this.getQuote">Random</button>
  </div>
</template>

<script>
import axios from "axios";

export default {
  name: "Kanye",
  data() {
    return {
      quote: ""
    };
  },
  methods: {
    async getQuote() {
      this.quote = "";
      const { data } = await axios.get("https://api.kanye.rest");

      this.quote = data.quote;
    }
  },
  async mounted() {
    this.getQuote();
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
h2 {
  margin: 40px 0;
  font-weight: normal;
}
button {
  background: #71a0a5;
  border: mone;
  color: white;
  appearance: none;
  padding: 12px 18px;
  font-size: 24px;
  font-weight: bold;
  border-radius: 4px;
  box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);

  &:hover {
    box-shadow: 0 2px 5px rgba(0, 0, 0, 0.3);
    background: #638b8e;
  }
}
</style>
