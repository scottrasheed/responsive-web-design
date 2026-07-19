# Notes

## Project
Debug a Pet Adoption Page Notes

---

## Fix #1: Incorrect Image Attribute

### Before
```html
<img href="https://cdn.freecodecamp.org/curriculum/cat-photo-app/cats.jpg" att="Two tabby kittens sleeping together on a couch."></img>
```

### After
```html
<img src="https://cdn.freecodecamp.org/curriculum/cat-photo-app/cats.jpg" alt="Two tabby kittens sleeping together on a couch.">
```

### Lesson Learned
- Images use the `src` attribute to specify the image location.
- Images use the `alt` attribute for alternative text.
- `<img>` is a void element and does **not** need a closing tag (`</img>`).

---

## Fix #2: Incorrect Link Attribute (Cats)

### Before
```html
<a src="/cats">Visit cats page</a>
```

### After
```html
<a href="cats">Visit cats page</a>
```

### Lesson Learned
- Anchor (`<a>`) elements use the `href` attribute to specify the destination.
- `src` is **not** used for hyperlinks.

---

## Fix #3: Incorrect Link Attribute (Dogs)

### Before
```html
<a src="/dogs">Visit dogs page</a>
```

### After
```html
<a href="dogs">Visit dogs page</a>
```

### Lesson Learned
- Every hyperlink should use `href`.
- Relative links point to another page within the same website.

---

# Summary

## What I Practiced

- Correcting invalid HTML attributes
- Using the `src` attribute for images
- Writing descriptive `alt` text
- Creating hyperlinks with `href`
- Understanding void elements like `<img>`
- Debugging HTML syntax
