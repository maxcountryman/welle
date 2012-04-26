# Welle, a Clojure client for Riak

Welle is a young idiomatic Clojure client for Riak built on top of the Riak Java driver.
Its API and code style closely follow other ClojureWerkz projects, namely [Neocons](https://github.com/michaelklishin/neocons), [Elastisch](https://github.com/clojurewerkz/elastisch)
and [Monger](https://github.com/michaelklishin/monger).

Welle is not the only Clojure client for Riak on the block: there is a client called [Sumo](https://github.com/reiddraper/sumo)
by one of Basho's engineers. If you are evaluating Welle, please consider Sumo as well.


## Project Goals

 * Be well maintained.
 * Be well documented.
 * Be well tested.
 * Target Clojure 1.3.0 and later from the ground up.
 * Integrate with libraries like clojure.data.json and Joda Time.
 * Support URI connections to be friendly to Heroku and other PaaS providers.
 * Learn from other clients like the Java and Ruby ones.


## Supported Features

 * Protocol Buffers and HTTP connection
 * Buckets: create, update, delete
 * Objects: put, fetch, delete
 * Secondary indexes (2i): indexing, index queries
 * Content-type based serialization of values in common formats (bytes, JSON, Clojure data/reader, UTF-8 text, gzipped JSON)


## Supported Clojure versions

Welle is built from the ground up for Clojure 1.3 and up. To store dates/instants with Clojure data serialization, Clojure 1.4.0
is the minimum required version because Clojure 1.3 reader cannot handle `java.util.Date` instances. As such, Clojure 1.4 is
recommended.


## Documentation & Examples

Welle is a young project and until 1.0 is released and documentation guides are written,
it may be challenging to use for anyone except the author. For code examples, see our test
suite.

Once documentation site is up, we will update this document.


## Community

To subscribe for announcements of releases, important changes and so on, please follow
[@ClojureWerkz](https://twitter.com/#!/clojurewerkz) on Twitter.



## Maven Artifacts

### Most Recent Release

With Leiningen:

    [com.novemberain/welle "1.0.0-alpha3"]


With Maven:

    <dependency>
      <groupId>com.novemberain</groupId>
      <artifactId>welle</artifactId>
      <version>1.0.0-alpha3</version>
    </dependency>



## This is a Work In Progress

Welle is very much a work in progress and right now, please keep this in mind.


## Continuous Integration

[![Continuous Integration status](https://secure.travis-ci.org/michaelklishin/welle.png)](http://travis-ci.org/michaelklishin/welle)

CI is hosted by [travis-ci.org](http://travis-ci.org)


## Development

Welle uses [Leiningen 2](https://github.com/technomancy/leiningen/blob/master/doc/TUTORIAL.md). Make
sure you have it installed and then run tests against all supported Clojure versions using

    lein2 ci test

Then create a branch and make your changes on it. Once you are done with your changes and all
tests pass, submit a pull request on Github.


## License

Copyright (C) 2011-2012 Michael S. Klishin

Distributed under the Eclipse Public License, the same as Clojure.
