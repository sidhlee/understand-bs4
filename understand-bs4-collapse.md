# Understand BS4
## Collapse
---
### Example
```html
<div class="container mt-3">
  <p>
    <a class="btn btn-primary" role="button"
       data-toggle="collapse" href="#content"
       aria-expanded="false" aria-controls="content">
      Link with href
    </a>
    <button class="btn btn-primary" type="button"
            data-toggle="collapse" data-target="#content"
            aria-expanded="false" aria-controls="content">
      Button with data-target
    </button>
  </p>
  <div class="collapse" id="content">
    <div class="card card-body">
      <ul>
        <li><code>.collapse</code> hides content</li>
        <li><code>.collapsing</code> is applied during transitions</li>
        <li><code>.collapse.show</code> shows content
      </ul>
      <p>
      You can use a link with the <code>href</code> attribute, 
      or a button with the <code>data-target</code> attribute. 
      In both cases, the <code>data-toggle="collapse"</code> is required.
      </p>
    </div>
  </div>
</div>
```
#### scss
`.collapse`
```scss
.collapse {
  display: none;
  &.show {
    display: block;
  }
}
```
`.card`
```scss
.card {
  position: relative;
  display: flex;
  flex-direction: column;
  min-width: 0;
  word-wrap: break-word;
  background-color: $card-bg;
  background-clip: border-box;
  border: $card-border-width solid $card-border-color;
  @include border-radius($card-border-radius);

  > hr {
    margin-right: 0;
    margin-left: 0;
  }

  > .list-group:first-child {
    .list-group-item:first-child {
      @include border-top-radius($card-border-radius);
    }
  }

  > .list-group:last-child {
    .list-group-item:last-child {
      @include border-bottom-radius($card-border-radius);
    }
  }
}
```
`.card-body`
```scss
.card-body {
  // Enable `flex-grow: 1` for decks and groups so that card blocks take up
  // as much space as possible, ensuring footers are aligned to the bottom.
  flex: 1 1 auto;
  padding: $card-spacer-x;
}
```



[codepen](https://codepen.io/sidhlee/pen/BEMGrE)