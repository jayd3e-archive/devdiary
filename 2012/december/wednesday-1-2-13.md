TODO:  After this discussion with braddunbar:

_jayd3e: can someone give me and example of a time you would want to call a View function directly from the inside of another View function, as opposed to creating an event that can be triggered to call that function
braddunbar: _jayd3e: Any time you don't care about loose coupling.  :)
braddunbar: i.e. Rarely, but sometimes.
_jayd3e: braddunbar: so that term is thrown around a ton, and I get why it's bad to have views tied together, but I don't see how it applies internally within a view
_jayd3e: so why does it matter if one function calls another from within a view
braddunbar: _jayd3e: In my experience, loosely coupled views are easier to test and reuse.  Let me elaborate a bit...
braddunbar: Let's say I have the views Foo and Bar.  Instances of Foo should cause Bar to be removed on some user action.
braddunbar: I can call `remove` on `this.bar` (tight coupling) or I can trigger `remove` on bar.
braddunbar: If I trigger "remove", Bar can be tested in isolation (without Foo).
braddunbar: Further, Bar can change it's implementation and handle "remove" differently without changing code in Foo.
_jayd3e: braddunbar: so let's say we're just discussing the view called Bar.  And within Bar, there is a method that updates the model that backs Bar and then replaces elements in the DOM to reflect this update.  One step in updating the DOM is clearing the view.el.  So let's say we have a special function that goes and removes everything in the view.el.  Do we create an event that can be triggered, then calls that clear function?  Or can we ju
_jayd3e: st call clear() directly?
braddunbar: _jayd3e: If it's within the same view, I usually just call the function.
_jayd3e: braddunbar: ok cool thanks.  The reason I sometimes create events to trigger certain functions, is if that event acts as a kind of "action" for the view itself.  So let's say a number of other views needed to clear Bar as well, not only itself.  I could create an event to clear Bar, so it could be called from outside the view.
_jayd3e: reasonable approach?
braddunbar: _jayd3e: Sure.

I decided that I need to go through, and each time I created a custom event to just call a function, I need to now just call the function directly.

TIP: Try to avoid representing SQLAlchemy tables as strings in python code.  It defeats some of the point of an ORM.
TIP: SQLAlchemy Filter() is covered from sql injection.

TODO: Talk with Mike about how to create a nice queryable api, that accepts dynamic fields as GET variables