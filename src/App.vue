<template>
  <div class="app">
    <header class="app-header">
      <h1 class="heading-1">Vue Design System</h1>
      <p class="body-lg">A comprehensive design system with all foundations and components</p>
    </header>

    <nav class="app-nav">
      <a href="#colors" class="nav-link">Colors</a>
      <a href="#typography" class="nav-link">Typography</a>
      <a href="#spacing" class="nav-link">Spacing</a>
      <a href="#borders" class="nav-link">Borders & Shading</a>
      <a href="#components" class="nav-link">Components</a>
    </nav>

    <main class="app-main">
      <!-- Colors Section -->
      <section id="colors" class="demo-section">
        <h2 class="heading-2">Color System</h2>
        <p class="body-lg">Our color system is organized into distinct categories: Primary Colors, Neutral Colors, Secondary Neutrals, Tertiary Neutrals, and Feedback Colors.</p>
        
        <div class="color-section">
          <h3 class="heading-4">Primary Colors</h3>
          <div class="color-grid">
            <div class="color-item">
              <div class="color-swatch" style="background-color: var(--primary-90);"></div>
              <div class="color-info">
                <div class="color-name">Primary 90</div>
                <div class="color-value">#EAF5DC</div>
              </div>
            </div>
            <div class="color-item">
              <div class="color-swatch" style="background-color: var(--primary-60);"></div>
              <div class="color-info">
                <div class="color-name">Primary 60</div>
                <div class="color-value">#62A60A</div>
              </div>
            </div>
            <div class="color-item">
              <div class="color-swatch" style="background-color: var(--primary-55);"></div>
              <div class="color-info">
                <div class="color-name">Primary 55</div>
                <div class="color-value">#5C9C08</div>
              </div>
            </div>
            <div class="color-item">
              <div class="color-swatch" style="background-color: var(--primary-50);"></div>
              <div class="color-info">
                <div class="color-name">Primary 50</div>
                <div class="color-value">#3E850D</div>
              </div>
            </div>
            <div class="color-item">
              <div class="color-swatch" style="background-color: var(--primary-40);"></div>
              <div class="color-info">
                <div class="color-name">Primary 40</div>
                <div class="color-value">#326B00</div>
              </div>
            </div>
          </div>
        </div>

        <div class="color-section">
          <h3 class="heading-4">Neutral Colors</h3>
          <div class="color-grid">
            <div class="color-item">
              <div class="color-swatch" style="background-color: var(--neutral-100); border: 1px solid var(--neutral-85);"></div>
              <div class="color-info">
                <div class="color-name">Neutral 100</div>
                <div class="color-value">#FFFFFF</div>
              </div>
            </div>
            <div class="color-item">
              <div class="color-swatch" style="background-color: var(--neutral-95);"></div>
              <div class="color-info">
                <div class="color-name">Neutral 95</div>
                <div class="color-value">#F4F5F7</div>
              </div>
            </div>
            <div class="color-item">
              <div class="color-swatch" style="background-color: var(--neutral-90);"></div>
              <div class="color-info">
                <div class="color-name">Neutral 90</div>
                <div class="color-value">#E8E9EB</div>
              </div>
            </div>
            <div class="color-item">
              <div class="color-swatch" style="background-color: var(--neutral-85);"></div>
              <div class="color-info">
                <div class="color-name">Neutral 85</div>
                <div class="color-value">#D4D7D9</div>
              </div>
            </div>
            <div class="color-item">
              <div class="color-swatch" style="background-color: var(--neutral-80);"></div>
              <div class="color-info">
                <div class="color-name">Neutral 80</div>
                <div class="color-value">#BCBFC2</div>
              </div>
            </div>
            <div class="color-item">
              <div class="color-swatch" style="background-color: var(--neutral-70);"></div>
              <div class="color-info">
                <div class="color-name">Neutral 70</div>
                <div class="color-value">#A2A6A8</div>
              </div>
            </div>
            <div class="color-item">
              <div class="color-swatch" style="background-color: var(--neutral-40);"></div>
              <div class="color-info">
                <div class="color-name">Neutral 40</div>
                <div class="color-value">#666B70</div>
              </div>
            </div>
            <div class="color-item">
              <div class="color-swatch" style="background-color: var(--neutral-20);"></div>
              <div class="color-info">
                <div class="color-name">Neutral 20</div>
                <div class="color-value">#313D47</div>
              </div>
            </div>
            <div class="color-item">
              <div class="color-swatch" style="background-color: var(--neutral-0);"></div>
              <div class="color-info">
                <div class="color-name">Neutral 0</div>
                <div class="color-value">#242C33</div>
              </div>
            </div>
          </div>
        </div>

        <div class="color-section">
          <h3 class="heading-4">Accent Colors</h3>
          <div class="color-grid">
            <div class="color-item">
              <div class="color-swatch" style="background-color: var(--accent-90);"></div>
              <div class="color-info">
                <div class="color-name">Accent 90</div>
                <div class="color-value">#E3F2FD</div>
              </div>
            </div>
            <div class="color-item">
              <div class="color-swatch" style="background-color: var(--accent-85);"></div>
              <div class="color-info">
                <div class="color-name">Accent 85</div>
                <div class="color-value">#BBDEFB</div>
              </div>
            </div>
            <div class="color-item">
              <div class="color-swatch" style="background-color: var(--accent-80);"></div>
              <div class="color-info">
                <div class="color-name">Accent 80</div>
                <div class="color-value">#90CAF9</div>
              </div>
            </div>
            <div class="color-item">
              <div class="color-swatch" style="background-color: var(--accent-60);"></div>
              <div class="color-info">
                <div class="color-name">Accent 60</div>
                <div class="color-value">#2196F3</div>
              </div>
            </div>
            <div class="color-item">
              <div class="color-swatch" style="background-color: var(--accent-40);"></div>
              <div class="color-info">
                <div class="color-name">Accent 40</div>
                <div class="color-value">#1976D2</div>
              </div>
            </div>
            <div class="color-item">
              <div class="color-swatch" style="background-color: var(--accent-30);"></div>
              <div class="color-info">
                <div class="color-name">Accent 30</div>
                <div class="color-value">#0D47A1</div>
              </div>
            </div>
          </div>
        </div>

        <div class="color-section">
          <h3 class="heading-4">Secondary Neutral Colors</h3>
          <div class="color-grid">
            <div class="color-item">
              <div class="color-swatch" style="background-color: var(--secondary-neutral-95);"></div>
              <div class="color-info">
                <div class="color-name">Secondary Neutral 95</div>
                <div class="color-value">#F5F4F3</div>
              </div>
            </div>
            <div class="color-item">
              <div class="color-swatch" style="background-color: var(--secondary-neutral-90);"></div>
              <div class="color-info">
                <div class="color-name">Secondary Neutral 90</div>
                <div class="color-value">#EEECEA</div>
              </div>
            </div>
            <div class="color-item">
              <div class="color-swatch" style="background-color: var(--secondary-neutral-85);"></div>
              <div class="color-info">
                <div class="color-name">Secondary Neutral 85</div>
                <div class="color-value">#DAD6D3</div>
              </div>
            </div>
            <div class="color-item">
              <div class="color-swatch" style="background-color: var(--secondary-neutral-80);"></div>
              <div class="color-info">
                <div class="color-name">Secondary Neutral 80</div>
                <div class="color-value">#BDB7B3</div>
              </div>
            </div>
            <div class="color-item">
              <div class="color-swatch" style="background-color: var(--secondary-neutral-70);"></div>
              <div class="color-info">
                <div class="color-name">Secondary Neutral 70</div>
                <div class="color-value">#A39A93</div>
              </div>
            </div>
            <div class="color-item">
              <div class="color-swatch" style="background-color: var(--secondary-neutral-40);"></div>
              <div class="color-info">
                <div class="color-name">Secondary Neutral 40</div>
                <div class="color-value">#85776F</div>
              </div>
            </div>
          </div>
        </div>

        <div class="color-section">
          <h3 class="heading-4">Tertiary Neutral Colors</h3>
          <div class="color-grid">
            <div class="color-item">
              <div class="color-swatch" style="background-color: var(--tertiary-neutral-95);"></div>
              <div class="color-info">
                <div class="color-name">Tertiary Neutral 95</div>
                <div class="color-value">#FAF9F5</div>
              </div>
            </div>
            <div class="color-item">
              <div class="color-swatch" style="background-color: var(--tertiary-neutral-90);"></div>
              <div class="color-info">
                <div class="color-name">Tertiary Neutral 90</div>
                <div class="color-value">#F5F1E9</div>
              </div>
            </div>
            <div class="color-item">
              <div class="color-swatch" style="background-color: var(--tertiary-neutral-85);"></div>
              <div class="color-info">
                <div class="color-name">Tertiary Neutral 85</div>
                <div class="color-value">#F0E9DA</div>
              </div>
            </div>
            <div class="color-item">
              <div class="color-swatch" style="background-color: var(--tertiary-neutral-80);"></div>
              <div class="color-info">
                <div class="color-name">Tertiary Neutral 80</div>
                <div class="color-value">#EBDDB9</div>
              </div>
            </div>
            <div class="color-item">
              <div class="color-swatch" style="background-color: var(--tertiary-neutral-70);"></div>
              <div class="color-info">
                <div class="color-name">Tertiary Neutral 70</div>
                <div class="color-value">#E1D0A5</div>
              </div>
            </div>
          </div>
        </div>

        <div class="color-section">
          <h3 class="heading-4">Feedback Colors</h3>
          <div class="feedback-colors">
            <div class="feedback-group">
              <h4 class="heading-5">Warning Colors</h4>
              <div class="color-grid">
                <div class="color-item">
                  <div class="color-swatch" style="background-color: var(--warning-90);"></div>
                  <div class="color-info">
                    <div class="color-name">Warning 90</div>
                    <div class="color-value">#FFEBEC</div>
                  </div>
                </div>
                <div class="color-item">
                  <div class="color-swatch" style="background-color: var(--warning-50);"></div>
                  <div class="color-info">
                    <div class="color-name">Warning 50</div>
                    <div class="color-value">#F42434</div>
                  </div>
                </div>
                <div class="color-item">
                  <div class="color-swatch" style="background-color: var(--warning-40);"></div>
                  <div class="color-info">
                    <div class="color-name">Warning 40</div>
                    <div class="color-value">#B30715</div>
                  </div>
                </div>
              </div>
            </div>

            <div class="feedback-group">
              <h4 class="heading-5">Alert Colors</h4>
              <div class="color-grid">
                <div class="color-item">
                  <div class="color-swatch" style="background-color: var(--alert-90);"></div>
                  <div class="color-info">
                    <div class="color-name">Alert 90</div>
                    <div class="color-value">#FEF6E7</div>
                  </div>
                </div>
                <div class="color-item">
                  <div class="color-swatch" style="background-color: var(--alert-80);"></div>
                  <div class="color-info">
                    <div class="color-name">Alert 80</div>
                    <div class="color-value">#FACD46</div>
                  </div>
                </div>
                <div class="color-item">
                  <div class="color-swatch" style="background-color: var(--alert-70);"></div>
                  <div class="color-info">
                    <div class="color-name">Alert 70</div>
                    <div class="color-value">#FF850D</div>
                  </div>
                </div>
                <div class="color-item">
                  <div class="color-swatch" style="background-color: var(--alert-50);"></div>
                  <div class="color-info">
                    <div class="color-name">Alert 50</div>
                    <div class="color-value">#AC6000</div>
                  </div>
                </div>
              </div>
            </div>

            <div class="feedback-group">
              <h4 class="heading-5">Accessibility Colors</h4>
              <div class="color-grid">
                <div class="color-item">
                  <div class="color-swatch" style="background-color: var(--accessibility-80);"></div>
                  <div class="color-info">
                    <div class="color-name">Accessibility 80</div>
                    <div class="color-value">#4095BF</div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </section>

      <!-- Typography Section -->
      <section id="typography" class="demo-section">
        <h2 class="heading-2">Typography System</h2>
        <p class="body-lg">Our typography system is based on the Roboto font from Google Fonts with a comprehensive scale and clear hierarchy.</p>
        
        <div class="typography-demo">
          <h3 class="heading-4">Type Scale</h3>
          <div class="type-examples">
            <div class="type-example">
              <h1 class="heading-1">Heading 1</h1>
              <div class="type-specs">64px • Light • 100% line height • -0.8px letter spacing</div>
            </div>
            <div class="type-example">
              <h2 class="heading-2">Heading 2</h2>
              <div class="type-specs">42px • Light • 120% line height • -0.4px letter spacing</div>
            </div>
            <div class="type-example">
              <h3 class="heading-3">Heading 3</h3>
              <div class="type-specs">32px • Light • 120% line height • -0.4px letter spacing</div>
            </div>
            <div class="type-example">
              <h4 class="heading-4">Heading 4</h4>
              <div class="type-specs">26px • Light • 120% line height • -0.2px letter spacing</div>
            </div>
            <div class="type-example">
              <h5 class="heading-5">Heading 5</h5>
              <div class="type-specs">22px • Light • 120% line height • 0 letter spacing</div>
            </div>
            <div class="type-example">
              <div class="subhead">Subhead Text</div>
              <div class="type-specs">18px • Bold • 140% line height • 0 letter spacing</div>
            </div>
            <div class="type-example">
              <div class="body-lg">Body Large - Perfect for paragraph content and main body text that needs to be highly readable.</div>
              <div class="type-specs">16px • Regular • 150% line height • 0 letter spacing</div>
            </div>
            <div class="type-example">
              <div class="body-sm">Body Small - Ideal for supporting content, captions, and areas where space is limited.</div>
              <div class="type-specs">14px • Regular • 150% line height • 0 letter spacing</div>
            </div>
            <div class="type-example">
              <div class="button-lg">BUTTON LARGE TEXT</div>
              <div class="type-specs">16px • Medium • 100% line height • 0.4px letter spacing</div>
            </div>
            <div class="type-example">
              <div class="button-sm">BUTTON SMALL TEXT</div>
              <div class="type-specs">14px • Medium • 100% line height • 0.2px letter spacing</div>
            </div>
            <div class="type-example">
              <div class="label">LABEL TEXT FOR FORM FIELDS</div>
              <div class="type-specs">12px • Regular • 150% line height • 0 letter spacing</div>
            </div>
          </div>
        </div>
      </section>

      <!-- Spacing Section -->
      <section id="spacing" class="demo-section">
        <h2 class="heading-2">Spacing System</h2>
        <p class="body-lg">Our spacing system provides consistent rhythm and hierarchy through standardized spacing values.</p>
        
        <div class="spacing-demo">
          <h3 class="heading-4">Spacing Scale</h3>
          <div class="spacing-examples">
            <div class="spacing-item">
              <div class="spacing-visual" style="width: 4px; height: 40px; background: var(--primary-60);"></div>
              <div class="spacing-info">
                <div class="spacing-name">Quarck</div>
                <div class="spacing-value">4px</div>
              </div>
            </div>
            <div class="spacing-item">
              <div class="spacing-visual" style="width: 8px; height: 40px; background: var(--primary-60);"></div>
              <div class="spacing-info">
                <div class="spacing-name">Nano</div>
                <div class="spacing-value">8px</div>
              </div>
            </div>
            <div class="spacing-item">
              <div class="spacing-visual" style="width: 12px; height: 40px; background: var(--primary-60);"></div>
              <div class="spacing-info">
                <div class="spacing-name">Micro</div>
                <div class="spacing-value">12px</div>
              </div>
            </div>
            <div class="spacing-item">
              <div class="spacing-visual" style="width: 16px; height: 40px; background: var(--primary-60);"></div>
              <div class="spacing-info">
                <div class="spacing-name">XXXS</div>
                <div class="spacing-value">16px</div>
              </div>
            </div>
            <div class="spacing-item">
              <div class="spacing-visual" style="width: 24px; height: 40px; background: var(--primary-60);"></div>
              <div class="spacing-info">
                <div class="spacing-name">XXS</div>
                <div class="spacing-value">24px</div>
              </div>
            </div>
            <div class="spacing-item">
              <div class="spacing-visual" style="width: 32px; height: 40px; background: var(--primary-60);"></div>
              <div class="spacing-info">
                <div class="spacing-name">XS</div>
                <div class="spacing-value">32px</div>
              </div>
            </div>
            <div class="spacing-item">
              <div class="spacing-visual" style="width: 40px; height: 40px; background: var(--primary-60);"></div>
              <div class="spacing-info">
                <div class="spacing-name">SM</div>
                <div class="spacing-value">40px</div>
              </div>
            </div>
            <div class="spacing-item">
              <div class="spacing-visual" style="width: 48px; height: 40px; background: var(--primary-60);"></div>
              <div class="spacing-info">
                <div class="spacing-name">MD</div>
                <div class="spacing-value">48px</div>
              </div>
            </div>
            <div class="spacing-item">
              <div class="spacing-visual" style="width: 56px; height: 40px; background: var(--primary-60);"></div>
              <div class="spacing-info">
                <div class="spacing-name">LG</div>
                <div class="spacing-value">56px</div>
              </div>
            </div>
            <div class="spacing-item">
              <div class="spacing-visual" style="width: 64px; height: 40px; background: var(--primary-60);"></div>
              <div class="spacing-info">
                <div class="spacing-name">XL</div>
                <div class="spacing-value">64px</div>
              </div>
            </div>
          </div>
        </div>
      </section>

      <!-- Borders & Shading Section -->
      <section id="borders" class="demo-section">
        <h2 class="heading-2">Borders & Shading</h2>
        <p class="body-lg">Visual elements that add depth, structure, and hierarchy to the interface.</p>
        
        <div class="borders-demo">
          <h3 class="heading-4">Border Radius</h3>
          <div class="border-examples">
            <div class="border-demo-item">
              <div class="border-demo-visual" style="background: var(--neutral-20); border-radius: 0;"></div>
              <div class="border-demo-name">None</div>
              <div class="border-demo-value">0px</div>
            </div>
            <div class="border-demo-item">
              <div class="border-demo-visual" style="background: var(--neutral-20); border-radius: 4px;"></div>
              <div class="border-demo-name">SM</div>
              <div class="border-demo-value">4px</div>
            </div>
            <div class="border-demo-item">
              <div class="border-demo-visual" style="background: var(--neutral-20); border-radius: 8px;"></div>
              <div class="border-demo-name">MD</div>
              <div class="border-demo-value">8px</div>
            </div>
            <div class="border-demo-item">
              <div class="border-demo-visual" style="background: var(--neutral-20); border-radius: 16px;"></div>
              <div class="border-demo-name">LG</div>
              <div class="border-demo-value">16px</div>
            </div>
            <div class="border-demo-item">
              <div class="border-demo-visual" style="background: var(--neutral-20); border-radius: 50px; width: 100px;"></div>
              <div class="border-demo-name">Pill</div>
              <div class="border-demo-value">500px</div>
            </div>
            <div class="border-demo-item">
              <div class="border-demo-visual" style="background: var(--neutral-20); border-radius: 50%;"></div>
              <div class="border-demo-name">Circular</div>
              <div class="border-demo-value">50%</div>
            </div>
          </div>

          <h3 class="heading-4">Drop Shadows</h3>
          <div class="shadow-examples">
            <div class="border-demo-item">
              <div class="border-demo-visual" style="background: white; box-shadow: 0 2px 6px rgba(0,0,0,0.2);"></div>
              <div class="border-demo-name">Level 1</div>
              <div class="border-demo-value">0 2px 6px</div>
            </div>
            <div class="border-demo-item">
              <div class="border-demo-visual" style="background: white; box-shadow: 0 8px 24px rgba(0,0,0,0.16);"></div>
              <div class="border-demo-name">Level 2</div>
              <div class="border-demo-value">0 8px 24px</div>
            </div>
            <div class="border-demo-item">
              <div class="border-demo-visual" style="background: white; box-shadow: 0 16px 32px rgba(0,0,0,0.16);"></div>
              <div class="border-demo-name">Level 3</div>
              <div class="border-demo-value">0 16px 32px</div>
            </div>
            <div class="border-demo-item">
              <div class="border-demo-visual" style="background: white; box-shadow: 0 16px 48px rgba(0,0,0,0.2);"></div>
              <div class="border-demo-name">Level 4</div>
              <div class="border-demo-value">0 16px 48px</div>
            </div>
          </div>
        </div>
      </section>

      <!-- Components Section -->
      <section id="components" class="demo-section">
        <h2 class="heading-2">Components</h2>
        <p class="body-lg">Reusable Vue components built with the design system foundations.</p>
        
        <div class="components-demo">
          <h3 class="heading-4">Buttons</h3>
          <div class="component-group">
            <div class="component-demo">
              <h4 class="heading-5">Primary Buttons</h4>
              <div class="button-examples">
                <DSButton variant="primary" size="large">Primary Large</DSButton>
                <DSButton variant="primary" size="small">Primary Small</DSButton>
                <DSButton variant="primary" size="large" :disabled="true">Disabled</DSButton>
              </div>
            </div>

            <div class="component-demo">
              <h4 class="heading-5">Secondary Buttons</h4>
              <div class="button-examples">
                <DSButton variant="secondary" size="large">Secondary Large</DSButton>
                <DSButton variant="secondary" size="small">Secondary Small</DSButton>
                <DSButton variant="secondary" size="large" :disabled="true">Disabled</DSButton>
              </div>
            </div>
          </div>

          <h3 class="heading-4">Input Components</h3>
          <div class="component-group">
            <div class="input-examples">
              <DSBoxInput size="xs" label="Extra Small Input" />
              <DSBoxInput size="small" label="Small Input" />
              <DSBoxInput size="medium" label="Medium Input" sideLabel="Side Label" />
              <DSBoxInput size="large" label="Large Input" description="This is a description for the large input" />
            </div>
          </div>
        </div>
      </section>
    </main>
  </div>
