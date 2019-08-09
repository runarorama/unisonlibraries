### New Functions

``` Idris
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
List.intersperse : a -> [a] -> [a]
List.isEmpty : [a] -> Boolean
List.last : [a] -> Optional a
List.replicate : Nat -> a -> [a]
List.span : (a ->{𝕖} Boolean) -> [a] ->{𝕖} ([a], [a])
List.splitAt : Nat -> [a] -> ([a], [a])
List.tail : [a] -> Optional [a]
Search.findIndex : (a ->{𝕖} Boolean)
                   -> [a]
                   ->{𝕖} Optional Nat
Search.findLastIndex : (a ->{𝕖} Boolean)
                       -> [a]
                       ->{𝕖} Optional Nat
Tuple.curry : (Tuple a b ->{𝕖} c) -> a -> b ->{𝕖} c
Tuple.uncurry : (a ->{𝕖} b ->{𝕖} c) -> Tuple a b ->{𝕖} c
flip : (a ->{𝕖} b ->{𝕖} c) -> b -> a ->{𝕖} c
```

### Tests

``` Idris
tests.List.filter.constFalseIsEmpty : [Test.Result]
tests.List.filter.constTrueIsIdentity : [Test.Result]
tests.List.gens.nonEmpty : '{.test.v1.Gen} [Nat]
tests.List.head.headOfCons : [Test.Result]
tests.List.head.headOfEmpty : [Test.Result]
tests.List.init.initOfEmpty : [Test.Result]
tests.List.init.initOfSnoc : [Test.Result]
tests.List.isEmpty.consIsNonempty : [Test.Result]
tests.List.isEmpty.emptyIsEmpty : [Test.Result]
tests.List.last.lastOfEmpty : [Test.Result]
tests.List.last.lastOfSnoc : [Test.Result]
tests.List.tail.tailOfCons : [Test.Result]
tests.List.tail.tailOfEmpty : [Test.Result]
```

