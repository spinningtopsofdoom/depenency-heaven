Diagnosing CLojure CLI
`-S` flags

!SLIDE

`clj -Sverbose`  gives confuration information to the console

```
version      = 1.9.0.326
install_dir  = /usr/local/lib/clojure
config_dir   = /home/peter/.clojure
config_paths = /usr/local/lib/clojure/deps.edn /home/peter/.clojure/deps.edn deps.edn
cache_dir    = /home/peter/.clojure/.cpcache
cp_file      = /home/peter/.clojure/.cpcache/1199981639.cp
```

!SLIDE

`clj -Stree` prints out a dependency tree

```
org.clojure/clojure 1.9.0
  org.clojure/spec.alpha 0.1.143
  org.clojure/core.specs.alpha 0.1.24
```

!SLIDE

`clj -Spath` lists off the entire class path

```
src:/home/peter/.m2/repository/org/clojure/clojure/1.9.0/clojure-1.9.0.jar:/home/peter/.m2/repository/org/clojure/spec.alpha/0.1.143/spec.alpha-0.1.143.jar:/home/peter/.m2/repository/org/clojure/core.specs.alpha/0.1.24/core.specs.alpha-0.1.24.jar
```

!SLIDE

`clj -Sresolve-tags`

Resolves the sha coordinate of a git tag and updates the `deps.edn` with the sha coordinate

!SLIDE

`clj -Spom`

Transforms dependency and path information into a `pom.xml`
