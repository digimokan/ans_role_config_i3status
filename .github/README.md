# ans_role_config_i3status

Install and configure the i3status panel-bar status area utility.

[![Release](https://img.shields.io/github/release/digimokan/ans_role_config_i3status.svg?label=release)](https://github.com/digimokan/ans_role_config_i3status/releases/latest "Latest Release Notes")
[![License](https://img.shields.io/badge/license-MIT-blue.svg?label=license)](LICENSE.md "Project License")

## Table Of Contents

* [Purpose](#purpose)
* [Supported Operating Systems](#supported-operating-systems)
* [Quick Start](#quick-start)
    * [Use From Playbook](#use-from-playbook)
* [Role Options](#role-options)
* [Contributing](#contributing)

## Purpose

* Install and configure the [i3status](https://i3wm.org/i3status/manpage.html#_external_scripts_programs_with_i3status)
  utility.
* i3status displays time/date, battery, volume, etc items in a window manager's
  panel bar (aka tray).
* i3status was designed to work with the [i3bar](https://i3wm.org/docs/userguide.html#_configuring_i3bar)
  panel bar, which is bundled with the core [i3wm](https://i3wm.org/), but it
  will also display status items in other bars, such as [dzen2](https://github.com/robm/dzen)
  or [lemonbar](https://github.com/LemonBoy/bar).

## Supported Operating Systems

* Ubuntu bionic (18.04), focal (20.04), hirsute (21.04), impish (21.10)
* Arch Linux
* FreeBSD

## Quick Start

### Use From Playbook

1. Create `requirements.yml` in ansible project root, and add this content:

   ```yaml
   # requirements.yml
   - src: https://github.com/digimokan/ans_role_config_i3status
   ```

2. From the project root directory, install/download the role:

   ```shell
   $ ansible-galaxy install --role-file requirements.yml --roles-path ./roles --force-with-deps
   ```

   * _NOTE:_ `--force-with-deps` _ensures subsequent calls download updates_

3. Include the role like any local role, from the project playbook:

   ```yaml
   # playbook.yml
   - hosts: localhost
     connection: local
     tasks:
       - name: "Install and configure the i3status panel-bar status area utility"
         ansible.builtin.include_role:
           name: ans_role_config_i3status
   ```

## Role Options

See the role `defaults` files for main role vars listings:

  * [defaults](../defaults/main/)

Define these _required_ vars for the role:

  * `i3status_user_name`: user name of main i3status user

## Contributing

* Feel free to report a bug or propose a feature by opening a new
  [Issue](https://github.com/digimokan/ans_role_config_i3status/issues).
* Follow the project's [Contributing](CONTRIBUTING.md) guidelines.
* Respect the project's [Code Of Conduct](CODE_OF_CONDUCT.md).

