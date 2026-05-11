## Preface

In the spring of 1963 I suggested to Grothendieck the possibility of my running a seminar at Harvard on his theory of duality for coherent sheaves — a theory which had been hinted at in his talk to the Séminaire Bourbaki in 1957 [8], and in his talk to the International Congress of Mathematicians in 1958 [9], but had never been developed systematically. He agreed, saying that he would provide an outline of the material, if I would fill in the details and write up lecture notes of the seminar. During the summer of 1963, he wrote a series of "prénotes" [10] which were to be the basis for the seminar.

I quote from the preface of the prénotes:

"Les présentes notes donnent une esquisse assez détaillée d'une théorie cohomologique de la dualité des Modules cohérents sur les préschémas. Les idées principales de la théorie m'étaient connues dès 1959, mais le manque de fondements adéquats d'Algèbre Homologique m'avait empêché d'aborder une rédaction d'ensemble. Cette lacune de fondements est sur le point d'être comblée par la thèse de VERDIER, ce qui rend en principe possible un exposé satisfaisant. Il est d'ailleurs

apparu depuis qu'il existe des théories cohomologiques de dualité formellement très analogues a celle développée ici dans toutes sortes d'autres contextes: faisceaux cohérents sur les espaces analytiques, faisceaux abéliens sur les espaces topologiques (VERDIER), modules galoisiens (VERDIER, TATE), faisceaux de torsion sur les schémas munis de leur topologie étale, corps de classe en tous genres ... Cela me semble une raison assez sérieuse pour se familiariser avec le yoga général de la dualité dans un cas type, comme la théorie cohomologique des résidus.

La théorie consiste pour l'essentiel dans des questions de variance: construction d'un foncteur f et d'un homomorphisme-trace  $\mathbb{R}f_*f$   $\longrightarrow$  id. La construction donnée ici est compliquée et indirecte et n'est pas valable sous des conditions aussi générales qu'on est en droit de s'y attendre. Il faudra sans doute une idée nouvelle pour apporter des simplifications substantielles."

The seminar took place in the fall and winter of 1963-64, with the assistance of David Mumford, John Tate, Stephen Lichtenbaum, John Fogarty, and others, and gave rise to a

series of six exposés which were circulated to a limited audience under the title "Séminaire Hartshorne". The present notes are a revised, expanded, and completed version of the previous notes.

I would like to take this opportunity to thank all those people who have helped in the course of this work, and in particular A. Grothendieck, who gave continual support and encouragement throughout the whole project.

R.H.

Cambridge, May 1966

## CONTENTS

|             |                                            | page        |
|-------------|--------------------------------------------|-------------|
| Preface     |                                            | III         |
| Content     | s                                          | VI          |
| Introdu     | <del></del>                                | 1           |
| Chapter     | I. The Derived Category                    | <b>1</b> 9  |
| So.         | Introduction                               | <b>1</b> 9  |
| _           | Triangulated categories                    | 20          |
| <b>§</b> 2. | K(A) is triangulated                       | 25          |
| <b>§</b> 3. | Localization of categories                 | 28          |
| 84.         | Qis and the derived category               | <b>3</b> 5  |
|             | Derived functors                           | 49          |
| <b>§</b> 6. | Examples. Ext and R Hom*                   | 62          |
|             | Way-out functors and isomorphisms          | 68          |
| Chapter     | II. Application to Preschemes              | 85          |
|             | Categories of sheaves                      | 85          |
|             | The derived functors of $f_*$ and $\Gamma$ | 87          |
|             | The derived functor of Hom                 | 90          |
| 81<br>€1    | The derived functors of $\otimes$ and f*   | 93          |
|             | Relations among the derived functors       | 100         |
|             | Compatibilities among the relations of §5  | <b>11</b> 5 |
| _           | Injective sheaves on a locally noetherian  |             |
| 57.         | prescheme                                  | 120         |
| Chanter     | III. Duality for Projective Morphisms      | 137         |
| <del></del> |                                            |             |
|             | Differentials                              | 137         |
|             | f# for a smooth morphism f'                | 145         |
|             | Recall of the explicit calculations        | 148         |
|             | The trace map for projective space         | <b>1</b> 54 |
| <b>§</b> 5. | The duality theorem for projective space   | 160         |
| <b>§</b> 6. | Duality for a finite morphism              | 164         |
| §7.         | The fundamental local isomorphism          | <b>1</b> 76 |
| <b>§</b> 8. | f for embeddable morphisms                 | 184         |
| <b>§</b> 9. | The residue symbol                         | <b>1</b> 95 |
| _           | Trace for projective morphisms             | 200         |
| <b>811.</b> | Duality for projective morphisms           | 210         |

