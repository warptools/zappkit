ZappKit -- a kit for building Zapps
===================================

Zapps (see [zapps.app](https://zapps.app/) !) are a convention for packaging linux executables
in a highly portable and distro-agnostic way.

More information about Zapps can be found in the website,
but in brief: Zapps offer simplicity of distribution on par with static linking, while still using dynamic libraries.
This means any application can be packaged as a Zapp (often, without even rebuilding!).

This repo is to collect tools which help produce Zapps.

---

Hacking Notes
-------------

This repo uses bash heavily.

Bash scripting may not be the most modern nor easy-to-use language,
but it is very good at lashing disparate sytems together,
and it is very nearly guaranteed that your current system has a bash on it,
which makes it a utilitarian choice for work such as this.

We use "bash safe mode" (e.g. `set -euo pipefail`) to improve the safety of working in bash.

We use Bash's built-in regexp support in some places.
We prefer this to shelling out to other processing systems such as awk,
because it's one fewer dependency overall.
Bash has had regexp support for a pretty long time;
we hope not to encounter any bug reports from people using shells so ancient it's unsupported ;)
(BASH_REMATCH first appears in the release notes for bash-3.0-alpha... that's now nearly 20 years ago.
I _think_ we ought to be reasonably safe to count on this feature, now.)

---

License
-------

We use a dual license of Apache2 or the MIT license, at your option.
This is intended to be a freedom-maximizing choice.
If you submit code to this repo, you agree your contributions will be redistributable under these licenses.

SPDX-License-Identifier: Apache-2.0 OR MIT
