# Set Theory Notation Cheatsheet

## Sample Data: Pilots and Planes

### Certification Relation $C$ - some call this a factless fact table 😉

| Pilot | Plane |
|-------|-------|
| Celko | Piper Cub |
| Higgins | B-52 Bomber |
| Higgins | F-14 Fighter |
| Higgins | Piper Cub |
| Jones | B-52 Bomber |
| Jones | F-14 Fighter |
| Smith | B-1 Bomber |
| Smith | B-52 Bomber |
| Smith | F-14 Fighter |
| Wilson | B-1 Bomber |
| Wilson | B-52 Bomber |
| Wilson | F-14 Fighter |
| Wilson | F-17 Fighter |

### Derived Sets

$$P = \{\text{Celko}, \text{Higgins}, \text{Jones}, \text{Smith}, \text{Wilson}\}$$

"$P$ is the set of all pilots."

$$D = \{\text{Piper Cub}, \text{B-1 Bomber}, \text{B-52 Bomber}, \text{F-14 Fighter}, \text{F-17 Fighter}\}$$

"$D$ is the set of all planes."

$$C \subseteq P \times D$$

"$C$ is a subset of the Cartesian product of $P$ and $D$."

### Certifications per Pilot

$$C(\text{Celko}) = \{\text{Piper Cub}\}$$

$$C(\text{Higgins}) = \{\text{B-52 Bomber}, \text{F-14 Fighter}, \text{Piper Cub}\}$$

$$C(\text{Jones}) = \{\text{B-52 Bomber}, \text{F-14 Fighter}\}$$

$$C(\text{Smith}) = \{\text{B-1 Bomber}, \text{B-52 Bomber}, \text{F-14 Fighter}\}$$

$$C(\text{Wilson}) = \{\text{B-1 Bomber}, \text{B-52 Bomber}, \text{F-14 Fighter}, \text{F-17 Fighter}\}$$

---

## Basic Set Notation

| Symbol | Notation | Reads As |
|--------|----------|----------|
| $\in$ | $x \in S$ | "$x$ is an element of $S$" |
| $\notin$ | $x \notin S$ | "$x$ is not an element of $S$" |
| $\subseteq$ | $A \subseteq B$ | "$A$ is a subset of $B$" |
| $\subset$ | $A \subset B$ | "$A$ is a proper subset of $B$" |
| $\supseteq$ | $A \supseteq B$ | "$A$ is a superset of $B$" |
| $=$ | $A = B$ | "$A$ equals $B$" |

### Examples

$$\text{Smith} \in P$$

"Smith is an element of $P$."

$$\text{Concorde} \notin D$$

"Concorde is not an element of $D$."

$$\{\text{B-52 Bomber}, \text{F-14 Fighter}\} \subseteq D$$

"The set containing B-52 Bomber and F-14 Fighter is a subset of $D$."

$$C(\text{Jones}) \subset C(\text{Smith})$$

"Jones's certifications are a proper subset of Smith's certifications."

---

## Set Operations

| Symbol | Notation | Reads As |
|--------|----------|----------|
| $\cup$ | $A \cup B$ | "$A$ union $B$" |
| $\cap$ | $A \cap B$ | "$A$ intersection $B$" |
| $\setminus$ | $A \setminus B$ | "$A$ minus $B$" or "$A$ set difference $B$" |
| $\times$ | $A \times B$ | "$A$ cross $B$" or "the Cartesian product of $A$ and $B$" |
| $\emptyset$ | $\emptyset$ | "the empty set" |

### Examples

$$C(\text{Smith}) \cup C(\text{Celko}) = \{\text{B-1 Bomber}, \text{B-52 Bomber}, \text{F-14 Fighter}, \text{Piper Cub}\}$$

"The union of Smith's and Celko's certifications."

$$C(\text{Higgins}) \cap C(\text{Jones}) = \{\text{B-52 Bomber}, \text{F-14 Fighter}\}$$

"The intersection of Higgins's and Jones's certifications."

$$C(\text{Wilson}) \setminus C(\text{Smith}) = \{\text{F-17 Fighter}\}$$

"Wilson's certifications minus Smith's certifications."

$$C(\text{Jones}) \cap \{\text{Piper Cub}\} = \emptyset$$

