## Test with Svelte Parallax

- Bun
- Tailwind
- Svelte

## Learning

This test helped me to understand and the **foundation** to create better parallax effects

Core concepts:

- Parallax Container
  A block which position is relative and will be the containing block for all the movement, this receives a parameter named **sections** which basically is the ammount of screens
- Parallax Layers
  Parallax layers are the actual absolute layers that will move across the container at **different speed** and will appear in different

- Sticky Layer
  Same as a Parallax layer, with the different that this will stick from a screen to another one

### Improvements:

- Make big changes based on smaller but keep the proportions. ie - change from 0.5 to 0.6 and make it smaller/bigger in that proportion (probably `onProgress`)

- Change `layout` of `sticky` based on the progress
