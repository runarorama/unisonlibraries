# Various libraries for Unison

This is a collection of [Unison](http://unisonweb.org) functions and data types not (yet) included in the [`.base` library](http://github.com/unisonweb/base).

## Installation

From the `ucm` prompt:

```
.> pull git@github.com:runarorama/unisonlibraries.git .lib
```

This will install the following into your codebase under the `.lib` namespace.

### New Functions

``` Idris
Float.pi : Float
Int.^ : Int -> Nat -> Int
Int.pow : Int -> Nat -> Int
List.all : (a ->{𝕖} Boolean) -> [a] ->{𝕖} Boolean
List.any : (a ->{𝕖} Boolean) -> [a] ->{𝕖} Boolean
List.break : (a ->{𝕖} Boolean) -> [a] ->{𝕖} ([a], [a])
List.chunk : Nat -> [a] -> [[a]]
List.concatenate : [[a]] -> [a]
List.dropRight : [a] -> [a] -> [a]
List.dropWhile : (a ->{𝕖} Boolean) -> [a] ->{𝕖} [a]
List.filter : (a ->{𝕖} Boolean) -> [a] ->{𝕖} [a]
List.first : [a] -> Optional a
List.head : [a] -> Optional a
List.init : [a] -> Optional [a]
List.intercalate : [a] -> [[a]] -> [a]
List.intersect : [a] -> [a] -> [a]
List.intersectBy : (a ->{𝕖} a ->{𝕖} Boolean) -> [a] -> [a] ->{𝕖} [a]
List.intersperse : a -> [a] -> [a]
List.isEmpty : [a] -> Boolean
List.last : [a] -> Optional a
List.replicate : Nat -> a -> [a]
List.span : (a ->{𝕖} Boolean) -> [a] ->{𝕖} ([a], [a])
List.splitAt : Nat -> [a] -> ([a], [a])
List.tail : [a] -> Optional [a]
List.takeWhile : (a ->{𝕖} Boolean) -> [a] ->{𝕖} [a]
Nat.^ : Nat -> Nat -> Nat
Nat.pow : Nat -> Nat -> Nat
Search.findIndex : (a ->{𝕖} Boolean) -> [a] ->{𝕖} Optional Nat
Search.findLastIndex : (a ->{𝕖} Boolean) -> [a] ->{𝕖} Optional Nat
Text.fromBytes : Bytes -> Text
Text.join : Text -> [Text] -> Text
Text.length : Text -> Nat
Text.split : Text -> Text -> [Text]
Text.startsWith : Text -> Text -> Boolean
Text.toBytes : Text -> Bytes
Tuple.curry : ((a, b) ->{𝕖} c) -> a -> b ->{𝕖} c
Tuple.schönfinkel : ((a, b) ->{𝕖} c) -> a -> b ->{𝕖} c
Tuple.uncurry : (a ->{𝕖} b ->{𝕖} c) -> (a, b) ->{𝕖} c
Tuple.unschönfinkel : (a ->{𝕖} b ->{𝕖} c) -> (a, b) ->{𝕖} c
Universal.!= : a -> a -> Boolean
Universal.max : a -> a -> a
Universal.min : a -> a -> a
asTypeOf : a -> a -> a
bind : (a ->{𝕖} b ->{𝕖} c) -> (b ->{𝕖} a) -> b ->{𝕖} c
contains : [a] -> a -> Boolean
flip : (a ->{𝕖} b ->{𝕖} c) -> b -> a ->{𝕖} c
fuse : (r ->{𝕖} a ->{𝕖} b) -> (r ->{𝕖} a) -> r ->{𝕖} b
iterate : Nat -> (a ->{𝕖} a) -> a ->{𝕖} [a]
iterateUntil : (a ->{𝕖} Boolean) -> (a ->{𝕖} a) -> a ->{𝕖} [a]
iterateWhile : (a ->{𝕖} Boolean) -> (a ->{𝕖} a) -> a ->{𝕖} [a]
scanLeft : (b ->{𝕖} a ->{𝕖} b) -> b -> [a] ->{𝕖} [b]
scanRight : (a ->{𝕖} b ->{𝕖} b) -> b -> [a] ->{𝕖} [b]
until : (a ->{𝕖} Boolean) -> (a ->{𝕖} a) -> a ->{𝕖} a
verschmelzen : (r ->{𝕖} a ->{𝕖} b) -> (r ->{𝕖} a) -> r ->{𝕖} b
while : (a ->{𝕖} Boolean) -> (a ->{𝕖} a) -> a ->{𝕖} a
xor : Boolean -> Boolean -> Boolean
```

### Tests

``` Idris
tests.List.filter.constFalseIsEmpty : [Test.Result]
tests.List.filter.constTrueIsIdentity : [Test.Result]
tests.List.gens.nonEmpty : '{test.v1.Gen} [Nat]
tests.List.head.headOfCons : [Test.Result]
tests.List.head.headOfEmpty : [Test.Result]
tests.List.init.initOfEmpty : [Test.Result]
tests.List.init.initOfSnoc : [Test.Result]
tests.List.intersect.spec : [Test.Result]
tests.List.isEmpty.consIsNonempty : [Test.Result]
tests.List.isEmpty.emptyIsEmpty : [Test.Result]
tests.List.last.lastOfEmpty : [Test.Result]
tests.List.last.lastOfSnoc : [Test.Result]
tests.List.replicate.length : [Test.Result]
tests.List.tail.tailOfCons : [Test.Result]
tests.List.tail.tailOfEmpty : [Test.Result]
tests.Nat.pow.expansion : [Test.Result]
tests.Nat.pow.homomorphism : [Test.Result]
tests.Nat.smallNat : ∀ (). () ->{test.v1.Gen} Nat
tests.Text.fromBytes : Bytes -> Text
tests.Text.join : Text -> [Text] -> Text
tests.Text.length : Text -> Nat
tests.Text.split : Text -> Text -> [Text]
tests.Text.startsWith : Text -> Text -> Boolean
tests.Text.toBytes : Text -> Bytes
```