|                                                             |                                                                                                                                                           | page                                                               |
|-------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| Chapter                                                     | IV. Local Cohomology                                                                                                                                      | 2 <b>1</b> 5                                                       |
| <b>8</b> 2.                                                 | Local cohomology groups, sheaves, and complexes Depth and the Cousin complex Generalization to complexes                                                  | 2 <b>1</b> 5<br>229<br>240                                         |
| Chapter                                                     | V. Dualizing Complexes and Local Duality                                                                                                                  | 252                                                                |
| <b>8</b> 2.<br><b>8</b> 34.<br><b>8</b> 56.<br><b>8</b> 88. | Example: duality for abelian groups                                                                                                                       | 252<br>254<br>257<br>266<br>272<br>275<br>276<br>286<br>286<br>293 |
|                                                             | Existence of dualizing complexes                                                                                                                          | 299                                                                |
| Chapter                                                     | VI. Residual Complexes                                                                                                                                    | 302                                                                |
| <b>81. 8</b> 2. <b>8</b> 3. <b>8</b> 4.                     | Introduction Residual complexes Functorial properties f for residual complexes Trace for residual complexes Behavior with respect to certain base changes | 302<br>304<br>311<br>318<br>335<br>349                             |
| Chapter                                                     | VII. The Duality Theorem                                                                                                                                  | 357                                                                |
| §1.<br>§2.<br>§3.<br>§4.                                    | Curves over an Artin ring The residue theorem The duality theorem for proper morphisms Smooth morphisms                                                   | 357<br>369<br>374<br>388                                           |
| Index_o                                                     | f Definitions                                                                                                                                             | 394                                                                |
| Index of Notations                                          |                                                                                                                                                           | 396                                                                |
| Bibliography                                                |                                                                                                                                                           | 401                                                                |
| Appendix                                                    | c. Cohomologie à Support Propre, et Construction du                                                                                                       |                                                                    |
| Foncteur f!, par P. Deligne                                 |                                                                                                                                                           | 404                                                                |
| Errata                                                      |                                                                                                                                                           | 422                                                                |

## Introduction

όδὸς ανω κάτω μία καὶ ωντή.

- Heraclitus

The main purpose of these notes is to prove a duality theorem for cohomology of quasi-coherent sheaves, with respect to a proper morphism of locally noetherian preschemes. Various such theorems are already known.

Typical is the duality theorem for a non-singular complete curve X over an algebraically closed field k, which says that

$$h^{O}(D) = h^{1}(K-D) ,$$

where D is a divisor, K is the canonical divisor, and

$$h^{i}(D) = dim_{k} H^{i}(X, L(D))$$

for any i, and any divisor D. (See e.g. [16,Ch. II] for a proof.)

Various attempts were made to generalize this theorem to varieties of higher dimension, and as Zariski points out in his report [20], his generalization of a lemma of Enriques-Severi [19] is equivalent to the statement that

for a normal projective variety X of dimension n over k,

$$h^{O}(D) = h^{n}(K-D)$$

for any divisor D. This is also equivalent to a theorem of Serre [FAC §76 Thm. 4] on the vanishing of the cohomology group  $H^1(X,L(-m))$  for m large and L locally free. Using a related theorem [FAC §75 Thm. 3], Zariski shows how one can deduce on a non-singular projective variety the formula

$$h^{i}(D) = h^{n-i}(K-D)$$

