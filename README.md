# remirror
Mirror ranking for Antergos and Arch. Does the same as [reflector-antergos](https://github.com/manuel-192/antergos-reflector) and more.
<br>
Note: this page is outdated, the latest package is available at [this repo](https://github.com/manuel-192/antergos-m).
## Usage
remirror --help
## Changes

0.1.49: 2019-Feb-27
- Added support for files /etc/remirror-{arch,antergos}-countries.txt, helps keeping country lists almost automatically up to date for bash completion
- minor bug fixes

0.1.45: 2019-Jan-05
- Options --c, --c-arch and --c-antergos can now use certain country names from Arch and Antergos mirror lists interchangeably, e.g. "USA" and "United_States".
- Option --help provides more examples.

0.1.44: 2019-Jan-04
- Added automatic call to "pacman -Syy" after mirror lists are updated.

0.1.42: 2019-Jan-04
- Added more detailed display about mirror connection failures.
- Added option --no-config for not using the config file. Note that this option, if used, must be the first on the command line.

0.1.41-2: 2019-Jan-02
- Moved remirror.timer and remirror.service to /usr/lib/systemd/system. Please
  - if you have enabled remirror.timer, disable it first (systemctl disable remirror.timer)
  - and then remove these two files manually from the old location at /etc/systemd/system

0.1.41: 2019-Jan-01
- Updated help.
- Updated bash completion file.

0.1.40: 2019-Jan-01
- Added option --x for excluding specific mirrors from ranking.

0.1.39: 2018-Dec-18
- Added option --result that shows the resulting mirror list file(s) before saving them.
- Related to the --result option, an environment variable REMIRROR_VIEWER can be set to have the command name of your favorite editor/viewer, e.g. "gedit" or "kate". The variable value is used for showing the file(s).
- Note: option --os is not really needed and becoming obsolete.
- Minor modifications to error output.

0.1.36: 2018-Dec-16
- Changed default action for option --save from <i>no</i> to <i>backup1</i>.

0.1.35: 2018-Dec-15
- Added new value 'backup1' for option --save, it keeps only one backup instead of many.
- Added option --args that show all given parameters, including from the config file.
- Fixed the display of what options were used while ranking mirrors.

0.1.32: 2018-Dec-14
- Added validity check for the generated mirror files.
- Added new option --sleep for determining initial sleep time. Initial sleep in remirror.service is 60 seconds.
- The default wait time for fetching the reference mirrorlist is now 60 seconds instead of 10.

0.1.29: 2018-Dec-09
- Added support for config file <b>/etc/remirror.conf</b>. If it exists, it will be sourced. Currently it may contain the following variables: REMIRROR_PREOPTIONS and REMIRROR_POSTOPTIONS; they may include any remirror options.
- Added option --version that show the current version number.
- Added systemd service timer for making periodical mirror update.

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
