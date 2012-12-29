BLOG IDEA:  Lesser known caveates in Backbone.js
Possible topics:

- How to properly remove views:

    view.remove();
    model.off(null, null, view);

- How to properly replace a view's elment like [so](https://github.com/documentcloud/backbone/issues/1639):

    var old = this.$el;
    this.setElement($(this.model.get('html')));
    old.replaceWith(this.$el);
