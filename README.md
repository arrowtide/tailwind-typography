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

## Other stuff

### `.prose` no longer has a container
Use the `.prose-container` class for that. 

### `.prose-invert` doesn't work
Havn't built a tailwind only dark theme yet. But it's coming. 
