<script>
  import Nav from 'src/components/organisms/Nav.svelte'
  import { Router } from '@roxi/routify'
  import { routes } from '../.routify/routes'
</script>

<style lang="sass">
  @import 'smelte/src/tailwind.css'
</style>

<Nav />

<main class="mt-20">
  <Router {routes} />
</main>
