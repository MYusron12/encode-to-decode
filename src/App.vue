<template>
  <nav class="navbar bg-body-tertiary">
    <div class="container">
      <a class="navbar-brand" href="#">
        Encode Decode
      </a>
    </div>
  </nav>
  <div class="container mt-5">
    <div class="row">
      <div class="col-6">
        <div class="mb-3">
          <label for="basic-url" class="form-label">Form Encode</label>
          <div class="input-group mb-3">
            <input type="text" class="form-control" v-model="inputEncode" placeholder="Form Encode" aria-label="Recipient's username" aria-describedby="button-addon2">
            <button class="btn btn-outline-secondary" type="button" id="button-addon2" @click="encodeText">Encode</button>
          </div>
          <div class="form-text" id="basic-addon4" v-if="encodedText">{{ encodedText }}</div>
        </div>
      </div>
      <div class="col-6">
        <div class="mb-3">
          <label for="basic-url" class="form-label">Form Decode</label>
          <div class="input-group mb-3">
            <input type="text" class="form-control" v-model="inputDecode" placeholder="Form Decode" aria-label="Recipient's username" aria-describedby="button-addon2">
            <button class="btn btn-outline-secondary" type="button" id="button-addon2" @click="decodeText">Button</button>
          </div>
          <div class="form-text" id="basic-addon4" v-if="decodedText">{{ decodedText }}</div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      inputEncode: "",
      inputDecode: "",
      encodedText: "",
      decodedText: ""
    };
  },
  methods: {
    encodeText() {
      this.encodedText = btoa(this.inputEncode);
    },
    decodeText() {
      this.decodedText = atob(this.inputDecode);
    }
  }
};
</script>

<style scoped>
/* Styling specific to this component */
</style>
