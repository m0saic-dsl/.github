<p align="left">
  <a href="https://m0saic.io" target="_blank" rel="noopener noreferrer">
    <img src="m0.png" alt="m0saic" width="180" />
    <picture>
      <source media="(prefers-color-scheme: dark)" srcset="assets/logo/wordmark.svg">
      <source media="(prefers-color-scheme: light)" srcset="assets/logo/wordmark-dark.svg">
      <img src="assets/logo/wordmark-dark.svg" alt="m0saic" width="380"/>
    </picture>
  </a>
</p>

# m0 (m0saic DSL)

**m0** is a deterministic, integer-only rectangle layout algebra and canonical string encoding maintained by **m0saic LLC**.

It defines a minimal grammar for transforming a single rectangle into a structured, deterministic set of child rectangles with stable identity and exact geometry.

m0 is designed to be:

- Deterministic  
- Integer-precise  
- Human-authorable  
- O(N) in evaluation  
- Portable across runtimes  
- Semantically stable  

---

## Definition

Given:

- A root rectangle `(width, height)`  
- A valid m0 string  

Evaluation produces:

- A deterministic set of rectangles  
- Stable ordering  
- Stable identity  
- Exact integer geometry  
- No floating-point ambiguity  
- No runtime-dependent variation  

m0 produces **geometry only**.  
It does not assign meaning to rectangles.

---

## Scope

m0 intentionally does not define:

- Content measurement  
- Responsive layout behavior  
- Styling or rendering  
- Runtime-dependent layout  

It is a layout algebra, not a UI system.

---

## Composition Model

m0 defines deterministic geometry as a pure function of:

```
(root rectangle, m0 string) → rectangles
```

Higher-level systems may bind meaning onto the resulting rectangles.

In the **m0saic** system, rectangles may be associated with:

- Media sources  
- Text primitives  
- Nested compositions  
- Rendering pipelines  

This separation preserves m0 as a portable, implementation-independent layout core.

---

## Reference Implementations

- **`dsl`** – Core parser, validator, and canonical implementation  
- **`dsl-stdlib`** – Standard construction utilities and generators  
- **`dsl-visual-tests`** – Engine-backed visual verification suite  

---

## Relationship to m0saic

m0 is the core layout algebra.

**m0saic** is a system built on top of m0 that provides:

- Visual editing tools  
- Template systems  
- Composition workflows  
- Rendering infrastructure  

m0 may be used independently of m0saic.

---

## Specification Stability

The m0 grammar and semantics follow semantic versioning.

- v1.x is backwards compatible  
- Breaking changes require a major version  
- Conformance defines correctness  

---

## Maintained by

m0 is maintained by **m0saic LLC**.

