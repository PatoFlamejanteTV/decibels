## 2024-05-23 - Volume Slider Accessibility
**Learning:** `Gtk.Scale` widgets in Blueprint files default to a generic "slider" role/name for screen readers. Explicitly adding an `accessibility { label: _("Name"); }` block is required for context.
**Action:** When working with sliders or icon-only controls in Blueprint, always verify if an accessible label is provided.
