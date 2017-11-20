

```kotlin
private inline fun <reified T : Any> reifiedEquals() = eq(T::class.java)

verify(myService).getFoos(eq(List<Foo>::class.java) // compiler error, due to type erasure this isn't allowed
verify(myService).getFoos(reifiedEquals<List<Patient>>()) // just fine
```
