# Using `clojure` and `clj`

!SLIDE

# `deps.edn`
## Contains dependencies, paths, aliases (profiles) and more

!SLIDE

# Dependencies

## Can access maven, clojars, git repositories, and local projects

    @@@clojure
    {:deps
      {clj-time  {:mvn/version "0.14.2"}
       org.clojure/clojurescript {
         :git/url "https://github.com/clojure/clojurescript.git"
         :sha "2f9ff09ea3046fc873ebeb1df774e1ceb7719174" }
       time-lib {:local/root "/path/to/time-lib"}}}

!SLIDE

# Class paths

    @@@clojure
    {:paths ["src" "public"]}

!SLIDE

# Aliases flags
* `-R` add or overwrite dependencies
* `-C` add on class paths
* `-A` both class path and dependency added

!SLIDE

# Extra Dependencies
## `clj -R:bench` adds criterium to dependencies

    @@@clojure
    {:aliases
     {:bench {:extra-deps {criterium/criterium {:mvn/version "0.4.4"}}}}}


!SLIDE

# Override dependencies
## `clj -R:1.7` adds replaces Clojure 1.9 with Clojure 1.7

    @@@clojure
    {:aliases
     {:1.7 {:override-deps {org.clojure/clojure {:mvn/version "1.7.0"}}}}}


!SLIDE

# Add Class Paths
## `clj -C:test` loads `src` and `test` on the class path

    @@@clojure
    {:aliases
     {:test {:extra-paths ["test"]}}}


!SLIDE

# Add all options of an alias
## `clj -A:1.7-test` loads `test` class path and set Clojure to 1.7

    @@@clojure
    {:aliases
     {:1.7-test
       {:override-deps {org.clojure/clojure {:mvn/version "1.7.0"}}
        :extra-paths ["test"]}}}

