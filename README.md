# cronexia-test-svelte-bootstrap

On part direct sur [SvelteKit](https://svelte.dev/docs/kit/creating-a-project)

```bash
npx sv create my-app

cd my-app
# npm install
# npm run dev
bun i

# bun run dev
bun run dev --open
```

---

Ajout de bootstrap

Portage [sveltestrap](https://sveltestrap.js.org/?path=/docs/sveltestrap-overview--docs)

```bash
bun add svelte @sveltestrap/sveltestrap
```

Bootstrap CSS

cronexia-test-svelte-bootstrap/my-app/src/app.html

dans head

<!-- Bootstrap -->
<link
  rel="stylesheet"
  href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/css/bootstrap.min.css"
/>