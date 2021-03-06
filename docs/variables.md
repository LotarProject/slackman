# SlackMan variables

A short description of all variables for SlackMan repositories configuration.


Variable         | Description
-----------------|--------------------------------------------------------------
`arch`           | Machine architecture (eg. x86_64, i686)
`arch.bit`       | Machine bit architecture (eg. 64, 32)
`arch.family`    | Machine architecture family (eg. x86_64, x86)
`mirror`         | Mirror URL from `mirror` config
`release`        | Slackware version from `/etc/slackware-release` (eg. 14.2) or current (follow `slackware.version` option in `slackman.conf` file)
`release.real`   | Slackware "real" release version from  `/etc/slackware-release` file (eg. 14.2)
`release.suffix` | Slackware release suffix (eg. 64 - for Slackware64,  arm - for Slackwarearm)

# Display variables value from slackman

    # slackman list variables

    Variable             Value
    ----------------------------------------
    arch                 x86_64
    arch.bit             64
    arch.family          x86_64
    release              current
    release.real         14.2
    release.suffix       64

## Examples

Slackware-14.2 (32-bit)
--------------

    name=Slackware{$release.suffix}-{$release.real} repository
    mirror=http://example.org/slackware{$release.suffix}-{$release.real}/

      release.suffix => 
      release.real   => 14.2

    name=Slackware64-14.2
    mirror=http://example.org/slackware-14.2

Slackware64-current (64-bit)
--------------

    name=Slackware{$release.suffix}-{$release} repository
    mirror=http://example.org/slackware{$release.suffix}-{$release}/

      release.suffix => 64
      release        => current

    name=Slackware64-current
    mirror=http://example.org/slackware64-current
