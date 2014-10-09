# Steve Klabnik, "Functional Reactive Programming with Frappucino"
## Keynote, EuRuKo 2013
## https://www.youtube.com/watch?v=0qv3hWgC950

- Frappucino is irresponsbile ruby

- "there will be live coding - because that always goes wrong. so that's fun."

- [linguistic relativity](http://en.wikipedia.org/wiki/Linguistic_relativity): "The principle of linguistic relativity holds that the structure of a language affects the ways in which its respective speakers conceptualize their world, i.e. their world view, or otherwise influences their cognitive processes."
  - (strong) language defines the way we think
  - (weak) language makes it more probable <-- scientifically valid

  tl;dr langauge shapes but does not determine what we do
- process contrains the way we build stuff (responsible mode)
- Roman Numeral Kata

- FRP is very good for user interfaces
- turn back time: Shoes!

- FRP in haskell - you can model GUIs in a way that makes Haskell sense
- 2 parts: functional + reactive

- bacon.js
- "now that i have a good name for a gem i have to make it"

### Reactive Programming
- (functional, functions as a first class concept)
- dataflows as a first class concept
- flwos of data maniulated by functions as a model of programming

- what is a dataflow?
- a= 5, b=a+6, b = 11, a = 6, b = 11 (not reactive)
- a= 5, b=a+6, b = 11, a = 6, b = 12 (reactive)
- VERY DECLARATIVE
- inputs
- streams of events out of inputs
- run through functions
- bind their results to outputs

#### language
- a and b are *time varying values*, *behavior/signal* (variables changes over time)
- *events*, happens MANY times (GUI sense - e.g. on click events)
- *switching*: reacting to those events

- have stuff that generates events
- stuff that processes those events
- time varying values that show the output

- WATCH: philip roberts on baconjs http://vimeo.com/68987289

#### frappucino
- require stream
- make an event happen, class button function push emits
- make a stream Frappucino::Stream.new(button), stream receives any events the object passed generates
- the event is whatever gets emitted into the stream
- frappucino allows you to do enumerable methods on streams

#### in rails?
- replace callback system?
- after you fetch a record, make the record a stream? uh no still need a call back

#### in pure ruby?
- declaratively type in your business logic
- 1 place that describes the entire logic of the application

- haskell technique learned at a javascript conf now teaching in ruby land
- "people should learn every programming language because they are interesting and exciting"

#### in javascript?
- put an AJAX request in a stream
- does all the calculation, request in background 
- only blocks when fetching
- put a future in, maybe using [celluloid](https://celluloid.io/) ??






