<template>
  <div class="example-app">
    <!-- Header Section -->
    <header class="example-header">
      <h1 class="heading-2">My App with Design System</h1>
      <p class="body-lg">This template shows how to use the design system components and tokens.</p>
    </header>

    <!-- Form Section -->
    <section class="example-section">
      <h2 class="heading-3">User Registration</h2>
      <form class="example-form" @submit.prevent="handleSubmit">
        <DSBoxInput 
          size="large"
          label="Full Name"
          description="Enter your first and last name"
          v-model="form.name"
        />
        
        <DSBoxInput 
          size="medium"
          label="Email"
          sideLabel="Required"
          v-model="form.email"
        />
        
        <DSBoxInput 
          size="small"
          label="Phone (Optional)"
          v-model="form.phone"
        />

        <div class="form-actions">
          <DSButton 
            variant="primary" 
            size="large" 
            type="submit"
            :disabled="!isFormValid"
          >
            Create Account
          </DSButton>
          
          <DSButton 
            variant="secondary" 
            size="large"
            @click="resetForm"
          >
            Reset
          </DSButton>
        </div>
      </form>
    </section>

    <!-- Cards Section -->
    <section class="example-section">
      <h2 class="heading-3">Feature Cards</h2>
      <div class="cards-grid">
        <div class="feature-card">
          <h3 class="heading-4">Design Tokens</h3>
          <p class="body-sm">Consistent colors, spacing, and typography across your app.</p>
          <DSButton variant="primary" size="small">
            Learn More
          </DSButton>
        </div>
        
        <div class="feature-card feature-card--highlighted">
          <h3 class="heading-4">Vue Components</h3>
          <p class="body-sm">Reusable, accessible components built with Vue 3.</p>
          <DSButton variant="secondary" size="small">
            Get Started
          </DSButton>
        </div>
        
        <div class="feature-card">
          <h3 class="heading-4">TypeScript</h3>
          <p class="body-sm">Full type safety and better developer experience.</p>
          <DSButton variant="primary" size="small">
            Explore
          </DSButton>
        </div>
      </div>
    </section>

    <!-- Status Messages -->
    <section class="example-section">
      <h2 class="heading-3">Status Messages</h2>
      <div class="status-messages">
        <div class="status-message status-message--success">
          <span class="subhead">Success!</span>
          <span class="body-sm">Your account has been created successfully.</span>
        </div>
        
        <div class="status-message status-message--warning">
          <span class="subhead">Warning</span>
          <span class="body-sm">Please verify your email address.</span>
        </div>
        
        <div class="status-message status-message--alert">
          <span class="subhead">Alert</span>
          <span class="body-sm">Your session will expire in 5 minutes.</span>
        </div>
      </div>
    </section>
  </div>
</template>

<script setup lang="ts">
import { ref, computed } from 'vue'
// Import your design system components
import DSButton from '@/design-system/components/DSButton.vue'
import DSBoxInput from '@/design-system/components/DSBoxInput.vue'

// Reactive form data
const form = ref({
  name: '',
  email: '',
  phone: ''
})

// Computed properties
const isFormValid = computed(() => {
  return form.value.name.length > 0 && form.value.email.includes('@')
})

// Methods
const handleSubmit = () => {
  console.log('Form submitted:', form.value)
  // Handle form submission
}

const resetForm = () => {
  form.value = {
    name: '',
    email: '',
    phone: ''
  }
}
</script>

<style scoped>
/* Import your design system styles first */
/* 
@import './design-system/styles/tokens.css';
@import './design-system/styles/typography.css';
@import './design-system/styles/button.css';
@import './design-system/styles/inputs.css';
@import './design-system/styles/grid.css';
@import './design-system/styles/spacing.css';
@import './design-system/styles/global.css';
*/

.example-app {
  max-width: 1200px;
  margin: 0 auto;
  padding: var(--space-lg);
}

.example-header {
  text-align: center;
  margin-bottom: var(--space-xl);
  padding: var(--space-lg);
  background: var(--neutral-95);
  border-radius: var(--border-radius-lg);
}

.example-section {
  margin-bottom: var(--space-xl);
  padding: var(--space-lg);
  border: 1px solid var(--neutral-90);
  border-radius: var(--border-radius-md);
  background: var(--neutral-100);
}

.example-form {
  display: flex;
  flex-direction: column;
  gap: var(--space-md);
  max-width: 500px;
}

.form-actions {
  display: flex;
  gap: var(--space-sm);
  margin-top: var(--space-md);
}

.cards-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
  gap: var(--space-md);
  margin-top: var(--space-md);
}

.feature-card {
  padding: var(--space-md);
  border: 1px solid var(--neutral-85);
  border-radius: var(--border-radius-md);
  background: var(--neutral-100);
  box-shadow: var(--shadow-level-1);
  transition: transform 0.2s ease, box-shadow 0.2s ease;
}

.feature-card:hover {
  transform: translateY(-2px);
  box-shadow: var(--shadow-level-2);
}

.feature-card--highlighted {
  border-color: var(--primary-60);
  background: var(--primary-90);
}

.feature-card h3 {
  margin-bottom: var(--space-xs);
  color: var(--neutral-20);
}

.feature-card p {
  margin-bottom: var(--space-sm);
  color: var(--neutral-40);
}

.status-messages {
  display: flex;
  flex-direction: column;
  gap: var(--space-sm);
  margin-top: var(--space-md);
}

.status-message {
  display: flex;
  align-items: center;
  gap: var(--space-sm);
  padding: var(--space-sm);
  border-radius: var(--border-radius-sm);
  border-left: 4px solid;
}

.status-message--success {
  background: var(--primary-90);
  border-left-color: var(--primary-60);
}

.status-message--warning {
  background: var(--warning-90);
  border-left-color: var(--warning-50);
}

.status-message--alert {
  background: var(--alert-90);
  border-left-color: var(--alert-70);
}

/* Responsive adjustments */
@media (max-width: 768px) {
  .example-app {
    padding: var(--space-md);
  }
  
  .form-actions {
    flex-direction: column;
  }
  
  .cards-grid {
    grid-template-columns: 1fr;
  }
}
</style> 