# Advanced Formatting Test File
This file is intended for testing only

### Tables

 | **Dag** | **Volgorde** |
 | - | - |
 | Maandag | 01 |
 | Dinsdag | 02 |
 | Woensdag | 03 |

### Highlighting code
Python:
```python
i = 0
i += i
```

Java:
```java
public static void main(String args[]) {
  int i = -9
}
```

### Local (relative) linking
[Readme.md](/README.md) <!-- Case sensitive -->

[testfile mark](/testfilemark)

### Mathematical expressions
$\sqrt{3x-1}+(1+x)^2$

**The Cauchy-Schwarz Inequality**
$$\left( \sum_{k=1}^n a_k b_k \right)^2 \leq \left( \sum_{k=1}^n a_k^2 \right) \left( \sum_{k=1}^n b_k^2 \right)$$

### Combinations

| Apple | Pear |
| - | - |
| [google](www.google.com) | $\sqrt{3^x/7}+(1^{-x})^{log(2)}$ |

### 3D model
```stl
solid cube_corner
  facet normal 0.0 -1.0 0.0
    outer loop
      vertex 0.0 0.0 0.0
      vertex 1.0 0.0 0.0
      vertex 0.0 0.0 1.0
    endloop
  endfacet
  facet normal 0.0 0.0 -1.0
    outer loop
      vertex 0.0 0.0 0.0
      vertex 0.0 1.0 0.0
      vertex 1.0 0.0 0.0
    endloop
  endfacet
  facet normal -1.0 0.0 0.0
    outer loop
      vertex 0.0 0.0 0.0
      vertex 0.0 0.0 1.0
      vertex 0.0 1.0 0.0
    endloop
  endfacet
  facet normal 0.577 0.577 0.577
    outer loop
      vertex 1.0 0.0 0.0
      vertex 0.0 1.0 0.0
      vertex 0.0 0.0 1.0
    endloop
  endfacet
endsolid
```

### Image alignment
_Surrounded by text_ \
This is example text to illustrate something or rather, somewhat, text alignment, pineapple. More text is to be included, which may or not be useful considering a necessary thing with another specific thing.
<img align="right" src="images/fta_symbol_xor.png">
_Alignment should be broken with the following text/statement_
<br clear="right"/>
This text should have space above it. \
Or perhaps, this one.