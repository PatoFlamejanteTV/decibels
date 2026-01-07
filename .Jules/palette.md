## 2024-02-14 - [Tooltip Shortcuts]
**Learning:** When adding keyboard shortcut hints to tooltips manually (e.g., "Play (Space)"), ensure they are updated dynamically in TypeScript if the button state changes (e.g., Play -> Pause). Also, avoid putting these hints in the `accessibility` label to keep screen reader output clean.
**Action:** Use `bind_property_full` with a transform function in TypeScript to manage dynamic tooltips with shortcuts.
