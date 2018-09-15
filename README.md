# remirror
Mirror ranking for Antergos and Arch. Does the same as reflector-antergos and more.
## Usage
remirror --help
## Changes
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
