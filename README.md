# Type Rodeo

1. Implement `Semigroup`, `Functor`, `Applicative`, `Monad`, `Foldable`, and `Traversable` for:
```haskell
data List a = Nil | Cons a (List a)
```
2. Implement `Functor`, `Applicative`, and `Monad` for:
```haskell
newtype StateT s m a =
  StateT
    { runStateT :: s -> m (a,s)
    }
```
3. Implement `Functor`, `Applicative`, and `Monad` for:
```haskell
newtype ContT m a =
  ContT
    { runContT :: forall r. (a -> m r) -> m r
    }
```
