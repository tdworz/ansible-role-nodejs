# Tom's Node.js Ansible Role

An Ansible role to install and configure Node.js.

## Available Variables

| Variable              | Type     | Default  | Description |
|:----------------------|:--------:|:--------:|:------------|
| nodejs_install_source | string   | `repos`  | One of the following: `repos`. |
| nodejs_version        | string   | `stable` | A semantic version number or keyword. If using a semantic version number, you must use one of the following: just the major version (ie. `22`), the major-minor version (ie. `22.12`), or the major-minor-patch version (ie. `22.12.1`). Allowed keywords are: `latest`, `base`, or `stable`. |

#### Installing from Repos

##### RHEL and RHEL Derivatives

If you want to install Node.js from an application stream module, set
`nodejs_version` to the stream (ie. `22`). The following table shows the
available streams known when this _README_ was last updated.

| Enterprise Linux Version | Stream | Node.js Version |
|:------------------------:|:------:|:---------------:|
| 9                        | `base` | 16.x.x          |
| 9                        | `18`   | 18.x.x          |
| 9                        | `20`   | 20.x.x          |
| 9                        | `22`   | 22.x.x          |

By default, `nodejs_version` is set to `stable` which corresponds to the `base`
stream. You may also set `nodejs_version` to `latest` to use the latest stream.

## Copyright &amp; License

Copyright © 2024 Tom "tdworz" Dworzanski.

This program is free software: you can redistribute it and/or modify it under
the terms of the GNU General Public License as published by the Free Software
Foundation, either version 3 of the License, or (at your option) any later
version.

This program is distributed in the hope that it will be useful, but WITHOUT ANY
WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A
PARTICULAR PURPOSE. See the GNU General Public License for more details.

You should have received a copy of the GNU General Public License along with
this program. If not, see <https://www.gnu.org/licenses/>.