</template>

<script setup lang="ts">
import DSButton from './components/DSButton.vue'
import DSBoxInput from './components/DSBoxInput.vue'
</script>

<style scoped>
.app {
  max-width: 1200px;
  margin: 0 auto;
  padding: 2rem;
}

.app-header {
  text-align: center;
  margin-bottom: 2rem;
}

.app-nav {
  display: flex;
  justify-content: center;
  gap: 2rem;
  margin-bottom: 3rem;
  padding: 1rem;
  background: var(--neutral-95);
  border-radius: 8px;
}

.nav-link {
  color: var(--neutral-40);
  text-decoration: none;
  font-weight: var(--font-weight-medium);
  padding: 0.5rem 1rem;
  border-radius: 4px;
  transition: all 0.2s ease;
}

.nav-link:hover {
  background: var(--primary-90);
  color: var(--primary-50);
}

.app-main {
  display: flex;
  flex-direction: column;
  gap: 4rem;
}

.demo-section {
  border: 1px solid var(--neutral-90);
  border-radius: 8px;
  padding: 2rem;
}

.color-section {
  margin: 2rem 0;
}

.color-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
  gap: 1rem;
  margin: 1rem 0;
}

.color-item {
  padding: 1rem;
  border-radius: 8px;
  border: 1px solid var(--neutral-90);
  background: white;
}

