QHttp - Qompoter Wrapper
===========

This [Qompoter](https://github.com/Fylhan/qompoter) wrapper helps to integrate [azadkuh/qhttp](https://github.com/azadkuh/qhttp), a light-weight and asynchronous HTTP library (both server & client) in Qt/C++ , using [Qompoter](https://github.com/Fylhan/qompoter).

This wrapper targets two versions of QHttp: the original one by [azadkuh](https://github.com/azadkuh/qhttp) requiring Qt5 and C++14, and a forked one by [oliviermaridat](https://github.com/oliviermaridat/qhttp) requiring only Qt5 and C++11.

Usage
-----------

To use [azadkuh/qhttp](https://github.com/azadkuh/qhttp) in a project, simply create (or update) the following `qompoter.json` file in your project root directoy:


```json
{
    "name": "acme/my-project",
    "require": {
        "qompoter/qhttp-wrapper": "version-3.*"
    }
}
```

Using `version-X` will target the version of [azadkuh](https://github.com/azadkuh/qhttp), using `vX` will target the version of  [oliviermaridat](https://github.com/oliviermaridat/qhttp).

Then, download and install `http-parser` using Qompoter:

```bash
qompoter install
```

*Note: to install Qompoter on your machine, use `npm install -g qompoter` or check [Qompoter documentation](https://github.com/Fylhan/qompoter/blob/master/README.md#installation).*

That's it! Qompoter has downloaded `qhttp` into the `vendor` directory, you can now include `vendor.pri` in the `.pro` file of your project, and select `qhttp` as a dependency:

```qmake
CONFIG += qhttp-server # To enable QHttp server module
CONFIG += qhttp-client # To enable QHttp client module
#CONFIG += qhttp # Uncomment to enable both QHttp client and server modules in one line
include(vendor/vendor.pri)
```

Let's start coding! Check [azadkuh/qhttp examples](https://github.com/azadkuh/qhttp#sample-codes).
