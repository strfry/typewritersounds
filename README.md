# Purpose

This configuration can help when you find that your keyboard is not making enough noise while typing.
It solves that problem by assigning typewriter sounds to keypress events.

# Installation (Debian)

```
  apt install triggerhappy

  cp triggers.d/typewriter.conf /etc/triggerhappy/triggers.d
  cp -r typewritersounds /usr/local/share/typewritersounds

  service triggerhappy restart
```

# Known Bugs

Since triggerhappy executes aplay as a different user (by default nobody),
which means that it will only work when the sound device is unblocked.
Redirection to pulseaudio also will not work without further configuration.
