# bdoc

A zero-dependency package which vendors [JSDoc][jsdoc] and all of its
dependencies for security and simplicity.

bdoc follows the same versioning scheme as jsdoc: e.g. `bdoc@3.5.5` should be
equivalent to `jsdoc@3.5.5`.

## Reasoning

bdoc is simply a snapshot of the official jsdoc NPM package. It was
specifically created for the [bcoin] development cycle. Bcoin is a
cryptocurrency project whose devs and users are particularly target-able for
certain kinds of package attacks like the one seen on the `event-stream`
package. As such, we seek to minimize the NPM attack surface.

### Why not use shrinkwrap?

Bundling the dependencies directly allows one to clone directly from github
without having to run `npm install`. We are aiming to minimize reliance on NPM
altogether.

### Why not bundle it?

JSDoc is difficult to bundle into a single file due to its use of dynamic
requires. Until someone takes the time to rid the entire codebase of all
dynamic requires, this is the best we can do.

## Usage

Note that this module will provide the `jsdoc` command. This will conflict
with the regular `jsdoc` install.

``` bash
$ jsdoc -h
```

## License

JSDoc license

```
JSDoc 3 is free software, licensed under the Apache License, Version 2.0 (the
"License"). Commercial and non-commercial use are permitted in compliance with
the License.

Copyright (c) 2011-present Michael Mathews <micmath@gmail.com> and the
[contributors to JSDoc](https://github.com/jsdoc3/jsdoc/graphs/contributors).
All rights reserved.

You may obtain a copy of the License at:
http://www.apache.org/licenses/LICENSE-2.0

In addition, a copy of the License is included with this distribution.

As stated in Section 7, "Disclaimer of Warranty," of the License:

> Licensor provides the Work (and each Contributor provides its Contributions)
> on an "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either
> express or implied, including, without limitation, any warranties or
> conditions of TITLE, NON-INFRINGEMENT, MERCHANTABILITY, or FITNESS FOR A
> PARTICULAR PURPOSE. You are solely responsible for determining the
> appropriateness of using or redistributing the Work and assume any risks
> associated with Your exercise of permissions under this License.

The source code for JSDoc 3 is available at:
https://github.com/jsdoc3/jsdoc

# Third-Party Software #

JSDoc 3 includes or depends upon the following third-party software, either in
whole or in part. Each third-party software package is provided under its own
license.

## MIT License ##

Several of the following software packages are distributed under the MIT
license, which is reproduced below:

> Permission is hereby granted, free of charge, to any person obtaining a copy
> of this software and associated documentation files (the "Software"), to deal
> in the Software without restriction, including without limitation the rights
> to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
> copies of the Software, and to permit persons to whom the Software is
> furnished to do so, subject to the following conditions:
>
> The above copyright notice and this permission notice shall be included in all
> copies or substantial portions of the Software.
>
> THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
> IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
> FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
> AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
> LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
> OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
> SOFTWARE.

## Google Code Prettify ##

Google Code Prettify is distributed under the Apache License 2.0, which is
included with this package.

Copyright (c) 2006 Google Inc.

The source code for Google Code Prettify is available at:
https://code.google.com/p/google-code-prettify/

## Jasmine ##

Jasmine is distributed under the MIT license, which is reproduced above.

Copyright (c) 2008-2011 Pivotal Labs.

The source code for Jasmine is available at:
https://github.com/pivotal/jasmine

## jasmine-node ##

jasmine-node is distributed under the MIT license, which is reproduced above.

Copyright (c) 2010 Adam Abrons and Misko Hevery (http://getangular.com).

The source code for jasmine-node is available at:
https://github.com/mhevery/jasmine-node

## Open Sans ##

Open Sans is distributed under the Apache License 2.0, which is
included with this package.

Copyright (c) 2010-2011, Google Inc.

This typeface, including the complete set of variations, are available at:
http://www.google.com/fonts/specimen/Open+Sans

## Tomorrow Theme for Google Code Prettify ##

The Tomorrow Theme for Google Code Prettify is distributed under the MIT
license, which is reproduced above.

Copyright (c) 2016 Yoshihide Jimbo.

The source code for the Tomorrow Theme is available at:
https://github.com/jmblog/color-themes-for-google-code-prettify
```

bdoc license

```
This software is licensed under the MIT License.

Copyright (c) 2018, Christopher Jeffrey (https://github.com/chjj)

Permission is hereby granted, free of charge, to any person obtaining a copy of
this software and associated documentation files (the "Software"), to deal in
the Software without restriction, including without limitation the rights to
use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies
of the Software, and to permit persons to whom the Software is furnished to do
so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

[jsdoc]: http://usejsdoc.org/
[bcoin]: https://github.com/bcoin-org