for  $0 \le i \le n$ . In terms of sheaves, this result corresponds to the fact that the k-vector spaces

$$H^{i}(X,F)$$
 and  $H^{n-i}(X,F^{\vee}\otimes\omega)$ 

are dual to each other, where F is a locally free sheaf, F' is the dual sheaf  $\underline{\operatorname{Hom}}(F, \mathcal{O}_X)$ , and  $\omega = \Omega_{X/k}^n$  is the sheaf of n-differentials on X. Serre [15] gives a proof of this same theorem by analytic methods for a compact complex analytic manifold X.

Grothendieck [8] gave some generalizations of these theorems for non-singular projective varieties, and then

in [9] announced the general theorem for schemes proper over a field, with arbitrary singularities, which is the subject of the present lecture notes.

To motivate the statement of our main theorem, let us consider the case of projective space  $X = \mathbb{P}^n_k$  over an algebraically closed field k. Then there is a canonical isomorphism

$$(1) Hn(x, \omega) \cong k$$

where  $w = \Omega_{X/k}^n$  is the sheaf of n-differentials. Combining this with the Yoneda pairing

(2) 
$$H^{i}(X,F) \times Ext_{X}^{n-i}(F,\omega) \longrightarrow H^{n}(X,\omega)$$

we obtain a pairing

(3) 
$$H^{i}(X,F) \times Ext_{X}^{n-i}(F,\omega) \longrightarrow k$$

which one shows easily to be a perfect pairing [SGA 62, exposé 12]. This generalizes the statements above, because for a locally free sheaf F,

$$\operatorname{Ext}^{\mathbf{n-i}}(\mathbf{F},\omega) = \operatorname{Ext}^{\mathbf{n-i}}(\mathcal{O}_{\mathbf{X}}',\mathbf{F}'\otimes\omega) = \operatorname{H}^{\mathbf{n-i}}(\mathbf{X},\mathbf{F}'\otimes\omega) .$$

Another way of looking at our duality pairing is as an isomorphism

(4) 
$$\operatorname{Ext}_{X}^{n-i}(F,\omega) \longrightarrow \operatorname{Hom}_{k}(H^{i}(X,F), k).$$

Since everything is linear over k, we may introduce a k-vector space G, and have an isomorphism

(5) 
$$\operatorname{Ext}_{X}^{n-i}(F, G\otimes_{k}\omega) \longrightarrow \operatorname{Hom}_{k}(H^{i}(X,F), G).$$

Before proceeding further, we must introduce the derived category. It will be discussed in detail in Chapter I, but for the moment it will be sufficient to know the following: For each abelian category A, there is a category D(A), called the derived category of A, whose objects are complexes of objects of A. If  $F: A \longrightarrow B$  is an additive functor from one abelian category to another, then under reasonable conditions there is a right derived functor  $P(A) \longrightarrow D(B)$  with the property that for any  $X \in Ob(A)$ , if X denotes also the complex which is X in degree zero, and zero elsewhere, then  $H^1(P(X)) = P^1(X)$ , where  $P(A) \longrightarrow P(B)$  is the ordinary it right derived functor of F. Finally, if  $P(A) \longrightarrow P(B)$  and  $P(B) \longrightarrow P(B)$  are two functors

then  $R(G \cdot F) = RG \cdot RF$ . This replaces the old-fashioned spectral sequence of a composite functor.

Now we can jazz up our duality for projective space as follows. We replace k by a prescheme Y, so that  $X = \mathbf{F}_Y^n$ . We consider the derived categories D(X) and D(Y) of the categories of  $\mathcal{O}_X$ -modules and  $\mathcal{O}_Y$ -modules, respectively. Then cohomology  $H^1$  becomes  $\mathbb{F}_X^n$ , the derived functor of the direct image functor  $f_*$ , where  $f: X \longrightarrow Y$  is the projection. Ext becomes the derived functor  $f_*$  Hom of Hom. We define  $f^{\bullet}(G) = f^*(G) \otimes_{\mathfrak{W}}$ , for  $G \in D(Y)$ , and we replace F by a complex of sheaves  $F \in D(X)$ . Then the isomorphism (1) gives us an isomorphism

(6) 
$$Rf_*f'G \xrightarrow{\sim} G$$

which we call the <u>trace map</u>. The Yoneda pairing reappears as a natural map

(7) 
$$\underline{R} \operatorname{Hom}_{X}(F, f \cdot G) \longrightarrow \underline{R} \operatorname{Hom}_{Y}(\underline{R}f_{*}F, \underline{R}f_{*}f \cdot G)$$
,

which, composed with the trace map (6) gives us the <u>duality</u> morphism

(8) 
$$\underline{\underline{R}} \operatorname{Hom}_{X}(F, f'G) \longrightarrow \underline{\underline{R}} \operatorname{Hom}_{Y}(\underline{\underline{R}}f_{*}F, G)$$

which generalizes (5). This is easily proved to be an isomorphism ([III 5.1] below) under suitable hypotheses on Y,F,G. In fact, the proof is nothing but "general nonsense" once one has the isomorphism (4).

Having examined the case of projective space, we can state the following ideal theorem, which is the primum mobile of these notes, although it may never appear explicitly in this form.

Ideal Theorem. (a) For every morphism  $f: X \longrightarrow Y$  of finite type of preschemes, there is a functor

$$f': D(Y) \longrightarrow D(X)$$

such that

- 1) if  $g: Y \longrightarrow Z$  is a second morphism of finite type, then  $(gf)^! = f^!g^!$ 
  - 2) if f is a smooth morphism, then

