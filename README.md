> [!IMPORTANT]  
> This requires Tailwind v4.

# tailwind-typography
Like the official Tailwind Typography package but:

- _Almost_ everything is css variables.
- No dependencies, just a css file.
- No need to overwrite the base styles, just edit them directly and keep the exact same specificity. 

# Installation
Just drop and drop the `typography.css` file into 
your your project and import it like so into the `base` layer. 

```css
@import 'typography' layer(base);
```

## Demo
You can check out [the demo here.](https://play.tailwindcss.com/1xXD1zTqcC?file=css). The demo is based on the original by [Tailwind Labs](https://github.com/tailwindlabs/tailwindcss-typography) 


> [!NOTE]  
> I think I got everything whilst porting this. If you think something is missing or broken, please submit an issue. Thanks!


---

## Changes

### `.prose` no longer has a container by default
Use the `.prose-container` class for that. 

### `.prose-invert` doesn't work
Havn't built a tailwind only dark theme yet. But it's coming. It's really easy to make one yourself in the meantime:

```css
.dark:root {
  --prose-color: var(--color-slate-500);
  ...
  ...
}
```

### `.lead` is no longer a thing
You can easily add this back in though:

```css
.prose :where(.lead):not(:where([class~="not-prose"], [class~="not-prose"] *)) {
    color: var(--prose-lead-color);
    font-size: var(--prose-lead-size);
    margin-top: var(--prose-lead--margin-top);
    margin-bottom: var(--prose-lead-margin-bottom);
    line-height: var(--prose-lead-leading);
    letter-spacing: var(--prose-lead-tracking);
}
```

