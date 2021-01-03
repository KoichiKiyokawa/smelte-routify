<script lang="ts">
  import Button from 'smelte/src/components/Button'
  import Card from 'smelte/src/components/Card'
  import TextField from 'smelte/src/components/TextField'

  let email: string
  let password: string

  function onSubmit() {
    alert(JSON.stringify({ email, password }))
  }
</script>

<form on:submit|preventDefault={onSubmit} class="max-w-screen-sm mx-auto">
  <Card.Card class="p-4 w-full">
    <div slot="title">
      <Card.Title title="Login" />
    </div>

    <div slot="text">
      <TextField
        bind:value={email}
        label="email"
        type="email"
        autoComplete="email" />
      <TextField
        bind:value={password}
        label="password"
        type="password"
        autoComplete="current-password" />
    </div>

    <div slot="actions">
      <Button>Login</Button>
    </div>
  </Card.Card>
</form>