$$f^{!}(G) = f^{*}(G) \otimes \omega ,$$

where  $\omega = \Omega_{X/Y}^{n}$  is the sheaf of highest order differentials

3) if f is a finite morphism, then

$$f'(G) = \underline{\text{Hom}}_{\mathcal{O}_{\mathbf{Y}}}(f_*\mathcal{O}_{\mathbf{X}},G)^{\sim}$$
.

(b) For every proper morphism  $f: X \longrightarrow Y$  of preschemes, there is a trace morphism

$$\operatorname{Tr}_{\mathbf{f}} : \operatorname{Rf}_{*} \mathbf{f}^{!} \longrightarrow \operatorname{id}$$

of functors from D(Y) to D(Y) such that

- 1) if g: Y  $\longrightarrow$  Z is a second proper morphism, then  $Tr_{\tt qf} = Tr_{\tt qf} Tr_{\tt f} \; .$
- 2) if  $X = \mathbb{P}_Y^n$ , then  $\operatorname{Tr}_f$  is the map deduced from the canonical isomorphism  $\operatorname{R}^n f_*(w) \cong \mathcal{O}_Y$
- 3) if f is a finite morphism, then  $\mathrm{Tr}_{\mathbf{f}}$  is obtained from the natural map "evaluation at one"

$$\underline{\underline{\text{Hom}}}_{\mathcal{O}_{\mathbf{Y}}}(f_{*}\mathcal{O}_{X},G) \longrightarrow G .$$

c) If  $f: X \longrightarrow Y$  is a proper morphism, then the duality morphism

