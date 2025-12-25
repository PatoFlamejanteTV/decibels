## 2024-05-23 - Accessibility in Blueprint Files
**Learning:** Screen readers often miss context for slider components (Scale) if they lack an explicit label. Adding `accessibility { label: _("Label"); }` in `.blp` files is a simple, standard way to fix this.
**Action:** Always check `Scale` and other input widgets for accessibility labels in `.blp` files.

## 2024-05-23 - Dynamic Tooltips in GNOME/GTK4
**Learning:** Dynamic tooltips for toggle buttons (like Mute/Unmute) significantly improve clarity. This can be achieved by creating a callback in the TypeScript class (e.g., `mute_button_tooltip_cb`) and binding it to `tooltip-text` in the Blueprint file.
**Action:** Use dynamic tooltips for state-toggling buttons instead of static "Toggle State" tooltips when possible.
