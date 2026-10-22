<template>
  <footer class="app-footer">
    <p class="footer-text">
      <span class="p">
        © 2026 雛野あいら hinasense.jp<br />
        Profile icon by
        <a href="https://x.com/neonewryomo" target="_blank" rel="noopener">@neonewryomo</a>
      </span>
    </p>
  </footer>
</template>

<style scoped>
.app-footer {
  margin-top: 3rem;
  width: 100%;
  text-align: center;
}

.footer-text {
  color: #ffffff;
  font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  font-size: 1em;
  line-height: 1.125;
  font-weight: 400;
  letter-spacing: 0rem;
  margin: 0;
}

.footer-text a {
  color: inherit;
  text-decoration: underline;
  transition: color 0.25s ease;
}

.footer-text a:hover {
  text-decoration: none;
}

@media (max-width: 736px) {
  .app-footer {
    margin-top: 2.25rem;
  }
}
</style>
