![gophish logo](https://raw.github.com/raginx/gophish/master/static/images/gophish_purple.png)

Gophish (fork)
=====================

![Build Status](https://github.com/raginx/gophish/workflows/CI/badge.svg)

Gophish: Open-Source Phishing Toolkit

[Gophish](https://github.com/raginx/gophish/) is an open-source phishing toolkit designed for businesses and penetration testers. It provides the ability to quickly and easily setup and execute phishing engagements and security awareness training.

This is an actively maintained fork of the [upstream project](https://github.com/gophish/gophish), which has had no commits since September 2024. This fork tracks dependency/security updates and selectively pulls in fixes and features from the upstream issue and PR backlog.

### Install

This fork does not currently publish binary releases. Build from source (see below). If you're looking for official upstream binaries instead, see the [upstream releases page](https://github.com/gophish/gophish/releases/).

### Building From Source
**Requires Go 1.25 or above.**

```
git clone https://github.com/raginx/gophish.git
cd gophish
go build
```

After this, you should have a binary called ```gophish``` in the current directory.

The built frontend assets (`static/js/dist/`, `static/css/dist/`) are checked
into git, so this is all you need for a normal build. If you change anything
under `static/js/src/` or `static/css/`, rebuild them with:
```
npm install
npm run build
```

### Docker
You can also use upstream Gophish via the official Docker container [here](https://hub.docker.com/r/gophish/gophish/). This fork does not currently publish its own Docker images.

### Setup
After running the Gophish binary, open an Internet browser to https://localhost:3333 and login with the default username and password listed in the log output.
e.g.
```
time="2020-07-29T01:24:08Z" level=info msg="Please login with the username admin and the password 4304d5255378177d"
```

### Documentation

Since this fork tracks upstream Gophish closely, the [upstream documentation](http://getgophish.com/documentation) mostly applies.

### Issues

Found a bug specific to this fork? Please [file an issue](https://github.com/raginx/gophish/issues/new) here. For issues that also affect upstream Gophish, consider checking the [upstream issue tracker](https://github.com/gophish/gophish/issues) as well.

### Contact

reinhard [at] westerholt [dot] me

### License
```
Gophish - Open-Source Phishing Framework

The MIT License (MIT)

Copyright (c) 2013 - 2020 Jordan Wright
Copyright (c) 2026 Reinhard Westerholt (fork-specific modifications)

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software ("Gophish Community Edition") and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.
```
