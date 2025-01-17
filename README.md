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
# 🚨 cd my-app
bun add svelte @sveltestrap/sveltestrap
```

## Bootstrap CSS

⚡️Note: mise en place du socle > Récupérer les fichiers plutôt que CDN lol

Add to your apps static index.html file

cronexia-test-svelte-bootstrap/my-app/src/app.html

```html
<!-- dans <head> -->
<!-- Bootstrap -->
<link
  rel="stylesheet"
  href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/css/bootstrap.min.css"
/>
```

---

Add to your main App.svelte file

cronexia-test-svelte-bootstrap/my-app/src/routes/+page.svelte

```svelte
<svelte:head>
  <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/css/bootstrap.min.css">
</svelte:head>
```

---

Import the styles directly in your CSS bundle

cronexia-test-svelte-bootstrap/my-app/src/routes/+page.svelte > fin de page

```html
<style>
  @import 'https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/css/bootstrap.min.css';
</style>
```

---

Use the provided Styles component

```svelte
<script>
  import { Styles } from '@sveltestrap/sveltestrap';
</script>

<Styles />
```

---

Then use Sveltestrap components in your svelte component:

```svelte
<script>
  import { Button, Col, Row } from '@sveltestrap/sveltestrap';
</script>

<Row>
  <Col>
    <Button color="primary" outline>Hello World!</Button>
  </Col>
</Row>
```

✅📌 test > le bouton est la & fonctionnel

---

## Bootstrap Icons

If you want to use the Icon component, you also must include a link to Bootstrap Icon CSS, for example:

✨ or the Styles component includes the Bootstrap Icon CSS by default:

[bootstrap icons](https://icons.getbootstrap.com/)

✅📌 test

```html
<Button color="primary" outline>Hello World! <i class="bi bi-airplane-engines"></i></Button>
```

---

## Sapper

what is that

[sapper](https://sapper.svelte.dev/) > The predecessor of SvelteKit

yeah bah non du coup

---

## Essai d'un composant au pif

✅📌 [listgroup](https://sveltestrap.js.org/?path=/docs/components-listgroup--docs)

Impecab'
