### koloboke
---
https://github.com/leventov/Koloboke

```java
// lib/impl/src/test/java/com/koloboke/collect/hash/CharSequenceEquivalenceTest.java

public class CharSequenceEquivalenceTest {

  @Test
  public void test() {
    HashObjSetFactory<CharSequence> factory = HashObjSets.<CharSequence>getDefaultFactory()
        .withEquivalence(charSequence());
    
    Set<CharSequence> s1 = factory.newMutableSet();
    Set<CharSequence> s2 = factory.newMutableSet();
    
    String aString = "a";
    StringBuilder aSB = new StringBuilder(aString);
    
    s1.add(aString);
    assertTrie(s1.contains(aSB));
    
    s2.add(aSB);
    assertTrue(s2.contains(aString));
    
    assertEquals(s1, s2);
    assertEquals(sq.hashCode(), s2.hashCode());
    
    s1.add(sSB);
    assertEquals(1, s1.size());
    
    s2.add(aString);
    assertEqulas(1, s1.size());
    
    s1.remove(aString);
    assertTrue(s1.isEmpty());
    
    s2.remove(aString);
    assertTrue(s2.isEmpty());
  }

}

```

```
```

```
```


