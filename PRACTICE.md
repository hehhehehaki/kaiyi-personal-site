# Rebuild the homepage, one step at a time

Work in a separate `practice` folder. Keep the original as a reference. Save your progress after each step.

## 1. Create the page skeleton

Create `index.html`:

```html
<!doctype html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>My personal homepage</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <header><nav>My name · About · Everyday Joys</nav></header>
  <main>
    <section id="home"><h1>Hi, I’m Kaiyi.</h1><p>Welcome to my little world.</p></section>
    <section id="about"><h2>About me</h2><p>Write a short introduction.</p></section>
  </main>
  <footer>Made with curiosity.</footer>
  <script src="script.js"></script>
</body>
</html>
```

Open it in your browser. Notice how HTML describes the content, even without styling.

## 2. Add your own colors

Create `styles.css`:

```css
:root {
  --bg: #fbf7fa;
  --ink: #44344f;
  --accent: #aa547b;
}
* { box-sizing: border-box; }
body { margin: 0; background: var(--bg); color: var(--ink); font-family: Arial, sans-serif; }
main { max-width: 1100px; margin: auto; padding: 24px; }
section { padding: 50px 0; }
```

Change `--accent` to another hex color. Refresh and inspect the result. A variable only affects elements whose styles use it: try `h1 { color: var(--accent); }`.

## 3. Build a hero with a photo

Put your introduction and an image inside a container with `class="hero"`. Copy the `assets` folder beside your HTML.

```html
<section class="hero" id="home">
  <div><h1>Hi, I’m Kaiyi.</h1><p>Life, learning, and a little curiosity.</p></div>
  <img src="assets/profile.jpg" alt="My Shiba Inu enjoying a walk">
</section>
```

```css
.hero { display: grid; grid-template-columns: 1.2fr 1fr; gap: 40px; align-items: center; }
.hero img { width: 100%; border-radius: 12px; }
```

Try changing the gap and column proportions. Explain what each change does before looking at the original.

## 4. Make it work on phones

```css
@media (max-width: 760px) {
  .hero { grid-template-columns: 1fr; }
}
```

Narrow your browser window. The two columns should stack. Look for text or images that overflow.

## 5. Add navigation and cards

Use `<a href="#about">About</a>` to jump to `<section id="about">`. Create three interest cards with `<article>`, a heading, and a paragraph. Use CSS Grid for desktop and a single column on small screens. Add `html { scroll-behavior: smooth; }` if you like smooth anchor scrolling.

## 6. Add a small JavaScript interaction

Create category buttons and entries:

```html
<button data-filter="all">All</button>
<button data-filter="learn">Learning</button>
<article data-category="learn">My learning experience</article>
<article data-category="make">My creative work</article>
```

In `script.js`:

```js
document.querySelectorAll('[data-filter]').forEach(button => {
  button.addEventListener('click', () => {
    const category = button.dataset.filter;
    document.querySelectorAll('[data-category]').forEach(entry => {
      entry.hidden = category !== 'all' && entry.dataset.category !== category;
    });
  });
});
```

Read it as: find buttons → listen for a click → read the chosen category → hide entries that do not match. In the finished source, selected buttons also update `aria-pressed` and their active appearance.

## 7. Check your result

- Read every heading and paragraph.
- Test all navigation links and filters.
- Check narrow and wide windows.
- Press Tab to visit links and buttons; keep focus visible.
- Confirm the image loads and has meaningful alternative text.
- Open browser developer tools and check the Console for errors.

## 8. Practice without copying everything

First change one color and one paragraph. Next add a fourth interest card. Then rebuild the hero without looking at the original. Finally add your own feature, such as a light/dark theme button. Keep each change small so you understand why it works.

This is a reconstructed learning guide for the finished design, not a transcript of the AI’s tool calls. Publishing the source to GitHub and hosting a website are separate actions.
