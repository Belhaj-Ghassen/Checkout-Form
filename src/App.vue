<script>
export default {
  data() {
    return {
      form: {
        firstName: '',
        lastName: '',
        username: '',
        email: '',
        address: '',
        country: '',
        state: '',
        zip: ''
      }
    }
  },
  methods: {
    submitForm() {
      alert('Form submitted!')
      console.log(this.form)
    }
  }
}
</script>

<template>
  <div class="checkout-form">
    <h2>HTML5 Validation with VueJs</h2>
    <form @submit.prevent="submitForm">
      <div class="form-group">
        <div class="form-field">
          <label for="firstName">First Name</label>
          <input v-model="form.firstName" type="text" id="firstName" required />
        </div>
        <div class="form-field">
          <label for="lastName">Last name</label>
          <input v-model="form.lastName" type="text" id="lastName" required />
        </div>
      </div>
      <div>
        <label for="username">Username</label>
        <div class="input-group">
          <span style="color: black">@</span>
          <input v-model="form.username" type="text" id="username" required />
        </div>
      </div>
      <div>
        <label for="email">Email (Optional)</label>
        <input v-model="form.email" type="email" id="email" />
      </div>
      <div>
        <label for="adress">Adress</label>
        <input v-model="form.adress" type="text" name="" id="adress" required />
      </div>
      <div class="form-group">
        <div class="form-field">
          <label for="country">Country</label>
          <select v-model="form.country" id="country" required>
            <option disabled value="">Choose...</option>
            <option>Tunisia</option>
            <option>Algeria</option>
            <option>Morroco</option>
            <option>Other</option>
          </select>
        </div>
        <div class="form-field">
          <label for="state">State</label>
          <select v-model="form.state" id="state" required>
            <option disabled value="">Choose...</option>
            <option>Medenine</option>
            <option>Sousse</option>
            <option>Wahran</option>
            <option>Other</option>
          </select>
        </div>
        <div class="form-field">
          <label for="zip">Zip</label>
          <input v-model="form.zip" type="text" id="zip" required />
        </div>
      </div>
      <button type="submit">Continue to checkout</button>
    </form>
  </div>
</template>

<style scoped>
.checkout-form {
  max-width: 600px;
  margin: auto;
  padding: 2em;
  background-color: #42b983;
  border-radius: 10px;
  position: relative;
  overflow: hidden;
}
.checkout-form h2 {
  text-align: center;
  color: white;
}
.checkout-form form {
  display: grid;
  gap: 1em;
}
.checkout-form label {
  display: block;
  margin-bottom: 0.5em;
  color: white;
}
.checkout-form input,
.checkout-form select {
  width: 100%;
  padding: 0.5em;
  border: 1px solid #ccc;
  border-radius: 5px;
  box-sizing: border-box;
}
.checkout-form .input-group {
  display: flex;
  align-items: center;
}
.checkout-form .input-group span {
  padding: 0.5em;
  background: #eee;
  border: 1px solid #ccc;
  border-right: 0;
  border-radius: 5px 0 0 5px;
}
.checkout-form .input-group input {
  flex: 1;
  border-radius: 0 5px 5px 0;
}
.checkout-form .form-group {
  display: flex;
  gap: 1em;
}
.checkout-form .form-field {
  flex: 1;
}
.checkout-form button {
  width: 100%;
  padding: 1em;
  background: #35495e;
  color: white;
  border: none;
  border-radius: 5px;
  cursor: pointer;
  transition: background 0.3s;
}
.checkout-form button:hover {
  background: #2c3e50;
}
</style>
