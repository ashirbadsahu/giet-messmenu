<script>
    import "../app.css";
  </script>
  
  <slot />

  <style lang="postcss">
    :global(html) {
      background-color: theme(colors.black);
      text: theme(colors.white)
    }
  </style>