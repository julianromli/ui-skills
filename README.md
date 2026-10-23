# Wheel latching proof

Proof clips for [ibelick/ui-skills#106](https://github.com/ibelick/ui-skills/pull/106). Recorded with Playwright at 1280x800 on the `design-system/` canvas of [gnoviawan/termul](https://github.com/gnoviawan/termul). Each wheel gesture sends events 40ms apart, so each gesture stays below the 150ms idle gap.

- `before.mp4` (termul `7977a8f2`, per-event routing): one downward gesture over the `ScrollArea` frame scrolls the frame to its end (514/514px). Then the same gesture pans the canvas by y −660px.
- `after.mp4` (termul `03480eb7`, gesture latching): the same gesture scrolls the frame to its end (514/514px), and the canvas does not move (0px). After a 1s pause, a new upward gesture starts on empty canvas and moves over the frame. The canvas pans by y +200px, and the frame stays at 514px.
