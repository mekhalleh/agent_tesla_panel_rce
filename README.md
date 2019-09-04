# agent_tesla_panel_rce

This module exploit the command injection vulnerability in control center of the agent Tesla.

## Setup

Resources for testing are available here:
<https://github.com/mekhalleh/agent_tesla_panel_rce/tree/master/resources>

### Windows

I used WAMP server 3.1.9 x64 configured with PHP version 5.6.40 (for ioncube compatibility).

### Linux

I used a Debian 9 on which I installed PHP version 5.6.40 (for ioncube compatibility).

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
