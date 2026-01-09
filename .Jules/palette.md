## 2025-01-20 - [Keyboard Access for Custom Sliders]
**Learning:** Custom slider widgets (like `APWaveformScale`) require manual implementation of `Gtk.AccessibleRole.SLIDER` behaviors, specifically focus management, keyboard navigation (Left/Right/Home/End), and visual focus rings. Standard `Gtk.Scale` does this automatically, but custom widgets do not.
**Action:** When creating custom interactive widgets, always explicitly:
1. Set `this.focusable = true`.
2. Add a `Gtk.EventControllerKey` for keyboard interaction.
3. Call `this.grab_focus()` on mouse/touch interaction.
4. Implement `vfunc_snapshot` to render a focus ring using `snapshot.render_focus()` when `this.has_focus`.