"The intersection of Jones's certifications and the set containing Piper Cub is the empty set."

---

## Cardinality

| Symbol | Notation | Reads As |
|--------|----------|----------|
| $\|S\|$ | $\|S\|$ | "the cardinality of $S$" |
| $\|A \cap B\|$ | $\|A \cap B\|$ | "the cardinality of $A$ intersection $B$" |
| $\|A\| > k$ | $\|A\| > k$ | "the cardinality of $A$ is greater than $k$" |
| $\|A\| \geq k$ | $\|A\| \geq k$ | "the cardinality of $A$ is at least $k$" |

### Examples

$$|P| = 5$$

"The cardinality of $P$ is 5."

$$|C(\text{Wilson})| = 4$$

"The cardinality of Wilson's certifications is 4."

$$|C(\text{Higgins}) \cap C(\text{Smith})| = 2$$

"The cardinality of the intersection of Higgins's and Smith's certifications is 2."

$$|C(\text{Wilson})| \geq 3$$

"The cardinality of Wilson's certifications is at least 3."

---

## Quantifiers

| Symbol | Notation | Reads As |
|--------|----------|----------|
| $\forall$ | $\forall x \in S$ | "for all $x$ in $S$" |
| $\exists$ | $\exists x \in S$ | "there exists an $x$ in $S$" |
| $\nexists$ | $\nexists x \in S$ | "there does not exist an $x$ in $S$" |
| $\exists!$ | $\exists! x \in S$ | "there exists exactly one $x$ in $S$" |

### Examples

$$\forall d \in C(\text{Jones}): d \in C(\text{Smith})$$

"For all planes $d$ in Jones's certifications, $d$ is in Smith's certifications."

$$\exists p \in P: \text{F-17 Fighter} \in C(p)$$

"There exists a pilot $p$ in $P$ such that F-17 Fighter is in $p$'s certifications."

$$\nexists p \in P: |C(p)| = 5$$

"There does not exist a pilot in $P$ who is certified for 5 planes."

$$\exists! p \in P: \text{F-17 Fighter} \in C(p)$$

"There exists exactly one pilot in $P$ certified for the F-17 Fighter."

---

## Logical Connectives

| Symbol | Notation | Reads As |
|--------|----------|----------|
| $\land$ | $A \land B$ | "$A$ and $B$" |
| $\lor$ | $A \lor B$ | "$A$ or $B$" |
| $\lnot$ | $\lnot A$ | "not $A$" |
| $\rightarrow$ | $A \rightarrow B$ | "$A$ implies $B$" or "if $A$ then $B$" |
| $\leftrightarrow$ | $A \leftrightarrow B$ | "$A$ if and only if $B$" |

### Examples

$$(p \in P) \land (\text{Piper Cub} \in C(p))$$

"$p$ is a pilot and $p$ is certified for the Piper Cub."

$$(\text{B-52 Bomber} \in C(p)) \lor (\text{F-14 Fighter} \in C(p))$$

"$p$ is certified for the B-52 Bomber or the F-14 Fighter (or both)."

$$\lnot(\text{F-17 Fighter} \in C(\text{Jones}))$$

"Jones is not certified for the F-17 Fighter."

$$(|C(p)| \geq 4) \rightarrow (p = \text{Wilson})$$

"If a pilot is certified for at least 4 planes, then that pilot is Wilson."

---

## Set Builder Notation

### General Form

$$\{ x \in S \mid \text{condition}(x) \}$$

"The set of all $x$ in $S$ such that the condition on $x$ holds."

### Examples

$$\{ p \in P \mid |C(p)| \geq 3 \}$$

"The set of all pilots $p$ in $P$ such that the cardinality of $p$'s certifications is at least 3."

**Result:** $\{\text{Higgins}, \text{Smith}, \text{Wilson}\}$

$$\{ p \in P \mid \text{Piper Cub} \in C(p) \}$$

"The set of all pilots $p$ in $P$ such that Piper Cub is in $p$'s certifications."

**Result:** $\{\text{Celko}, \text{Higgins}\}$

---

## Relational Division Patterns

### ALL Pattern (Universal Quantification)