.color-swatch {
  height: 80px;
  border-radius: 4px;
  margin-bottom: 0.5rem;
}

.color-info {
  font-size: 0.875rem;
}

.color-name {
  font-weight: var(--font-weight-bold);
  margin-bottom: 0.25rem;
}

.color-value {
  font-family: monospace;
  color: var(--neutral-70);
  font-size: 0.75rem;
}

.feedback-colors {
  display: flex;
  flex-direction: column;
  gap: 2rem;
}

.feedback-group {
  border: 1px solid var(--neutral-90);
  border-radius: 8px;
  padding: 1.5rem;
}

.typography-demo, .spacing-demo, .borders-demo, .components-demo {
  margin-top: 2rem;
}

.type-examples {
  display: flex;
  flex-direction: column;
  gap: 1.5rem;
}

.type-example {
  padding: 1rem;
  border: 1px solid var(--neutral-90);
  border-radius: 8px;
  background: white;
}

.type-specs {
  font-size: 0.75rem;
  color: var(--neutral-70);
  margin-top: 0.5rem;
  font-family: monospace;
}

.spacing-examples {
  display: flex;
  flex-wrap: wrap;
  gap: 2rem;
  margin: 1rem 0;
}

.spacing-item {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 0.5rem;
}

.spacing-info {
  text-align: center;
}

.spacing-name {
  font-weight: var(--font-weight-medium);
  font-size: 0.875rem;
}

.spacing-value {
  font-size: 0.75rem;
  color: var(--neutral-70);
}

.border-examples, .shadow-examples {
  display: flex;
  flex-wrap: wrap;
  gap: 2rem;
  margin: 2rem 0;
}

.border-demo-item {
  display: flex;
  flex-direction: column;
  align-items: center;
  text-align: center;
  width: 120px;
}

.border-demo-visual {
  width: 80px;
  height: 80px;
  margin-bottom: 0.75rem;
}

.border-demo-name {
  font-weight: var(--font-weight-medium);
  margin-bottom: 0.25rem;
}

.border-demo-value {
  font-size: 0.75rem;
  color: var(--neutral-70);
}

.component-group {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 2rem;
  margin: 2rem 0;
}

.component-demo {
  padding: 1.5rem;
  border: 1px solid var(--neutral-90);
  border-radius: 8px;
  background: white;
}

.button-examples {
  display: flex;
  flex-direction: column;
  gap: 1rem;
  align-items: flex-start;
}

.input-examples {
  display: flex;
  flex-direction: column;
  gap: 1rem;
}
</style> 