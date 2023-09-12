<script>
    import "../app.css";
    import { dev } from '$app/environment';
    import { inject } from '@vercel/analytics';
 
    inject({ mode: dev ? 'development' : 'production' });
  </script>
  
  <slot />

  <style lang="postcss">
    :global(html) {
      background-color: theme(colors.black);
      text: theme(colors.white)
    }
  </style>