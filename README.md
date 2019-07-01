# Type Rodeo

1. Implement `Semigroup`, `Functor`, `Applicative`, `Monad`, `Foldable`, and `Traversable` for:
```haskell
data List a =
    Nil 
  | Cons a (List a)
```
2. Determine which of the following are `Covariant`, `Contravariant`, or `Invariant` and implement the instances
```
newtype A a = A (a -> a)

newtype B a = B ((Int -> a) -> Int)

newtype C a = C ((a -> Int) -> Int)
```
3. Implement `Functor`, `Applicative`, and `Monad` for:
```haskell
newtype StateT s m a =
  StateT
    { runStateT :: s -> m (a,s)
    }
```
4. Implement `Functor`, `Applicative`, and `Monad` for:
```haskell
newtype ContT m a =
  ContT
    { runContT :: forall r. (a -> m r) -> m r
    }
```
