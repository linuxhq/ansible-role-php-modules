# ansible-role-php-modules

[![Build Status](https://travis-ci.org/linuxhq/ansible-role-php-modules.svg?branch=master)](https://travis-ci.org/linuxhq/ansible-role-php-modules)

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

GPLv3

## Author Information

This role was created by [Taylor Kimball](http://www.linuxhq.org).
