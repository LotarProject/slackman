# SlackMan - Slackware Package Manager ChangeLog

## [v1.1.0]

### Added
  * New commands (`config` get & set via CLI, `log`, etc) and options (`--details`, `--Security-fix`, etc)
  * Added DBus interface to fetch latest Security Fix & ChangeLog and packages update
  * Added `slackman-notifier` DBus client to notifiy Security Fix & ChangeLog and packages update via `org.freedesktop.Notification`
  * Color Output (you can disable temporary via `--color=never` option or via `slackman config main.color never` command)
  * Informational message for new kernel upgrade. New SlackMan remember and help the user to create new `initrd.gz` file and install the new kernel via `lilo` (or `eliloconfig`) command
  * Added `.new` config file search in `/etc` directory & user interaction (`slackpkg` like feature)
  * Added daily update metadata (packages list & ChangeLog) via cron
  * Added new bugs to fix later

### Changed
  * DB structure (added new fileds and index to speedup operations)
  * DB schema update
  * Splitted `SlackMan/Command.pm` module in different modules `SlackMan/Commands/*.pm`

### Fixed
  * Fixed ChangeLog parser. Now slackman support most Slackware ChangeLog dialect (AliebBob, SlackOnly, etc)

## Older releases

  * [v1.0.4]
  * [v1.0.3]
  * [v1.0.2]
  * [v1.0.1]
  * [v1.0.0]

[Develop]: https://github.com/LotarProject/slackman/compare/master...develop
[v1.1.0]: https://github.com/LotarProject/slackman/compare/v1.0.4...v1.1.0
[v1.0.4]: https://github.com/LotarProject/slackman/compare/v1.0.3...v1.0.4
[v1.0.3]: https://github.com/LotarProject/slackman/compare/v1.0.2...v1.0.3
[v1.0.2]: https://github.com/LotarProject/slackman/compare/v1.0.1...v1.0.2
[v1.0.1]: https://github.com/LotarProject/slackman/compare/v1.0.0...v1.0.1
[v1.0.0]: https://github.com/LotarProject/slackman/compare/v1.0.0...v1.0.0