# rearbreeze-spec

> Spec of a utility first CSS framework based on HTML data attributes

Utility first CSS frameworks are a great way to enable developers take full
control of their design. But, sometimes, you need to describe a lot of class
names in order to proper render you component.

The idea of Rearbreeze is to, instead of creating classes to define you style,
you create HTML data attributes. Here are some advantages:

- The possibility to break lines
- Fast reorder of data attributes
- Grouping attributes with the same category

## Comparison with...

### Tailwindcss

```html
<div class="flex bg-gray-200">
  <div class="flex-1 text-gray-700 text-center bg-gray-400 px-4 py-2 m-2">1</div>
  <div class="flex-1 text-gray-700 text-center bg-gray-400 px-4 py-2 m-2">2</div>
  <div class="flex-1 text-gray-700 text-center bg-gray-400 px-4 py-2 m-2">3</div>
</div>
```

### Rearbreeze

```html
<div
    flex
    bg-gray-200
>
  <div
    flex-1
    text-center
    text-gray-700
    bg-gray-400
    px-4
    py-2
    m-2
  >1</div>
  <div
    flex-1 text-center
    text-gray-700 bg-gray-400
    px-4 py-2 m-2
  >2</div>
  <div flex-1 text-center text-gray-700 bg-gray-400 px-4 py-2 m-2>3</div>
</div>
```

```css
[flex] {
    display: flex;
}

[flex-1] {
    flex: 1 1 0%;
}

[bg-gray-200] {
    background-color: #edf2f7;
}

[bg-gray-400] {
    background-color: #cbd5e0!important;
}

[text-gray-700] {
    color: #4a5568!important;
}

[text-center] {
    text-align: center;
}

[px-4] {
    padding-left: 1rem;
    padding-right: 1rem;
}

[py-2] {
    padding-top: .5rem;
    padding-bottom: .5rem;
}

[m-2] {
    margin: .5rem;
}
```

## How about collision?

To avoid collision, with user data attributes, the bundle version can
come with a prefix.

## How can I start using?

Unfortunately, this is just the idea of a CSS Framework. If you interested in
implementing it, feel free to do it.
