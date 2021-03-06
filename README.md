<!-- Source: https://github.com/MattIPv4/template/blob/master/README.md -->

<!-- Title -->
<h1 align="center" id="dns-over-discord">
    DNS over Discord
</h1>

<!-- Tag line -->
<h3 align="center">A 1.1.1.1 DNS resolver built in Go for Discord</h3>

<!-- Badges -->
<p align="center">
    <a href="https://1.1.1.1/" target="_blank">
        <img src="https://img.shields.io/badge/Cloudflare%20DNS-1.1.1.1-F38020?logo=cloudflare&style=flat-square" alt="Cloudflare DNS - 1.1.1.1"/>
    </a>
    <a href="https://github.com/users/MattIPv4/sponsorship" target="_blank">
        <img src="https://img.shields.io/badge/GitHub%20Sponsors-MattIPv4-blue.svg?style=flat-square" alt="GitHub Sponsors"/>
    </a>
    <a href="http://patreon.mattcowley.co.uk/" target="_blank">
        <img src="https://img.shields.io/badge/Patreon-IPv4-blue.svg?style=flat-square" alt="Patreon"/>
    </a>
    <a href="http://slack.mattcowley.co.uk/" target="_blank">
        <img src="https://img.shields.io/badge/Slack-MattIPv4-blue.svg?style=flat-square" alt="Slack"/>
    </a>
</p>

----

<!-- Content -->
## Invite

I'm hosting a copy of this bot myself and you can invite it to your Discord server using this link:

> https://bit.ly/1111-Discord

## Build

This assumes you already have a working Go environment setup, with DiscordGo (github.com/bwmarrin/discordgo) and
 tablewriter (github.com/olekukonko/tablewriter) installed correctly on your system.

From within the 1.1.1.1-Discord project folder, run the below command to compile the Discord bot.

```
go build
```

## Usage

### Go

You can start the Discord bot by running the following, where `<token>` is your Discord Bot token and `<user-id>` is
 your Discord user ID to be the bot admin.

```
./1.1.1.1-Discord -t <token> -a <user-id>
```

### Discord

The bot can be used in Discord by mentioning the bot and then providing a domain name to look up using 1.1.1.1.
By default, if only a domain name is provided, the bot will lookup all supported record types and report them all.
However, you can also provide a list of record types (space separated) after the domain name to select which to lookup.

Mentioning the bot in Discord with no additional arguments will generate the usage message as follows:

```
Usage: @1.1.1.1 <domain> [...types]

Examples:
  @1.1.1.1 mattcowley.co.uk
  @1.1.1.1 mattcowley.co.uk A AAAA

Types:
  If not provided, the default type of "A" will be used
  You can provide a type of "*" to lookup all supported types

Supported types:
  A
  NS
  CNAME
  MX
  TXT
  AAAA
  SRV
  CAA

Invite: https://bit.ly/1111-Discord
Open-source: https://github.com/MattIPv4/1.1.1.1-Discord
```

As the bot admin (see the `-a` argument above), this also enables two extra commands I find useful for production
 deployment. These are the `pull` command than runs `git pull` in the bot directory to fetch updates from Github, as
  well as `exit` which cleanly terminates the bot process.

## Supported Record Types

 - A
 - NS
 - CNAME
 - MX
 - TXT
 - AAAA
 - SRV
 - CAA
 
_The latest supported record types can be found at the top of dns.go in the types map._

<!-- Contributing -->
## Contributing

Contributions are always welcome to this project!\
Take a look at any existing issues on this repository for starting places to help contribute towards, or simply create your own new contribution to the project.

Please make sure to follow the existing standards within the project such as code styles, naming conventions and commenting/documentation.

When you are ready, simply create a pull request for your contribution and I will review it whenever I can!

### Donating

You can also help me and the project out by sponsoring me through [GitHub Sponsors](https://github.com/users/MattIPv4/sponsorship) (preferred), contributing through a [donation on PayPal](http://paypal.mattcowley.co.uk/) or by supporting me monthly on my [Patreon page](http://patreon.mattcowley.co.uk/).
<p>
    <a href="https://github.com/users/MattIPv4/sponsorship" target="_blank">
        <img src="https://img.shields.io/badge/GitHub%20Sponsors-MattIPv4-blue.svg?logo=github&logoColor=FFF&style=flat-square" alt="GitHub Sponsors"/>
    </a>
    <a href="http://patreon.mattcowley.co.uk/" target="_blank">
        <img src="https://img.shields.io/badge/Patreon-IPv4-blue.svg?logo=patreon&logoColor=F96854&style=flat-square" alt="Patreon"/>
    </a>
    <a href="http://paypal.mattcowley.co.uk/" target="_blank">
        <img src="https://img.shields.io/badge/PayPal-Matt%20(IPv4)%20Cowley-blue.svg?logo=paypal&logoColor=00457C&style=flat-square" alt="PayPal"/>
    </a>
</p>

<!-- Discussion & Support -->
## Discussion, Support and Issues

Need support with this project, have found an issue or want to chat with others about contributing to the project?
> Please check the project's issues page first for support & bugs!

Not found what you need here?

* If you have an issue, please create a GitHub issue here to report the situation, include as much detail as you can!
* _or,_ You can join our Slack workspace to discuss any issue, to get support for the project or to chat with contributors and myself:

<a href="http://slack.mattcowley.co.uk/" target="_blank">
    <img src="https://img.shields.io/badge/Slack-MattIPv4-blue.svg?logo=slack&logoColor=blue&style=flat-square" alt="Slack" height="30">
</a>
