# m0 (m0saic DSL)

**m0** is a deterministic, integer-only rectangle layout algebra and canonical string encoding maintained by **m0saic LLC**.

It defines a minimal grammar for transforming a single rectangle into a structured set of child rectangles with stable identity and deterministic geometry.

m0 is designed to be:

- Deterministic
- Human-authorable
- Integer-precise
- O(N) in layout computation
- Portable across runtimes
- Backwards compatible once released

---

## What m0 Does

Given:

- A root rectangle `(width, height)`
- A valid m0 string

The m0 runtime produces:

- A deterministic set of child rectangles
- Stable ordering
- Stable identity keys
- No floating-point geometry
- No runtime-dependent layout differences

m0 intentionally does **not** handle:

- Content measurement
- Responsive layout rules
- Styling or rendering
- Dynamic layout based on runtime content

It is a layout algebra, not a UI framework.

---

## Repositories

- **`dsl`** – Canonical TypeScript reference implementation  
- **`dsl-conformance`** – Specification conformance suite  
- **`dsl-wasm`** – Official WebAssembly runtime  

---

## Conformance

Behavioral correctness is defined by the **m0 Conformance Suite**.

Any implementation that passes the conformance suite may claim compatibility with:

**m0 Specification v1.x**

Conformance verifies:

- Grammar validation
- Canonicalization rules
- Split invariants
- Carry / claim semantics
- Overlay behavior
- Deterministic geometry output
- Error codes

---

## Relationship to m0saic

m0 is the core layout algebra.

**m0saic** is the primary tooling and rendering ecosystem built on top of m0, including:

- Video composition (FFmpeg backend)
- CLI tooling
- Desktop and web applications
- Template libraries

m0 may be used independently of m0saic.

---

## Specification Stability

The m0 grammar and semantics follow semantic versioning.

- m0 v1.x is backwards compatible.
- Changes to grammar or semantics require a major version increment.
- Conformance defines correctness.

---

## Maintained by

m0 is maintained by **m0saic LLC**.

Learn more:  
https://m0saic.io/dsl
