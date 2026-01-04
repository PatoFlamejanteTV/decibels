## 2024-05-23 - Accessibility in Blueprint Files
**Learning:** Screen readers often miss context for slider components (Scale) if they lack an explicit label. Adding `accessibility { label: _("Label"); }` in `.blp` files is a simple, standard way to fix this.
**Action:** Always check `Scale` and other input widgets for accessibility labels in `.blp` files.

## 2024-05-23 - Dynamic Tooltips in GNOME/GTK4
**Learning:** Dynamic tooltips for toggle buttons (like Mute/Unmute) significantly improve clarity. This can be achieved by creating a callback in the TypeScript class (e.g., `mute_button_tooltip_cb`) and binding it to `tooltip-text` in the Blueprint file.
**Action:** Use dynamic tooltips for state-toggling buttons instead of static "Toggle State" tooltips when possible.
## 2024-05-23 - Accessibility Labels in Blueprint
**Learning:** GTK4/Blueprint apps often use `tooltip-text` as a fallback for accessibility names on icon-only buttons, but explicit `accessibility { label: _("..."); }` blocks are superior. They ensure the accessible name is robust, independent of tooltip settings, and allow for distinct descriptions if needed.
**Action:** When auditing Blueprint UI files (`.blp`), always check icon-only buttons (`Button`, `MenuButton`, `ToggleButton`) for explicit accessibility labels. If missing, add them using the localized string format `_("...")`.
## 2024-05-23 - Helper Buttons in Popovers
**Learning:** For inputs like sliders (Scale) that have a "default" or "normal" value (like 1.0x speed), adding a helper button (e.g., "Reset") in the popover significantly improves usability for mouse users who might struggle to drag the slider to the exact value.
**Action:** Consider adding helper buttons for common actions alongside controls in popovers.

## 2025-05-23 - Keyboard Shortcut Discovery
**Learning:** Users often miss keyboard shortcuts when they are hidden in a dialog or menu. Adding hints to tooltips (e.g., "Play (Space)") is a non-intrusive way to improve discoverability without cluttering the UI.
**Action:** When adding or auditing button tooltips, always check if there is an associated keyboard shortcut and include it in the tooltip text, but keep the accessible label clean.

## 2025-05-23 - Blueprint Syntax Traps
**Learning:** In Blueprint files, property assignments (like `tooltip-text: ...`) mistakenly placed inside a `styles []` block will cause parsing errors or silently fail. `styles` must only contain class strings.
**Action:** Double-check indentation and scope when modifying `.blp` files, especially when copying code snippets.
