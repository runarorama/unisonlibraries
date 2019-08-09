### New Functions

``` Idris
List.break : (a ->{𝕖} .base.Boolean) -> [a] ->{𝕖} ([a], [a])
List.chunk : .base.Nat -> [a] -> [[a]]
List.concatenate : [[a]] -> [a]
List.dropRight : [a] -> [a] -> [a]
List.dropWhile : (a ->{𝕖} .base.Boolean) -> [a] ->{𝕖} [a]
List.filter : (a ->{𝕖} .base.Boolean) -> [a] ->{𝕖} [a]
List.first : [a] -> .base.Optional a
List.head : [a] -> .base.Optional a
List.init : [a] -> .base.Optional [a]
List.intercalate : [a] -> [[a]] -> [a]
List.intersperse : a -> [a] -> [a]
List.isEmpty : [a] -> .base.Boolean
List.last : [a] -> .base.Optional a
List.replicate : .base.Nat -> a -> [a]
List.span : (a ->{𝕖} .base.Boolean) -> [a] ->{𝕖} ([a], [a])
List.splitAt : .base.Nat -> [a] -> ([a], [a])
List.tail : [a] -> .base.Optional [a]
Search.findIndex : (a ->{𝕖} .base.Boolean)
                   -> [a]
                   ->{𝕖} .base.Optional .base.Nat
Search.findLastIndex : (a ->{𝕖} .base.Boolean)
                       -> [a]
                       ->{𝕖} .base.Optional .base.Nat
Tuple.curry : (.base.Tuple a b ->{𝕖} c) -> a -> b ->{𝕖} c
Tuple.uncurry : (a ->{𝕖} b ->{𝕖} c) -> .base.Tuple a b ->{𝕖} c
flip : (a ->{𝕖} b ->{𝕖} c) -> b -> a ->{𝕖} c
```

### Tests

``` Idris
tests.List.filter.constFalseIsEmpty : [.base.Test.Result]
tests.List.filter.constTrueIsIdentity : [.base.Test.Result]
tests.List.gens.nonEmpty : '{.test.v1.Gen} [.base.Nat]
tests.List.head.headOfCons : [.base.Test.Result]
tests.List.head.headOfEmpty : [.base.Test.Result]
tests.List.init.initOfEmpty : [.base.Test.Result]
tests.List.init.initOfSnoc : [.base.Test.Result]
tests.List.isEmpty.consIsNonempty : [.base.Test.Result]
tests.List.isEmpty.emptyIsEmpty : [.base.Test.Result]
tests.List.last.lastOfEmpty : [.base.Test.Result]
tests.List.last.lastOfSnoc : [.base.Test.Result]
tests.List.tail.tailOfCons : [.base.Test.Result]
tests.List.tail.tailOfEmpty : [.base.Test.Result]
```
