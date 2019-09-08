<template>
  <div id="app">
    <div class="container">
      <section class="grid area-selected">
        <label
          class="btn selected"
          v-for="selectedCurrency in selectedCurrencies"
          :key="selectedCurrency"
        >
          <input
            type="checkbox"
            name="currency"
            :value="selectedCurrency"
            v-model="selectedCurrencies"
          />{{ selectedCurrency }}
          <span></span>
        </label>
      </section>
      <section class="grid">
        <label
          class="btn myCheckbox"
          v-for="currency in currencies"
          :key="currency"
        >
          <input
            type="checkbox"
            name="currency"
            :value="currency"
            v-model="selectedCurrencies"
          />{{ currency }}
          <span></span>
        </label>
      </section>
    </div>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      currencies: [
        "EUR",
        "PLN",
        "GEL",
        "DKK",
        "CZK",
        "GBP",
        "SEK",
        "USD",
        "RUB"
      ],
      selectedCurrencies: [],
    };
  },
};
</script>

<style lang="scss">
@import "./styles/style.scss";
</style>
