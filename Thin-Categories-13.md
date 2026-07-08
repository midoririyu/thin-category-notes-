**[Back to Table of Contents](../README.md)**

# Thin Categories (13)  
Kan Extensions with Thin Categories as Targets

We would like to consider Kan extensions with thin categories as targets, without assuming cocompleteness of the category (i.e., the existence of all (locally small) colimits).

## Definition of Upper Bounds (in General Categories)

We first recall the definition of an upper bound in a general category.

For a subclass $B$ of the objects of a locally small category $\mathcal{C}$, an object $a \in Ob(\mathcal{C})$ is said to satisfy the following two conditions:

1. **Upper bound property**: For every $b \in B$, there exists a morphism $b \to a$.
2. **Least upper bound property**: If there exists an object $a' \in Ob(\mathcal{C})$ such that $b \to a'$ for every $b \in B$, then there exists a morphism $a \to a'$.

When such an $a$ exists, it is called the **supremum** (or **upper bound**) of $B$, and is denoted by $\sup B$ or $\bigvee B$.

When $B$ is empty, condition 1 is vacuously true, and every object is an upper bound of the empty set. Thus, by condition 2, if there exists an object that receives a morphism from every object (i.e., an **initial object** $0$ or $\bot$), then it serves as $\sup B$.

Although the supremum is not necessarily unique as an object, if $a_1$ and $a_2$ are both suprema, then by condition 2 there exist morphisms $a_1 \to a_2$ and $a_2 \to a_1$, so $a_1$ and $a_2$ are isomorphic. It immediately follows that if $\mathcal{C}$ is skeletal, the supremum is unique.

**Proposition**  
Let $F$ be a functor between locally small categories $\mathcal{C}$ and $\mathcal{D}$, and suppose that $\sup B$ and $\sup F(B)$ exist for a subclass $B \subseteq Ob(\mathcal{C})$. Then there exists a morphism $\sup F(B) \to F(\sup B)$.

**Proof**  
By the upper bound property, for every $b \in B$ there is a morphism $b \to \sup B$. By functoriality of $F$, there is a morphism $F(b) \to F(\sup B)$. By the least upper bound property of $\sup F(B)$, there exists a morphism $\sup F(B) \to F(\sup B)$. (Proof complete)

When $\mathcal{C}$ is thin, the existence condition for morphisms automatically strengthens to uniqueness.

## Left Kan Extensions in Thin Categories

**Proposition**  
Let $\mathcal{C}$ be a thin locally small category. For functors $K: \mathcal{A} \to \mathcal{X}$ and $F: \mathcal{A} \to \mathcal{C}$, define the subclass $B_x$ ($x \in \mathcal{X}$) of $Ob(\mathcal{C})$ by
$
B_x = ｛ F(a) \mid a \in \mathcal{A} \text{ and there exists a morphism } K(a) \to x ｝.
$
If $\sup B_x$ exists, choose one such supremum and denote it by $\operatorname{Sup}_K F(x)$.

Then the functor $\operatorname{Sup}_K F : \mathcal{X} \to \mathcal{C}$ defined in this way is a left Kan extension $\operatorname{Lan}_K F$ of $F$ along $K$. Conversely, any left Kan extension $\operatorname{Lan}_K F$ is isomorphic (objectwise) to $\operatorname{Sup}_K F$. If $\sup B_x$ does not exist for some $x \in \mathcal{X}$, then the left Kan extension of $F$ along $K$ does not exist (it fails).

(Proof follows from verifying the universal property of Kan extensions using the simplified definition for thin categories.)

From this proposition, the necessary and sufficient condition for the existence of a left Kan extension with a thin category as target is that $\sup B_x$ exists for every $x \in \mathcal{X}$.

## Relation to the General Case

Let $\mathcal{C}$ be a general locally small category, and suppose a left Kan extension $\operatorname{Lan}_K F : \mathcal{X} \to \mathcal{C}$ of $F$ along $K$ exists. In general categories, $(\operatorname{Lan}_K F)(x)$ is given as the colimit of the diagram consisting of the objects $B_x = ｛ F(a) \mid K(a) \to x \text{ exists} ｝$ and the morphisms induced by the comma category $(K \downarrow x)$.

Even in $\mathcal{C}$, if $\sup B_x$ exists, then there is a morphism $\operatorname{Lan}_K F(x) \to \operatorname{Sup}_K F(x)$.

Furthermore, if a thinning functor $T : \mathcal{C} \to \mathcal{D}$ to a thin category $\mathcal{D}$ is given, the following proposition holds.

**Proposition**  
If the left Kan extension $\operatorname{Lan}_K (T \circ F) : \mathcal{X} \to \mathcal{D}$ of the composite functor $T \circ F$ along $K$ exists, then for every $x \in \mathcal{X}$ there exist morphisms
$
\operatorname{Lan}_K (T \circ F)(x) \to (T \circ \operatorname{Sup}_K F)(x) \to (T \circ \operatorname{Lan}_K F)(x).
$

This proposition shows that, when the order on the thin functor category $[\mathcal{X}, \mathcal{D}]$ is denoted by $\leq$, we have
$
\operatorname{Lan}_K (T \circ F) \leq T \circ \operatorname{Sup}_K F \leq T \circ \operatorname{Lan}_K F.
$

Moreover, if we take the packed arrows functor as the thinning functor $T$, and if $\operatorname{Lan}_K F$ exists, then $\operatorname{Lan}_K (T \circ F) \cong \operatorname{Sup}_K (T \circ F)$ is also defined.

As a contrapositive, if $\operatorname{Lan}_K (T \circ F)$ does not exist, then $\operatorname{Lan}_K F$ does not exist either. This can sometimes serve as a simple criterion for the non-existence of Kan extensions.

It is easier to check the non-existence of a Kan extension in a thin category than in a thick one.

---

## Lower Bounds and Right Kan Extensions

Lower bounds and right Kan extensions can be treated analogously (proofs omitted).

For a subclass $B \subseteq Ob(\mathcal{C})$ of a locally small category $\mathcal{C}$, an object $a \in Ob(\mathcal{C})$ satisfies the following two conditions:

1. **Lower bound property**: For every $b \in B$, there exists a morphism $a \to b$.
2. **Greatest lower bound property**: If there exists an object $a' \in Ob(\mathcal{C})$ such that $a' \to b$ for every $b \in B$, then there exists a morphism $a' \to a$.

Such an $a$ is called the **infimum** (or **lower bound**) of $B$, denoted by $\inf B$ or $\bigwedge B$.

If $\mathcal{C}$ is skeletal, the infimum is unique.

Right Kan extensions can be defined using $\inf B_x$ as $\operatorname{Inf}_K F$, and with a thinning functor $T : \mathcal{C} \to \mathcal{D}$, we obtain the inequality
$
T \circ \operatorname{Ran}_K F \leq T \circ \operatorname{Inf}_K F \leq \operatorname{Ran}_K (T \circ F).
$

If the slogan "every concept in category theory is a Kan extension" is true, then "every concept with a thin category as target is an upper or lower bound."
