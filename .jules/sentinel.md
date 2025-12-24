## 2024-05-23 - Command Injection via String Interpolation
**Vulnerability:** String interpolation of object properties into GStreamer pipeline descriptions (`Gst.parse_launch`).
**Learning:** Even if the interpolated value is currently a number, future refactoring or external exposure could turn it into a sink for command injection (e.g. `interval=100 ! bad_plugin`).
**Prevention:** Always use `set_property` on the created elements instead of embedding values directly into the pipeline string. This enforces strict separation of structure (pipeline) and data (properties).
