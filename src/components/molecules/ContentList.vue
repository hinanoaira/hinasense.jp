<script setup lang="ts">
withDefaults(
  defineProps<{
    variant?: 'primary' | 'secondary' | 'tertiary'
  }>(),
  {
    variant: 'secondary',
  }
)
</script>

<template>
  <div :class="['content-list', `variant-${variant}`]">
    <ul>
      <slot />
    </ul>
  </div>
</template>

<style scoped>
.content-list {
  display: block;
  text-align: left;
  width: 100%;
}

.content-list ul {
  list-style: none;
  padding: 0;
  margin: 0;
  width: 100%;
}

:deep(li) {
  display: flex;
  align-items: flex-start;
  position: relative;
  line-height: 1.875;
  margin-top: 0.5rem;
  color: #ffffff;
  font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
}

:deep(li:first-child) {
  margin-top: 0 !important;
}

:deep(li::before) {
  content: '';
  display: block;
  flex-grow: 0;
  flex-shrink: 0;
  height: 1.875rem;
  width: 0.875rem;
  background-position: left center;
  background-repeat: no-repeat;
  background-size: contain;
  margin-right: 0.625rem;
}

:deep(li > p),
:deep(li > span),
:deep(li > a) {
  flex-grow: 1;
  flex-shrink: 1;
  line-height: 1.875;
  margin: 0;
}

/* ==========================================================================
   Variant 1: Primary (Category Items like "VRChat", "neosVR", etc.)
   Filled white circle bullet
   ========================================================================== */
.variant-primary {
  font-size: 1.05em;
  font-weight: 700;
  margin-top: 1.25rem;
  padding-left: 0;
}

.variant-primary :deep(li::before) {
  background-image: url('data:image/svg+xml;charset=utf8,%3Csvg%20xmlns%3D%22http%3A%2F%2Fwww.w3.org%2F2000%2Fsvg%22%20viewBox%3D%220%200%2040%2040%22%3E%3Ccircle%20cx%3D%2220%22%20cy%3D%2220%22%20r%3D%2210%22%20fill%3D%22%23FFFFFF%22%20%2F%3E%3C%2Fsvg%3E');
}

/* ==========================================================================
   Variant 2: Secondary (Regular Items)
   Ring-shaped / Donut bullet, indented
   ========================================================================== */
.variant-secondary {
  font-size: 1em;
  font-weight: 400;
  margin-top: 0.5rem;
  padding-left: 1.25rem;
}

.variant-secondary :deep(li::before) {
  background-image: url('data:image/svg+xml;charset=utf8,%3Csvg%20xmlns%3D%22http%3A%2F%2Fwww.w3.org%2F2000%2Fsvg%22%20viewBox%3D%220%200%2040%2040%22%3E%3Cpath%20d%3D%22M20%2C5C11.7%2C5%2C5%2C11.7%2C5%2C20c0%2C8.3%2C6.7%2C15%2C15%2C15c8.3%2C0%2C15-6.7%2C15-15C35%2C11.7%2C28.3%2C5%2C20%2C5z%20M20%2C31c-6.1%2C0-11-4.9-11-11%20S13.9%2C9%2C20%2C9s11%2C4.9%2C11%2C11S26.1%2C31%2C20%2C31z%22%20fill%3D%22%23FFFFFF%22%20%2F%3E%3C%2Fsvg%3E');
}

/* ==========================================================================
   Variant 3: Tertiary (Sub-items)
   Square bullet, deeper indentation
   ========================================================================== */
.variant-tertiary {
  font-size: 0.95em;
  font-weight: 400;
  margin-top: 0.35rem;
  padding-left: 2.5rem;
}

.variant-tertiary :deep(li::before) {
  background-image: url('data:image/svg+xml;charset=utf8,%3Csvg%20xmlns%3D%22http%3A%2F%2Fwww.w3.org%2F2000%2Fsvg%22%20viewBox%3D%220%200%2040%2040%22%3E%3Crect%20x%3D%227.5%22%20y%3D%227.5%22%20width%3D%2225%22%20height%3D%2225%22%20fill%3D%22%23FFFFFF%22%20%2F%3E%3C%2Fsvg%3E');
}

/* ==========================================================================
   Links inside lists
   ========================================================================== */
:deep(a) {
  color: #ffffff;
  text-decoration: underline;
  transition: opacity 0.2s ease, color 0.2s ease;
}

:deep(a:hover) {
  opacity: 0.8;
  color: #7e9ca6;
}

/* Responsive adjustments */
@media (max-width: 480px) {
  .variant-secondary {
    padding-left: 0.9375rem;
  }

  .variant-tertiary {
    padding-left: 1.875rem;
  }
}
</style>
