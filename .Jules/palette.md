## 2024-05-23 - Accessibility Labels in Blueprint
**Learning:** GTK4/Blueprint apps often use `tooltip-text` as a fallback for accessibility names on icon-only buttons, but explicit `accessibility { label: _("..."); }` blocks are superior. They ensure the accessible name is robust, independent of tooltip settings, and allow for distinct descriptions if needed.
**Action:** When auditing Blueprint UI files (`.blp`), always check icon-only buttons (`Button`, `MenuButton`, `ToggleButton`) for explicit accessibility labels. If missing, add them using the localized string format `_("...")`.