Find pilots certified for ALL planes in a given set $D'$.

Let $D' = \{\text{B-52 Bomber}, \text{F-14 Fighter}\}$

$$\{ p \in P \mid D' \subseteq C(p) \}$$

"The set of all pilots $p$ in $P$ such that $D'$ is a subset of $p$'s certifications."

Equivalent formulation:

$$\{ p \in P \mid \forall d \in D': d \in C(p) \}$$

"The set of all pilots $p$ in $P$ such that for all planes $d$ in $D'$, $d$ is in $p$'s certifications."

**Result:** $\{\text{Higgins}, \text{Jones}, \text{Smith}, \text{Wilson}\}$

---

### ANY Pattern (Existential Quantification)

Find pilots certified for ANY plane in a given set $D'$.

Let $D' = \{\text{Piper Cub}, \text{F-17 Fighter}\}$

$$\{ p \in P \mid C(p) \cap D' \neq \emptyset \}$$

"The set of all pilots $p$ in $P$ such that the intersection of $p$'s certifications and $D'$ is not empty."

Equivalent formulation:

$$\{ p \in P \mid \exists d \in D': d \in C(p) \}$$

"The set of all pilots $p$ in $P$ such that there exists a plane $d$ in $D'$ that is in $p$'s certifications."

**Result:** $\{\text{Celko}, \text{Higgins}, \text{Wilson}\}$

---

### EXACT Pattern

Find pilots certified for EXACTLY the planes in a given set $D'$.

Let $D' = \{\text{B-52 Bomber}, \text{F-14 Fighter}\}$

$$\{ p \in P \mid C(p) = D' \}$$

"The set of all pilots $p$ in $P$ such that $p$'s certifications equals exactly $D'$."

**Result:** $\{\text{Jones}\}$

---

### ATLEAST(k) Pattern

Find pilots certified for at least $k$ planes from a given set $D'$.

Let $D' = \{\text{B-1 Bomber}, \text{B-52 Bomber}, \text{F-14 Fighter}\}$ and $k = 3$

$$\{ p \in P \mid |C(p) \cap D'| \geq k \}$$

"The set of all pilots $p$ in $P$ such that the cardinality of the intersection of $p$'s certifications and $D'$ is at least $k$."

**Result:** $\{\text{Smith}, \text{Wilson}\}$

---

### NONE Pattern

Find pilots certified for NONE of the planes in a given set $D'$.

Let $D' = \{\text{Piper Cub}\}$

$$\{ p \in P \mid C(p) \cap D' = \emptyset \}$$

"The set of all pilots $p$ in $P$ such that the intersection of $p$'s certifications and $D'$ is the empty set."

**Result:** $\{\text{Jones}, \text{Smith}, \text{Wilson}\}$

---

## Quick Reference: Division Patterns

| Pattern | Formula | Reads As |
|---------|---------|----------|
| ALL | $D' \subseteq C(p)$ | "$D'$ is a subset of $p$'s certifications" |
| ANY | $C(p) \cap D' \neq \emptyset$ | "the intersection of $p$'s certifications and $D'$ is not empty" |
| EXACT | $C(p) = D'$ | "$p$'s certifications equals $D'$" |
| ATLEAST($k$) | $\|C(p) \cap D'\| \geq k$ | "the cardinality of the intersection of $p$'s certifications and $D'$ is at least $k$" |
| NONE | $C(p) \cap D' = \emptyset$ | "the intersection of $p$'s certifications and $D'$ is the empty set" |

---

## Projection Notation

| Notation | Reads As |
|----------|----------|
| $\pi_1(C)$ | "the projection of $C$ onto the first component" |
| $\pi_2(C)$ | "the projection of $C$ onto the second component" |

### Examples

$$\pi_1(C) = \{\text{Celko}, \text{Higgins}, \text{Jones}, \text{Smith}, \text{Wilson}\}$$

"The projection of $C$ onto the first component is the set of all pilots appearing in $C$."

$$\pi_2(C) = \{\text{Piper Cub}, \text{B-1 Bomber}, \text{B-52 Bomber}, \text{F-14 Fighter}, \text{F-17 Fighter}\}$$

"The projection of $C$ onto the second component is the set of all planes appearing in $C$."
