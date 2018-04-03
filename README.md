# hindent [![Hackage](https://img.shields.io/hackage/v/hindent.svg?style=flat)](https://hackage.haskell.org/package/hindent) [![Build Status](https://travis-ci.org/commercialhaskell/hindent.png)](https://travis-ci.org/commercialhaskell/hindent)

Haskell pretty printer for RV

To run it on our own tests file:

```
stack build --profile && cat tests/test.in | stack exec hindent -- --indent-size 4 > tests/test.golden.new && diff tests/test.golden.new tests/test.golden
```

To run it on an entire project:

```
for f in `find . -name '*.hs'`; do cat $f | ~/runtime-verification/others/hindent/.stack-work/dist/x86_64-linux/Cabal-1.24.2.0/build/hindent/hindent --indent-size 4 > $f.tmp; rm $f; mv $f.tmp $f; done
```

One can also try the TESTS.md file.

Also see the original hindent [![documentation](https://github.com/commercialhaskell/hindent/blob/master/README.md)].
