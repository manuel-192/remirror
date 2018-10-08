# remirror
Mirror ranking for Antergos and Arch. Does the same as reflector-antergos and more.
## Usage
remirror --help
## Changes
0.1.23: 2018-Oct-08
- Minor cleanups.

0.1.20: 2018-Oct-04
- Added option --list to show available mirror countries.
- By default, only https mirrors are ranked.
- Streamlined how mirror list saving is done.

0.1.18: 2018-Sep-15
- Changed 'su -c' to 'sudo' (it is used when saving lists to /etc/pacman.d).

0.1.15: 2018-Sep-15
- Fixed some bugs with the country options.

0.1.13: 2018-Sep-15
- Added support for ranking both Antergos and Arch mirrors in one pass. Use option --os=both (the default now) with options --c-antergos=<countries> and --c-arch=<countries>.
- Note that remirror-bash-completion cannot separate Antergos and Arch mirror countries with the old option --c=<countries>. As a workaround it lists both Antergos and Arch mirror countries.

0.1.10: 2018-Sep-15
- Fixed a bug with the --help option, thanks joekamprad!

0.1.9: 2018-Sep-15
- Added option --save={no|yes|backup} that allows saving the ranked mirrorlist file directly into /etc/pacman.d.

0.1.6: 2018-Sep-07
- Added remirror-bash-completion. And because of the completion support, most options are required to start with two hyphens.
- Caveats: remirror-bash-completion does not work in all cases. Workaround: on errors, just don't use it.

0.1.2: 2018-Sep-03
- Warn if no up to date mirrors are found.

0.1: 2018-Aug-31
- Initial release for beta testing.
