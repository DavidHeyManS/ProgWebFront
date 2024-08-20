
<template>
  <div class="preferences-page">
    <h2>User Preferences</h2>
    <form @submit.prevent="savePreferences">
      <div class="input-group">
        <label for="userName">Name</label>
        <input type="text" v-model="preferences.name" id="userName" required />
      </div>
      <div class="input-group">
        <label for="userEmail">Email</label>
        <input type="email" v-model="preferences.email" id="userEmail" required />
      </div>
      <div class="input-group">
        <label for="userPassword">Password</label>
        <input type="password" v-model="preferences.password" id="userPassword" />
      </div>
      <button type="submit" class="save-btn">Save Changes</button>
    </form>
  </div>
</template>

<script>
export default {
  name: 'PreferencesPage',
  data() {
    return {
      preferences: {
        name: '',
        email: '',
        password: ''
      }
    };
  },
  methods: {
    savePreferences() {
      // Logic for saving user preferences
      if (this.preferences.name && this.preferences.email) {
        // Save user preferences
      } else {
        alert('Name and email are required fields');
      }
    }
  }
}
</script>

<style scoped>
.preferences-page {
  max-width: 500px;
  margin: 0 auto;
  padding: 20px;
  background-color: #f0f0f0;
  border-radius: 8px;
  box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
}
.input-group {
  margin-bottom: 20px;
}
.save-btn {
  width: 100%;
  padding: 10px;
  background-color: #007bff;
  color: white;
  border: none;
  border-radius: 5px;
  cursor: pointer;
}
</style>
