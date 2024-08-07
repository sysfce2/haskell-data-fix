## 0.3.4

- Use quantified constraints superclasses for `Eq`, `Ord`, `NFData` and
  `Hashable Fix` instances, when available.

## 0.3.3

- Drop support for GHCs prior 8.6.5

## 0.3.2

- Add `(un)wrapFix/Mu/Nu`
- Support `transformers-0.6`

## 0.3.1

- Update bounds for GHC-9.0

## 0.3.0

- Rename `cata`, `ana` and `hylo` into `foldFix`, `unfoldFix` and `refold.
  Old names are now deprecated, and will be eventually removed.
  Similarly, rename monadic variants.
- Add `hoistFix` and `hoistFix'` function.
- Add `Hashable` and `NFData` instance.
  Latter is available only with `deepseq >=1.4.3.0`,
  which provides `NFData1` type-class
- Change `Eq`, `Ord`, `Show` and `Read` instances to use
  `Eq1`, `Ord1`, `Show1` and `Read1` instances of a base functor.
- Add least and greatest fixed point types, `Mu` and `Nu`.
- Drop requirement for `Applicative m` in monadic combinators,
  `Monad m` is enough.
- Remove `~>` alias for `refold` (`hylo`).
- Extend the GHC support window.
  There is nothing magical in this package.
- Mark `Data.Fix` as Trustworthy (Safe Haskell)
- Make `refold` (and `refoldM`) more efficient.
  This results in different effect ordering for `refoldM`.
