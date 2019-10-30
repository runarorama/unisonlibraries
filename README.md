### New Functions

``` Idris
1.  Float.pi : Float
2.  Int.^ : Int -> Nat -> Int
3.  Int.pow : Int -> Nat -> Int
4.  List.all : (a ->{𝕖} Boolean) -> [a] ->{𝕖} Boolean
5.  List.any : (a ->{𝕖} Boolean) -> [a] ->{𝕖} Boolean
6.  List.break : (a ->{𝕖} Boolean) -> [a] ->{𝕖} ([a], [a])
7.  List.chunk : Nat -> [a] -> [[a]]
8.  List.concatenate : [[a]] -> [a]
9.  List.dropRight : [a] -> [a] -> [a]
10. List.dropWhile : (a ->{𝕖} Boolean) -> [a] ->{𝕖} [a]
11. List.filter : (a ->{𝕖} Boolean) -> [a] ->{𝕖} [a]
12. List.first : [a] -> Optional a
13. List.head : [a] -> Optional a
14. List.init : [a] -> Optional [a]
15. List.intercalate : [a] -> [[a]] -> [a]
16. List.intersect : [a] -> [a] -> [a]
17. List.intersectBy : (a ->{𝕖} a ->{𝕖} Boolean) -> [a] -> [a] ->{𝕖} [a]
18. List.intersperse : a -> [a] -> [a]
19. List.isEmpty : [a] -> Boolean
20. List.last : [a] -> Optional a
21. List.replicate : Nat -> a -> [a]
22. List.span : (a ->{𝕖} Boolean) -> [a] ->{𝕖} ([a], [a])
23. List.splitAt : Nat -> [a] -> ([a], [a])
24. List.tail : [a] -> Optional [a]
25. List.takeWhile : (a ->{𝕖} Boolean) -> [a] ->{𝕖} [a]
26. Nat.^ : Nat -> Nat -> Nat
27. Nat.pow : Nat -> Nat -> Nat
28. Search.findIndex : (a ->{𝕖} Boolean) -> [a] ->{𝕖} Optional Nat
29. Search.findLastIndex : (a ->{𝕖} Boolean) -> [a] ->{𝕖} Optional Nat
30. Tuple.curry : ((a, b) ->{𝕖} c) -> a -> b ->{𝕖} c
31. Tuple.schönfinkel : ((a, b) ->{𝕖} c) -> a -> b ->{𝕖} c
32. Tuple.uncurry : (a ->{𝕖} b ->{𝕖} c) -> (a, b) ->{𝕖} c
33. Tuple.unschönfinkel : (a ->{𝕖} b ->{𝕖} c) -> (a, b) ->{𝕖} c
34. Universal.!= : a -> a -> Boolean
35. Universal.max : a -> a -> a
36. Universal.min : a -> a -> a
37. asTypeOf : a -> a -> a
38. bind : (a ->{𝕖} b ->{𝕖} c) -> (b ->{𝕖} a) -> b ->{𝕖} c
39. contains : [a] -> a -> Boolean
40. flip : (a ->{𝕖} b ->{𝕖} c) -> b -> a ->{𝕖} c
41. fuse : (r ->{𝕖} a ->{𝕖} b) -> (r ->{𝕖} a) -> r ->{𝕖} b
42. iterate : Nat -> (a ->{𝕖} a) -> a ->{𝕖} [a]
43. iterateUntil : (a ->{𝕖} Boolean) -> (a ->{𝕖} a) -> a ->{𝕖} [a]
44. iterateWhile : (a ->{𝕖} Boolean) -> (a ->{𝕖} a) -> a ->{𝕖} [a]
45. scanLeft : (b ->{𝕖} a ->{𝕖} b) -> b -> [a] ->{𝕖} [b]
46. scanRight : (a ->{𝕖} b ->{𝕖} b) -> b -> [a] ->{𝕖} [b]
65. until : (a ->{𝕖} Boolean) -> (a ->{𝕖} a) -> a ->{𝕖} a
66. verschmelzen : (r ->{𝕖} a ->{𝕖} b) -> (r ->{𝕖} a) -> r ->{𝕖} b
67. while : (a ->{𝕖} Boolean) -> (a ->{𝕖} a) -> a ->{𝕖} a
68. xor : Boolean -> Boolean -> Boolean
```

### Tests

``` Idris
47. tests.List.filter.constFalseIsEmpty : [Test.Result]
48. tests.List.filter.constTrueIsIdentity : [Test.Result]
49. tests.List.gens.nonEmpty : '{test.v1.Gen} [Nat]
50. tests.List.head.headOfCons : [Test.Result]
51. tests.List.head.headOfEmpty : [Test.Result]
52. tests.List.init.initOfEmpty : [Test.Result]
53. tests.List.init.initOfSnoc : [Test.Result]
54. tests.List.intersect.spec : [Test.Result]
55. tests.List.isEmpty.consIsNonempty : [Test.Result]
56. tests.List.isEmpty.emptyIsEmpty : [Test.Result]
57. tests.List.last.lastOfEmpty : [Test.Result]
58. tests.List.last.lastOfSnoc : [Test.Result]
59. tests.List.replicate.length : [Test.Result]
60. tests.List.tail.tailOfCons : [Test.Result]
61. tests.List.tail.tailOfEmpty : [Test.Result]
62. tests.Nat.pow.expansion : [Test.Result]
63. tests.Nat.pow.homomorphism : [Test.Result]
64. tests.Nat.smallNat : ∀ (). () ->{test.v1.Gen} Nat
```

