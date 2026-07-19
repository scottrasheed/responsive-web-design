# Notes

## Debugging Practice

### Invalid Heading

**Before**
```html
<heading2>About</heading2>
```

**After**
```html
<h2>About</h2>
```

**Lesson**
There is no `<heading2>` tag. HTML headings only go from `<h1>` to `<h6>`.

---

### Invalid Paragraph

**Before**
```html
<pp>My name is Camperbot...</pp>
```

**After**
```html
<p>My name is Camperbot...</p>
```

**Lesson**
Paragraphs always use the `<p>` element.

---

### Incorrect Closing Tag

**Before**
```html
<h3>Background and Interests<h3/>
```

**After**
```html
<h3>Background and Interests</h3>
```

**Lesson**
Closing tags must begin with a forward slash (`/`).
