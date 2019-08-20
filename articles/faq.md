# FAQ

### Why is there no remaining time displayed in DropPy?

*DropPy* has **no way to know** how long your script takes.

It extracts the files from your dropped object and kicks off your *Workflow*.

And I didn't want to require any kind of status reporting or time estimation inside *Task*. Writing *Tasks* should be as easy as possible. Not even understanding inheritage is necessary for writing a *Task*.

### Why doesn't DropPy work with versions of macOS before 10.12 Sierra?

*DropPy* uses the **item-based API** for accessing dragged & dropped objects that was introduced at **WWDC 2016** and rolled out in **Sierra**.

The old **NSPasteboard** based implementation is deprecated now, but still available in **High Sierra**.

The reason why I don't want to support both implementations is because they react fundamentally different on dropped items. For example when dragging a file from Finder to *DropPy* accessing it through the NSPasteboard implementation **moves it** while the item-based API **copies it**.

Once it was clear that I needed at least 10.12 I also used **Unified Logging**.

### Why is DropPy not available on the macOS AppStore?

Nobody uses the App Store.