$$\Theta_{f}: \underline{R} \operatorname{Hom}_{X}(F, f'G) \longrightarrow \underline{R} \operatorname{Hom}_{Y}(\underline{R}f_{*}F, G)$$

obtained by composing the natural map (7) above with  $\operatorname{Tr}_{\mathbf{f}}$ , is an isomorphism for  $F \in D(X)$  and  $G \in D(Y)$ .

It should be noted that we have deliberately left certain technical details out of the above statement, for ease of reading. Thus it seems reasonable to make these statements only for complexes of quasi-coherent sheaves, or rather for complexes of arbitrary sheaves, whose cohomology sheaves are quasi-coherent. (We denote this category by  $D_{qq}(Y)$  or  $D_{qq}(X)$ .) In fact, we give an example in the case of a finite morphism to show that the duality theorem (c) fails if G is not quasi-coherent (see example following [III 6.7]). Secondly one must expect certain boundedness conditions on the complexes involved, namely F should be bounded above (we write  $F \in D^{-}_{CC}(X)$ ) and G should be bounded below  $(G \in D_{ac}^+(Y))$  for the duality theorem. Finally, questions of variance will be very important in the proof, and so the equals signs in al and bl must be taken with a grain of salt. We must preserve very carefully the distinction between "equals" and "is canonically isomorphic to". Hence we will have more precise statements below.

As to proving the ideal theorem, we succeed only partially. Certainly the conditions under which we can prove it will suffice for most applications, but it is unsatisfying

to have restrictive hypotheses which are apparently not essential to the truth of the theorem. I mention four sets of hypotheses under which the theorem can be proved.

- (i) For the category of noetherian preschemes of finite Krull dimension, and morphisms  $f\colon X\longrightarrow Y$  which can be factored through a suitable projective space  $\mathbb{P}^N_Y$ , we have al-3 for  $\mathbb{D}^+_{qc}(Y)$  [III 8.7], bl-3 for  $\mathbb{D}^+_{qc}(Y)$  [III 10.5], and c for  $F\in \mathbb{D}^-_{qc}(X)$  and  $G\in \mathbb{D}^+_{qc}(Y)$  [III 11.1].
- (ii) For the category of noetherian preschemes which admit dualizing complexes (see [V \$10]; this implies in particular that the preschemes have finite Krull dimension) and morphisms whose fibres are of bounded dimension, we have al-3 and bl-3 for  $D_C^+(Y)$ , and c for  $F \in D_{QC}^-(X)$ ,  $G \in D_C^+(Y)$  [VII 3.4]. Here the subscript "c" denotes complexes with coherent cohomology sheaves.
- (iii) For the category of noetherian preschemes of finite Krull dimension and smooth morphisms, we have al-3 for  $D_{qc}^+(Y)$ , bl-3 for  $G \in D_{qc}^b(Y)$ , and C for  $F \in D_{qc}^-(X)$  and  $G \in D_{qc}^b(Y)$  [VII 4.3]. Here the exponent "b" denotes complexes which are bounded in both directions, i.e., finite.

(iv) Recently P. Deligne has shown (unpublished) that for the category of noetherian preschemes, one can construct  $f^{!}$  and  $Tr_{f}$  satisfying al,bl, and c, working with  $F \in D(Qco(X))$  and  $G \in D^{+}(Qco(Y))$ , the derived categories of the categories of quasi-coherent sheaves on X and Y, respectively.

The principal difficulty has been the lack of a suitable construction of the functor f. Our procedure is to define it locally, and then glue. For a finite or a smooth morphism, we have it given to us, by a2 and a3 [III §2,86]. Thus by composition we can obtain it for any morphism which can be factored into a finite morphism followed by a smooth morphism [III §8]. However, the derived category is not a local object, so we cannot glue these local determinations of f. to obtain a global one. We resort to a clumsy, round-about procedure of defining f. for a special class of complexes, called residual complexes [VI §3], and then pulling ourselves up by our bootstraps to get it for arbitrary complexes [VII §3]. But our result has the unpleasant hypotheses of (ii) above.

Deligne's construction of f is entirely different, and proceeds essentially by representing the functor (for  $F \in D(X)$ )

$$F \longmapsto R \operatorname{Hom}_{V} (Rf_{*}F,G).$$

This approach has the advantage of giving the duality theorem immediately. He also has a method for calculating f'G locally on X. However, it is not immediately clear from his construction that the properties a2,3 and b2,3 hold. In fact, their proof will probably require some knowledge of the duality theorem as we have proved it here. At least one can hope that some combination of the two approaches will provide substantial simplifications of the theory at a later date.

A second difficulty, which lurks on the fringes of these notes, is that the derived category seems to be a little too big when it comes to unbounded complexes. For example, one can have two unequal morphisms  $f,g: X \longrightarrow Y$  in  $D^+(A)$  (where A is an abelian category) such that their restrictions to each truncation of the complex X to a bounded complex, are equal. This gives rise to some trouble with unbounded complexes (see the problem after [II 5.7], the boundedness hypotheses in [IV 3.1] and [VII 4.3a], and the remark following [VI 1.1c]). Perhaps one will have to replace  $D^+$  by the categories ind  $D^b$  and pro  $D^b$ , which however may not be triangulated categories!

Thirdly, some discussion of our noetherian hypotheses is in order. In the present state of the theory, the noetherian hypotheses are well entrenched. We have used them in [II §7] for the structure of the injective objects in the category of sheaves on a locally noetherian prescheme, and its consequence that  $D^{+}(Qco(X)) \longrightarrow D^{+}_{GC}(X)$  is an equivalence of categories. We have used them in the construction of the trace map for projective space [III \$4], in the construction of f' for a finite morphism [III §6], in the whole theory of dualizing complexes [V 82], in the definition of residual complexes [VI \$1], and so forth. Our finite Krull dimension hypotheses are often needed only to make possible the definition of  $Rf_*$  for unbounded complexes — a problem which will disappear when the second difficulty above is solved, and the relation between D(Qco(X)) and  $D_{CC}(X)$  is better understood. It is certainly clear that our methods of proof rely heavily on noetherian hypotheses. I expect, however, that once a suitable statement is obtained, e.g., in case (iii) above, one could expect to prove the theorem without noetherian hypotheses, by reducing to the noetherian case. More satisfactory, of course, would be a

eliminated from the proofs as well as from the statements.

When that is achieved, it will be reasonable to state the duality theorem for a proper morphism of ringed topos, whose fibres are noetherian schemes... At the present, however, this must remain a dream of things to come.

Now we will give the reader a brief description of the organization of these notes.

Chapter I gives the language of derived categories, which is used continually in the sequel. Sections 1-5, containing the definition of derived categories and derived functors, are essential, while sections 6 and 7 are refinements which are needed in proofs later on. This chapter is a self-contained treatment of the subject, and makes no reference to algebraic geometry, so can be used independently as an introduction to the notion of derived category. Sections 1-6 (except for the notion of localizing subcategory and the corresponding categories  $K_{A^{\perp}}(A)$ ,  $D_{A^{\perp}}(A)$ , etc.) are taken almost without change from notes of Verdier, and should appear in his thesis [18].

Chapter II is a fairly systematic treatment of the applications of the language of derived categories to the category of sheaves on a prescheme. We consider the functors  $\Gamma$ ,  $f_*$ ,  $\operatorname{Hom}$ ,  $\operatorname{Hom}$ ,  $\otimes$ ,  $f^*$ , their derived functors, and relations between these derived functors, such as associativity formulae. There is really no new mathematics involved here, since it is merely a translation into a new language of known results. However, some care is taken to see what hypotheses are needed. Only section 7 is notable new material. Here we give the structure of injective  $\mathcal{O}_X$ -modules on a locally noetherian prescheme X, showing that they are all direct sums of certain indecomposable injectives J(x,x'), for pairs of points x specializing to x' of X. This extends results of Matlis [13] and Gabriel [5] for the case of quasi-coherent sheaves.

Chapter III contains everything we can say about duality for projective morphisms, and if the reader cares only for them, he may stop at the end of this chapter. However, it should be noted that the following chapters, besides giving us the tools for the proof of the general duality theorem in Chapter VII, also give much new insight into the nature of duality for a projective morphism.

There are so many situations in which we have a functor  $f^{!}$  like the one mentioned in the ideal theorem above, that we use different notations for them. Thus we have  $f^{\#}$  for a smooth morphism in section 2,  $f^{\dag}$  for a finite morphism in section 6, and  $f^{!}$  for an embeddable morphism in section 8. Later we will also have  $f^{Y}$ ,  $f^{Z}$  [VI §2] and  $f^{A}$ [VI §3] for residual complexes.

In sections 3, 4, and 5 we recall the explicit calculations of cohomology for projective space, and give the old duality for projective space in the new language of derived categories.

Sections 6 and 7 give the corresponding formalism for finite morphisms, and its relation to the case of smooth morphisms, so that in sections 8, 10, and 11 we can prove the ideal duality theorem for projective morphisms. Section 9 gives the formalism of a residue symbol which generalizes the classical residue of a differential on a curve. Even over the complex numbers, this important concept of residue for varieties of dimension greater than one was not known before.

In Chapter IV we study "local cohomology", or cohomology with restricted supports, of abelian sheaves on a locally noetherian topological space, generalizing results of [LC §§1,3]. In particular, we discuss various cohomological

properties which a sheaf or complex of sheaves may have with respect to certain families of supports. This gives rise to the notions of depth, Cousin complex, Cohen-Macaulay complex, and Gorenstein complex. The results of this chapter are independent of all other chapters of these notes, and so may be of use elsewhere, although their only application for the moment is to the theory of duality on preschemes.

Chapter V discusses dualizing complexes (read section 0 to find out what one is) and gives a duality theorem for modules over a local ring, generalizing results of [LC §§2,4,6]. In particular, the dualizing functor  $D = \frac{R}{R} \frac{Hom}{(\cdot,R^{\cdot})}$  treated here will be useful for our bootstrap operation (construction of  $f^{\cdot}$ ) later, because it interchanges  $\otimes$  and Hom,  $f^{\cdot}$  and  $Lf_{*}$ , and commutes with  $Rf_{*}$  (duality theorem!).

In Chapter VI we prepare for the final duality theorem by giving the construction of f and Tr for residual complexes. This is accomplished by a delicate glueing procedure which is the most difficult part of the theory, so we have given it in some detail. Perhaps some day this type of construction will be done more elegantly using the language of fibred categories and results of Giraud's thesis [6].

Chapter VII contains two main results. The first is the residue theorem, which generalizes the classical theorem that the sum of the residues of a differential on a curve is zero, and which is proved by reduction to that case. The second is the proof of the duality theorem for a proper morphism, which, now that all the functorial machinery has been set up, is little more than putting together the pieces of a jigsaw puzzle.

It remains to give the reader some perspective by listing some topics which have a logical place in these notes, but which are not here.

1. The cohomology class associated to a cycle. Let X be proper and smooth of dimension n over a field k. In [8, §4] it is shown how to associate to each non-singular subvariety Y of codimension p of X, a cohomology class

$$P_X(Y) \in H^p(X, \Omega_{X/k}^p)$$
.

Now this can be done for an arbitrary subvariety of X, using the remarks in [9]. One defines  $w_{Y} = H^{-n+p}(g^{!}k)$ , where  $g: Y \longrightarrow k$  is the projection. Then there is a canonical element

$$\eta \in \operatorname{Ext}_{\mathcal{O}_{\mathbf{Y}}'}^{-n+p}(\omega_{\mathbf{Y}}, g^{!}k)$$
.

One defines a natural map

$$\Omega_{\mathbf{Y}/\mathbf{k}}^{\mathbf{n-p}} \longrightarrow \omega_{\mathbf{Y}}$$
 ,

which, together with  $\eta$  and the construction of [8, 84], gives the cohomology class  $P_X(Y)$ . One proves the fundamental theorem that formation of the cohomology class associated to a cycle takes an intersection of cycles into the cup-product of their cohomology classes.

- 2. The theory of Poincaré duality and the Gysin homomorphism can be developed as in [8, \$7].
- 3. A Lefschetz-Verdier fixed point formula for coherent sheaves on a scheme proper over a field, to generalize [21, Thm. 2]. In particular, the determination of the local contribution at a non-simple fixed point presents an interesting topic for future investigation.
- 4. The still lacking theory of duality for complexes with differential operators as boundary operator, its ties with ordinary singular <a href="https://doi.org/10.1001/journal.com/">homology</a> theory and with vector bundles with integrable connections, as suggested in [22].

A remark on references: Theorem 5.1 of Chapter III is referred to as "Theorem 5.1" in Chapter III, and as [III 5.1] elsewhere. References to the bibliography at the end are given by square brackets with an arabic numeral or some capital letters e.g., [14,(31.1)] or [EGA III 2.1.12].