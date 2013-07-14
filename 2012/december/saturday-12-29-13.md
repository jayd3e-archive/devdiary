BLOG IDEA:  Lesser known caveates in Backbone.js
Possible topics:

- How to properly remove views:

```javascript
view.remove();
model.off(null, null, view);
```

- How to properly replace a view's elment like [so](https://github.com/documentcloud/backbone/issues/1639):

```javascript
var old = this.$el;
this.setElement($(this.model.get('html')));
old.replaceWith(this.$el);
```

- Common rules surrounding Backbone.js software design.  Such has views should only care about
themselves and the creation of their children, all interface changes should be the result of
a model changes in some way, and view events should define everything that the view can "do".

- Cached elements will invalidate as you replace contents of this.$el.\

- jQuery.data() should only be called on page load to consume the page, never during execution.

RANDOM CONCERN:  Let's thing about merging Comments and Solutions into one element in the future,
if they never diverge.  The frontend code for the two modules is near identical!  It's becoming a huge
duplication effort to keep the two in sync with one another.