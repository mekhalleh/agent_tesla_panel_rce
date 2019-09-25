# agent_tesla_panel_rce

This module exploit the command injection vulnerability in control center of the agent Tesla.

## Setup

Resources for testing are available here:
<https://github.com/mekhalleh/agent_tesla_panel_rce/tree/master/resources>

### Windows

For WebPanel1.7z (unauthenticated RCE), I used WAMP server 3.1.9 x64 configured with PHP version 5.6.40 (for ioncube compatibility).

For WebPanel2.7z (authenticated RCE), I used WAMP server 3.1.9 x64 configured with PHP version 7.2.18 (for ioncube compatibility).

For WebPanel3.7z (authenticated RCE), I used WAMP server 3.1.9 x64 configured with PHP version 7.2.18 (source code is not obfuscated, don't need ioncube).

### Linux

For WebPanel1.7z (unauthenticated RCE), I used a Debian 9 on which I installed PHP version 5.6.40 (for ioncube compatibility).

For WebPanel2.7z (authenticated RCE), I used a Debian 9 on which I installed the default PHP version (for ioncube compatibility).

For WebPanel3.7z (unauthenticated RCE), I used a Debian 9 on which I installed the default PHP version (source code is not obfuscated, don't need ioncube).

## Verification Steps

1. Install the module as usual
2. Start msfconsole
3. Do: `use exploit/multi/http/agent_tesla_panel_rce`
4. Do: `set RHOSTS 192.168.0.15`
5. Do: `run`

![alt text][module_info]

## Targeting

### Windows

![alt text][module_auto-windows]

![alt text][module_cmd-windows]

### Linux

![alt text][module_auto-linux]

![alt text][module_cmd-linux]

[module_info]: https://raw.githubusercontent.com/mekhalleh/agent_tesla_panel_rce/master/pictures/01-demo.png "Module: info"
[module_auto-windows]: https://raw.githubusercontent.com/mekhalleh/agent_tesla_panel_rce/master/pictures/02-demo.png "Module: auto-targeting windows"
[module_cmd-windows]: https://raw.githubusercontent.com/mekhalleh/agent_tesla_panel_rce/master/pictures/03-demo.png "Module: cmd-windows"
[module_auto-linux]: https://raw.githubusercontent.com/mekhalleh/agent_tesla_panel_rce/master/pictures/04-demo.png "Module: auto-linux"
[module_cmd-linux]: https://raw.githubusercontent.com/mekhalleh/agent_tesla_panel_rce/master/pictures/05-demo.png "Module: cmd-linux"
