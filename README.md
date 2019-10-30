### New Functions

``` Idris
  1.  Float.pi : .base.Float
  2.  Int.^ : .base.Int -> .base.Nat -> .base.Int
  3.  Int.pow : .base.Int -> .base.Nat -> .base.Int
  4.  List.all : (a ->{𝕖} .base.Boolean) -> [a] ->{𝕖} .base.Boolean
  5.  List.any : (a ->{𝕖} .base.Boolean) -> [a] ->{𝕖} .base.Boolean
  6.  List.break : (a ->{𝕖} .base.Boolean) -> [a] ->{𝕖} ([a], [a])
  7.  List.chunk : .base.Nat -> [a] -> [[a]]
  8.  List.concatenate : [[a]] -> [a]
  9.  List.dropRight : [a] -> [a] -> [a]
  10. List.dropWhile : (a ->{𝕖} .base.Boolean) -> [a] ->{𝕖} [a]
  11. List.filter : (a ->{𝕖} .base.Boolean) -> [a] ->{𝕖} [a]
  12. List.first : [a] -> .base.Optional a
  13. List.head : [a] -> .base.Optional a
  14. List.init : [a] -> .base.Optional [a]
  15. List.intercalate : [a] -> [[a]] -> [a]
  16. List.intersect : [a] -> [a] -> [a]
  17. List.intersectBy : (a ->{𝕖} a ->{𝕖} .base.Boolean) -> [a] -> [a] ->{𝕖} [a]
  18. List.intersperse : a -> [a] -> [a]
  19. List.isEmpty : [a] -> .base.Boolean
  20. List.last : [a] -> .base.Optional a
  21. List.replicate : .base.Nat -> a -> [a]
  22. List.span : (a ->{𝕖} .base.Boolean) -> [a] ->{𝕖} ([a], [a])
  23. List.splitAt : .base.Nat -> [a] -> ([a], [a])
  24. List.tail : [a] -> .base.Optional [a]
  25. List.takeWhile : (a ->{𝕖} .base.Boolean) -> [a] ->{𝕖} [a]
  26. Nat.^ : .base.Nat -> .base.Nat -> .base.Nat
  27. Nat.pow : .base.Nat -> .base.Nat -> .base.Nat
  28. Search.findIndex : (a ->{𝕖} .base.Boolean) -> [a] ->{𝕖} .base.Optional .base.Nat
  29. Search.findLastIndex : (a ->{𝕖} .base.Boolean) -> [a] ->{𝕖} .base.Optional .base.Nat
  30. Tuple.curry : ((a, b) ->{𝕖} c) -> a -> b ->{𝕖} c
  31. Tuple.schönfinkel : ((a, b) ->{𝕖} c) -> a -> b ->{𝕖} c
  32. Tuple.uncurry : (a ->{𝕖} b ->{𝕖} c) -> (a, b) ->{𝕖} c
  33. Tuple.unschönfinkel : (a ->{𝕖} b ->{𝕖} c) -> (a, b) ->{𝕖} c
  34. Universal.!= : a -> a -> .base.Boolean
  35. Universal.max : a -> a -> a
  36. Universal.min : a -> a -> a
  37. asTypeOf : a -> a -> a
  38. bind : (a ->{𝕖} b ->{𝕖} c) -> (b ->{𝕖} a) -> b ->{𝕖} c
  39. contains : [a] -> a -> .base.Boolean
  40. flip : (a ->{𝕖} b ->{𝕖} c) -> b -> a ->{𝕖} c
  41. fuse : (r ->{𝕖} a ->{𝕖} b) -> (r ->{𝕖} a) -> r ->{𝕖} b
  42. iterate : .base.Nat -> (a ->{𝕖} a) -> a ->{𝕖} [a]
  43. iterateUntil : (a ->{𝕖} .base.Boolean) -> (a ->{𝕖} a) -> a ->{𝕖} [a]
  44. iterateWhile : (a ->{𝕖} .base.Boolean) -> (a ->{𝕖} a) -> a ->{𝕖} [a]
  45. scanLeft : (b ->{𝕖} a ->{𝕖} b) -> b -> [a] ->{𝕖} [b]
  46. scanRight : (a ->{𝕖} b ->{𝕖} b) -> b -> [a] ->{𝕖} [b]
  47. tests.List.filter.constFalseIsEmpty : [.base.Test.Result]
  48. tests.List.filter.constTrueIsIdentity : [.base.Test.Result]
  49. tests.List.gens.nonEmpty : '{.base.test.v1.Gen} [.base.Nat]
  50. tests.List.head.headOfCons : [.base.Test.Result]
  51. tests.List.head.headOfEmpty : [.base.Test.Result]
  52. tests.List.init.initOfEmpty : [.base.Test.Result]
  53. tests.List.init.initOfSnoc : [.base.Test.Result]
  54. tests.List.intersect.spec : [.base.Test.Result]
  55. tests.List.isEmpty.consIsNonempty : [.base.Test.Result]
  56. tests.List.isEmpty.emptyIsEmpty : [.base.Test.Result]
  57. tests.List.last.lastOfEmpty : [.base.Test.Result]
  58. tests.List.last.lastOfSnoc : [.base.Test.Result]
  59. tests.List.replicate.length : [.base.Test.Result]
  60. tests.List.tail.tailOfCons : [.base.Test.Result]
  61. tests.List.tail.tailOfEmpty : [.base.Test.Result]
  62. tests.Nat.pow.expansion : [.base.Test.Result]
  63. tests.Nat.pow.homomorphism : [.base.Test.Result]
  64. tests.Nat.smallNat : ∀ (). () ->{.base.test.v1.Gen} .base.Nat
  65. until : (a ->{𝕖} .base.Boolean) -> (a ->{𝕖} a) -> a ->{𝕖} a
  66. verschmelzen : (r ->{𝕖} a ->{𝕖} b) -> (r ->{𝕖} a) -> r ->{𝕖} b
  67. while : (a ->{𝕖} .base.Boolean) -> (a ->{𝕖} a) -> a ->{𝕖} a
  68. xor : .base.Boolean -> .base.Boolean -> .base.Boolean
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

