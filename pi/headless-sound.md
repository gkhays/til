# Play Sound from Unattended Session

I'm working on a Python program that runs on the Raspberry Pi and plays a sound. When running interactively, everything is great. But when attempting to run from `systemd` or otherwise unattended, it does not play the sound.

I gave up on `systemd` for the moment because I got it working under `cron`. The trick is to set the `XDG_RUNTIME_DIR` environment variable.

```bash
XDG_RUNTIME_DIR=/run/user/user_id
```

In the `crontab` file it looks like this.

```bash
* * * * * XDG_RUNTIME_DIR=/run/user/$(id -u) /path/to/script
```

## References

1. [(Resolved) Audio over bluetooth doesn't work when launch as a systemd service](https://raspberrypi.stackexchange.com/questions/145499/resolved-audio-over-bluetooth-doesnt-work-when-launch-as-a-systemd-service)
1. [Audio doesn't play with crontab on Raspberry Pi](https://stackoverflow.com/a/43436895/6146580)
1. [Play sound from a non-interactive shell (systemd service, cron)](https://wiki.archlinux.org/title/PulseAudio#Play_sound_from_a_non-interactive_shell_.28systemd_service.2C_cron.29)
1. [How to Auto Start a Program on Raspberry Pi? (4 ways)](https://raspberrytips.com/autostart-a-program-on-boot/)
