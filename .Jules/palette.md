## 2024-05-23 - Playback Rate Accessibility
**Learning:** GTK4 `MenuButton` needs explicit `accessibility { label: ... }` when its content (icon/text) doesn't provide a clear functional name.
**Action:** Always check `MenuButton` and interactive controls inside `Popover` for accessible labels, especially if they are icon-only or use technical labels (like "x 1.0").
