# serialization

Binary serialization for zepto datatypes.

All standard datatypes are currently supported, primitives are only
pickled by name (so if you are running a different version of zepto
with different native extensions loaded, it will fail to look them
up).

## Installation

```
zeps install hellerve/serialization
```

## Usage

The module exposes two functions `serialize` and `deserialize`.

```clojure
(import-all "serialization/serialization" "sz")

(sz:deserialize (sz:serialize [10 (20) "lol" #\a {#t} 1 2 b{1} #{1 2 3 4} :abc b]))
; => (10 (20) lol 'a' #(#t) 1 2 b{1} #{1: 2,  3: 4, } :abc b)
```

<hr/>

Have fun!
