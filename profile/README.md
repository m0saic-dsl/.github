# m0 (m0saic DSL)

**m0** is a deterministic, integer-only rectangle layout algebra and canonical string encoding maintained by **m0saic LLC**.

It defines a minimal grammar for transforming a single rectangle into a structured, deterministic set of child rectangles with stable identity and deterministic geometry.

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

The m0 runtime evaluates the string into:

- A deterministic set of rectangles  
- Stable ordering  
- Stable identity keys  
- Exact integer geometry  
- No floating-point layout  
- No runtime-dependent differences  

m0 produces **layout only**.  
It does not assign meaning to rectangles.

m0 intentionally does **not** handle:

- Content measurement  
- Responsive layout rules  
- Styling or rendering  
- Dynamic layout based on runtime content  

It is a layout algebra, not a UI framework.

---

## From Layout Algebra to Renderable Systems

m0 defines geometry.

Higher-level systems may assign semantic meaning to the evaluated rectangles.  
For example, the **m0saic** ecosystem binds:

- Media sources  
- Text primitives  
- Audio  
- Nested compositions  
- Rendering pipelines  

onto the deterministic rectangle output of m0.

This separation allows m0 to function as a portable layout core while enabling richer composition systems to be built on top.

Learn more about the m0saic composition model:  
https://m0saic.io/architecture

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

**m0saic** is the primary composition and rendering ecosystem built on top of m0, including:

- Deterministic visual composition  
- Video and image rendering (FFmpeg backend)  
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
