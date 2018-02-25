How to use Clojure CLI

!SLIDE

Dependency information conatining in top level `deps.edn`

Can access maven, clojars, git repositories, and local projects

```
{ :deps
  {clj-time  {:mvn/version "0.14.2"}
   org.clojure/clojurescript {
     :git/url "https://github.com/clojure/clojurescript.git"
     :sha "2f9ff09ea3046fc873ebeb1df774e1ceb7719174" }
   time-lib {:local/root "/path/to/time-lib"}
        }}
```

!SLIDE

Running `clj` at the command line will load those dependencies

!SLIDE
`-R` Adds on extra dependencies

```
{
:aliases
 {:bench {:extra-deps {criterium/criterium {:mvn/version "0.4.4"}}}}
 }
```

`clj -R:bench` adds criterium to dependencies

!SLIDE

Override dependencies

```
{
:aliases
{:1.7 {:override-deps {org.clojure/clojure {:mvn/version "1.7.0"}}}}
 }
```

`clj -R:1.7` adds replaces Clojure 1.9 with Clojure 1.7

!SLIDE

Class paths

```
{:paths ["src"]
:aliases
 {:test {:extra-paths ["test"]}}
 }
```

`clj -C:test` loads `src` and `test` on the class path

!SLIDE

`-A` adds all options of an aliad

```
{
:aliases
{:1.7-test {:override-deps {org.clojure/clojure {:mvn/version "1.7.0"}}
            :extra-paths ["test"]}}
 }
```

`clj -A:1.7-test` loads `test` class path and set CLojure to 1.7
