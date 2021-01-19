# yast2-rmt

[![Workflow Status](https://github.com/yast/yast-rmt/workflows/CI/badge.svg?branch=master)](
https://github.com/yast/yast-rmt/actions?query=branch%3Amaster)
[![Coverage Status](https://coveralls.io/repos/github/SUSE/yast2-rmt/badge.svg?branch=master)](https://coveralls.io/github/SUSE/yast2-rmt?branch=master)
[![Maintainability](https://api.codeclimate.com/v1/badges/672b5ba57176d8b4be53/maintainability)](https://codeclimate.com/github/SUSE/yast2-rmt/maintainability)

Provides the YaST module to configure the Repository Mirroring Tool ([RMT](https://github.com/SUSE/rmt)) Server.

## Development

First read the excellent tutorial [:green_book: Creating the YaST journalctl module](http://yast.opensuse.org/yast-journalctl-tutorial/) to learn the basics about YaST module development.

### Running the module

`yast2-ruby-bindings` RPM package is not available as a gem, YaST runs on the default system-wide Ruby interpreter only (available in the OSS repository).

There different ways to run the module:

* `rake run` — by default starts Qt interface if it is available;
* `Y2DIR=src/ /usr/sbin/yast2 rmt` — same as above;
* `DISPLAY= rake run` — forces to run in ncurses mode;
* `Y2DIR=src/ /usr/sbin/yast2 --ncurses rmt` — same as above.

### Running tests

It is possible to run the specs in a Docker container:

```
docker build -t yast-rmt-image .
docker run -it yast-rmt-image rspec
```

### Resources

- [YaST Style Guide](https://en.opensuse.org/openSUSE:YaST_style_guide)
- [YaST Localization](https://yastgithubio.readthedocs.io/en/latest/localization/)
