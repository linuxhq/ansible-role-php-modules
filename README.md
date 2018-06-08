# ansible-role-php-modules

[![Build Status](https://travis-ci.org/linuxhq/ansible-role-php-modules.svg?branch=master)](https://travis-ci.org/linuxhq/ansible-role-php-modules)
[![Ansible Galaxy](https://img.shields.io/badge/ansible--galaxy-php--modules-blue.svg?style=flat)](https://galaxy.ansible.com/linuxhq/php-modules)
[![License](https://img.shields.io/badge/license-GPLv3-brightgreen.svg?style=flat)](COPYING)

RHEL/CentOS - Configure PHP modules and extensions

## Requirements

None

## Role Variables

Available variables are listed below, along with default values:

    php_modules_enablerepo: ''
    php_modules: {}

## Dependencies

None

## Example Playbook

    - hosts: servers
      roles:
        - role: linuxhq.php-modules
          php_modules_enablerepo: remi
          php_modules:
            - package: common
              extensions:
                - name: curl
                  enabled: True
                - name: fileinfo
                  enabled: True
                - name: json
                  enabled: True
                - name: phar
                  enabled: False
                - name: zip
                  enabled: Tre
            - package: xml
              extensions:
                - name: dom
                  enabled: False
                - name: wddx
                  enabled: False
                - name: xmlreader
                  enabled: True
                - name: xmlwriter
                  enabled: True
                - name: xsl
                  enabled: True
         
## License

Copyright (C) 2018 Taylor Kimball <tkimball@linuxhq.org>

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program. If not, see <http://www.gnu.org/licenses/>.
