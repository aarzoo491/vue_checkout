<template>
  <div class="checkout-container">
    <div class="checkout-box">
      <h2>Checkout</h2>
      <p class="subtitle">Complete your purchase securely</p>

      <form @submit.prevent="submitPayment">
        <div class="form-group">
          <label for="email">Email Address</label>
          <input
            id="email"
            v-model="email"
            type="email"
            placeholder="Enter your email address"
            required
            class="form-input"
          />
        </div>

        <div class="form-group">
          <label for="amount">Amount (USD)</label>
          <input
            id="amount"
            v-model="amount"
            type="number"
            placeholder="Enter amount"
            min="0.01"
            step="0.01"
            required
            class="form-input"
          />
        </div>

        <button
          type="submit"
          :disabled="loading"
          class="btn-submit"
        >
          {{ loading ? 'Processing...' : 'Submit Payment' }}
        </button>
      </form>

      <p v-if="message" class="msg" :class="messageType">
        {{ message }}
      </p>

      <div class="payment-info">
        <p>✓ Secure payment processing</p>
        <p>✓ 100% encrypted transaction</p>
        <p>✓ Money-back guarantee</p>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue'
import axios from 'axios'

const email = ref('')
const amount = ref('')
const loading = ref(false)
const message = ref('')
const messageType = ref('')

const submitPayment = async () => {
  if (!email.value || !amount.value) {
    message.value = 'Please fill in all fields'
    messageType.value = 'error'
    return
  }

  loading.value = true
  message.value = ''
  messageType.value = ''

  try {
    const response = await axios.post(
      "/.netlify/functions/pay-now",
      {
        email: email.value,
        amount: amount.value
      }
    );

    message.value = response.data?.message || 'Payment submitted successfully!'
    messageType.value = 'success'

    email.value = ''
    amount.value = ''
  } catch (error: any) {
    message.value = error.response?.data?.message || 'Something went wrong. Please try again.'
    messageType.value = 'error'
  } finally {
    loading.value = false
  }
}
</script>

<style scoped>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

.checkout-container {
  min-height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  padding: 20px;
}

.checkout-box {
  background: white;
  padding: 50px;
  border-radius: 10px;
  box-shadow: 0 10px 40px rgba(0, 0, 0, 0.2);
  max-width: 450px;
  width: 100%;
}

.checkout-box h2 {
  font-size: 32px;
  font-weight: 700;
  margin-bottom: 10px;
  color: #1a1a1a;
  text-align: center;
}

.subtitle {
  text-align: center;
  color: #666;
  margin-bottom: 30px;
  font-size: 15px;
}

form {
  margin-bottom: 30px;
}

.form-group {
  margin-bottom: 25px;
}

.form-group label {
  display: block;
  font-size: 15px;
  font-weight: 600;
  color: #1a1a1a;
  margin-bottom: 8px;
}

.form-input {
  width: 100%;
  padding: 12px 15px;
  font-size: 15px;
  border: 1px solid #ddd;
  border-radius: 6px;
  transition: all 0.3s ease;
  font-family: inherit;
}

.form-input:focus {
  outline: none;
  border-color: #667eea;
  box-shadow: 0 0 0 3px rgba(102, 126, 234, 0.1);
}

.btn-submit {
  width: 100%;
  padding: 14px;
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  color: white;
  border: none;
  border-radius: 6px;
  font-size: 16px;
  font-weight: 600;
  cursor: pointer;
  transition: all 0.3s ease;
}

.btn-submit:hover:not(:disabled) {
  transform: translateY(-2px);
  box-shadow: 0 8px 20px rgba(102, 126, 234, 0.3);
}

.btn-submit:disabled {
  opacity: 0.7;
  cursor: not-allowed;
}

.msg {
  padding: 15px;
  border-radius: 6px;
  text-align: center;
  margin-top: 20px;
  font-size: 15px;
}

.msg.success {
  background-color: #d4edda;
  color: #155724;
  border: 1px solid #c3e6cb;
}

.msg.error {
  background-color: #f8d7da;
  color: #721c24;
  border: 1px solid #f5c6cb;
}

.payment-info {
  margin-top: 30px;
  padding-top: 20px;
  border-top: 1px solid #eee;
  text-align: center;
}

.payment-info p {
  font-size: 14px;
  color: #666;
  margin: 8px 0;
}

.payment-info p::before {
  color: #28a745;
  margin-right: 5px;
}

@media (max-width: 480px) {
  .checkout-box {
    padding: 30px 20px;
  }

  .checkout-box h2 {
    font-size: 24px;
  }

  .form-group {
    margin-bottom: 20px;
  }

  .btn-submit {
    padding: 12px;
    font-size: 15px;
  }
}
</style>
