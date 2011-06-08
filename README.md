timesheet
=========

Simple automated timesheet recording for Linux/Xorg. Every 30s or so, it looks
at the title of your active window, and records the time and title if it has
changed since last time.

Prerequisites
-------------

* `xdotool` (Compile from [Git][1] if your version doesn't have `getwindowname`)
* `xprintidle`

tmux
----

If you use tmux, you can name windows (using whatever `rename-window` is bound
to) and show the window name in the window title by adding something like this
to your `.tmux.conf`:

    set -g set-titles on
    set -g set-titles-string '#W'

Usage
-----

Just run `timesheet`. You probably want to log the output::

    timesheet | tee -a ~/timesheet.txt

To do
-----

I haven't written the analysis tools yet.

[1]: https://github.com/jordansissel/xdotool
