# util.log
![lint status](https://github.com/bardcollege/util.log/actions/workflows/lint.yml/badge.svg)

Basic set of dependencies and configuration to get logging working. Custom
helper macros are provided in `bard.util.log`.

## Usage

Leiningen dependency:
```clojure
[bard/util.log "0.1.4"]
```

Clojure [tools.logging](https://github.com/clojure/tools.logging) is included
as a dependency; for the majority of operations, it should suffice:
```clojure
(ns some-ns
  (:require
     [clojure.tools.logging :as log]))
```

For special use cases, use the macros in `idm.log`; generally these are
referred by name, e.g.:
```clojure
(ns some-ns
  (:require
    [clojure.tools.logging :as log]
    [bard.util.log :refer [passf]]))
```

## Configuration
If you need to configure the underlying log engine (Log4j2), simply copy
[`log4j2.yml`](resources/log4j2.yml) into your classpath (i.e., `resources/`)
and make requisite changes - it will override the one provided here.


## License

Copyright © 2021 Bard College

This program and the accompanying materials are made available under the
terms of the Eclipse Public License 2.0 which is available at
http://www.eclipse.org/legal/epl-2.0.

This Source Code may also be made available under the following Secondary
Licenses when the conditions for such availability set forth in the Eclipse
Public License, v. 2.0 are satisfied: GNU General Public License as published by
the Free Software Foundation, either version 2 of the License, or (at your
option) any later version, with the GNU Classpath Exception which is available
at https://www.gnu.org/software/classpath/license.html.
