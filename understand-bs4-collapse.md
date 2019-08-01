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

`.collapse`
```scss
.collapse {
  display: none;
  &.show {
    display: block;
  }
}
```




[codepen](https://codepen.io/sidhlee/pen/BEMGrE)