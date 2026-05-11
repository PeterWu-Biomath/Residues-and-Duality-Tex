#### CHAPTER V. DUALIZING COMPLEXES AND LOCAL DUALITY

### \$0. Introduction.

In this chapter we discuss dualizing complexes on a locally noetherian prescheme X. A dualizing complex is a complex  $R^* \in D^+(X)$  such that the functor

$$\underline{D}\colon M^{\bullet} \longrightarrow \underline{R} \operatorname{Hom}^{\bullet}(M^{\bullet}, R^{\bullet})$$

induces an auto-duality of the category  $D_{\mathbf{C}}^{\mathbf{b}}(\mathbf{X})$  consisting of those bounded complexes in  $D^+(\mathbf{X})$  which have coherent cohomology. We will show that a large class of preschemes admits dualizing complexes, and that they are almost uniquely determined.

The notion of dualizing complex will allow us to write the duality theorem in a new way. For example, let X be projective n-space over a field k. Then  $R^* = \omega[n]$  (where  $\omega = \omega_{X/k}$  is the sheaf of relative n-differentials [III §1]) is a dualizing complex for X, and k is a dualizing complex for k. We have a canonical isomorphism  $\Pr_{C}(\omega[n]) \cong k$  [III 3.4], and hence, for any complex  $F^* \in D^b_C(X)$ , a homomorphism

$$\Theta\colon \ \ \underline{\mathbf{R}}\mathbf{f}_{*} \ \underline{\mathbf{D}}_{X}(\mathbf{F}^{*}) \longrightarrow \underline{\mathbf{D}}_{k}(\underline{\mathbf{R}}\mathbf{f}_{*}(\mathbf{F}^{*})) \ ,$$

where  $\underline{D}_X$  and  $\underline{D}_k$  are the dualizing functors on X and on k, respectively. The duality theorem [III 5.1] says that  $\Theta$  is an isomorphism, i.e., that the dualizing functors on X and on k commute with  $\underline{R}f_*$ .

In the latter part of the chapter we discuss the local duality theorem, as in [LC §2,4,6] or [SGA 62, exposé 2,4]. The proof of the duality theorem given here is different, however.

The reader will see that the existence of a dualizing complex on a locally noetherian prescheme X implies that X has finite Krull dimension. Hence we will give a more general notion, that of a pointwise dualizing complex, to cover the case of infinite Krull dimension.

For convenience we defer the question of existence of dualizing complexes until the end of the chapter (section 10).

#### \$1. Example: Duality for abelian groups.

Let  $X = \operatorname{Spec} \mathbb{Z}$ . Then the category of quasi-coherent sheaves on X is isomorphic to the category (Ab) of abelian groups. We know that  $\mathbb{Q}/\mathbb{Z}$  gives a good duality for finite abelian groups, i.e., that the functor  $\operatorname{Hom}(\cdot, \mathbb{Q}/\mathbb{Z})$  is an exact contravariant functor, which, when applied twice to a finite abelian group, gives that group back again. Similarly, the group  $\mathbb{Q}$  gives a good notion of duality for finitely generated free abelian groups. Combining the two, we consider the complex

$$q \longrightarrow q/z$$

and work in the derived category  $D_{\mathbf{c}}^{\mathbf{b}}(A\mathbf{b})$ , consisting of those bounded complex in  $D^{+}(A\mathbf{b})$  which have finitely generated cohomology. (c is for "coherent", which means "finitely generated" in our case.) Since the complex above is an injective resolution of  $\mathbf{Z}$ , hence isomorphic to  $\mathbf{Z}$  in the derived category, we arrive at the following proposition.

Proposition 1.1. The functor

D: 
$$M^{\bullet} \longrightarrow \mathbb{R} \text{ Hom}^{\bullet}(M^{\bullet},\mathbb{Z})$$

is a contravariant  $\partial$ -functor from  $D_{\mathbf{C}}^{\mathbf{b}}(\mathbf{Ab})$  into itself, and there is a natural functorial isomorphism

$$\eta: \operatorname{id}_{\operatorname{D}_{\mathbf{C}}^{\mathbf{b}}(\operatorname{Ab})} \xrightarrow{\sim} \operatorname{DD}.$$

<u>Proof.</u> Since the cohomology of  $D(M^{\circ})$  is  $\operatorname{Ext}^{1}(M^{\circ}, \mathbb{Z})$ , if  $M^{\circ} \in D^{b}_{C}(Ab)$ , then so is  $D(M^{\circ})$ . The natural functorial homomorphism  $\eta$  is defined in Lemma 1.2 below. To show that it is an isomorphism, by taking a free resolution of  $M^{\circ}$  and applying the lemma on way-out functors [I.7.1], we reduce to the case  $M^{\circ} = \mathbb{Z}^{r}$  for some r. Since the functors in question are additive, one reduces to the case  $M^{\circ} = \mathbb{Z}$ , and to complete the proof, one need only observe that  $\operatorname{Ext}^{1}(\mathbb{Z},\mathbb{Z}) = \mathbb{Z}$  if i = 0, and 0 otherwise.

Lemma 1.2. Let X be a prescheme, let  $R' \in D^+(X)$  and let  $F' \in D(X)$ . Then there is a natural functorial homomorphism

$$\eta: F' \longrightarrow \underline{R} \xrightarrow{\text{Hom}^*} (\underline{R} \xrightarrow{\text{Hom}^*} (F',R'), R')$$
.

<u>Proof.</u> Replacing R° by an injective resolution, we can erase the <u>R</u>. As usual, we need only define  $\mathcal{T}$  on <u>objects</u> of D(X), i.e., complexes. Given an index p, and a section  $s \in F^p(U)$ 

over an open set U in X, we must define, for each q, a homomorphism of sheaves

$$\underline{\text{Hom}}^{q}(F^{\bullet},R^{\bullet})_{U} \longrightarrow R_{U}^{p+q}$$
,

where the subscript U denotes restriction of sheaves to U. Given a homomorphism  $f \in \underline{\operatorname{Hom}}^q(F^{\:\raisebox{3.5pt}{\text{\circle*{1.5}}}},R^{\:\raisebox{3.5pt}{\text{\circle*{1.5}}}})_U(V)$  defined on an open set  $V \subseteq U$ , we send it to the section  $f(s_V) \in \mathbb{R}^{p+q}(V)$ , where  $s_V$  is the section s, restricted to V. One checks that this indeed does define a morphism of complexes, and that it is functorial in  $F^{\:\raisebox{3.5pt}{\text{\circle*{1.5}}}}$ .

# §2. Dualizing Complexes.

Throughout this section, X will denote a locally noetherian prescheme. We will consider complexes  $R^* \in D^+(X)$  which have coherent cohomology and finite injective dimension, i.e.,  $R^* \in D_{\mathbf{C}}^+(X)_{\mathbf{fid}}$  (see [I.7.6] and [II.7.20]). Note that if X is quasi-compact, then the condition of finite injective dimension on a complex  $R^* \in D_{\mathbf{C}}^+(X)$  can be checked locally (eg., by [II 7.20(<u>iii)</u>]). Note also that such a complex  $R^*$  is quasi-isomorphic to a bounded complex of quasi-coherent injective sheaves on X [II 7.20(i)qc], and hence (using [II 3.3]) the functor

$$\underline{D}\colon F^{\bullet} \longrightarrow \underline{R} \operatorname{\underline{Hom}}^{\bullet}(F^{\bullet}, R^{\bullet})$$

sends  $D_{c}^{b}(X)$  into itself, and interchanges  $D_{c}^{+}(X)$  and  $D_{c}^{-}(X)$ .

Definition. Let  $R^* \in D^+(X)$ . We say that a complex  $F^* \in D(X)$  is reflexive (with respect to  $R^*$ ) if the natural map

$$\eta: F^{\bullet} \longrightarrow \underline{R} \xrightarrow{\text{Hom}^{\bullet}} (\underline{R} \xrightarrow{\text{Hom}^{\bullet}} (F^{\bullet}, R^{\bullet}), R^{\bullet})$$

of Lemma 1.2 is an isomorphism.

<u>Proposition 2.1.</u> Let  $R^* \in D^+_{\mathbf{C}}(X)_{\text{fid}}$ . Then the following conditions are equivalent:

- (i) Every  $F^* \in D_C(X)$  is reflexive (with respect to  $R^*$ ).
- (ii) Every  $F^* \in D_C^b(X)$  is reflexive.
- (iii) Every coherent sheaf on X is reflexive.
- (iv) The structure sheaf  $\theta_{\chi}$  is reflexive.

<u>Proof.</u> Clearly (i)  $\Longrightarrow$  (ii)  $\Longrightarrow$  (iv). To prove (iv)  $\Longrightarrow$  (i) we note that the question is local on X. Hence we may assume that X is affine. Then every coherent sheaf on X is the quotient of a free sheaf  $\mathcal{O}_X^r$ ; the functors in question are additive, so the result follows from the Lemma on Way-Out Functors [I.7.1 (ii) and (iv)], taking into account [II 7.20(<u>ii</u>)] which implies that  $R \to \infty$  is way-out in both directions.

Definition. Let X be a locally noetherian prescheme. A complex  $R^* \in D^+_c(X)_{\mbox{fid}}$  satisfying the equivalent conditions of the proposition is called a dualizing complex for X.

Definition. The Krull dimension of a locally noetherian prescheme X is the largest n (or  $+\infty$ ) for which there is a chain  $Z_0 < Z_1 < \cdots < Z_n$  of closed irreducible subsets  $Z_i$  of X. It is also the sup of the dimensions of the local rings of X.

Example 2.2. Let X be a regular prescheme of finite Krull dimension. (A regular prescheme is a prescheme X such that all the local rings  $\mathcal{O}_{X,X}$  of points of X are regular local rings.) Then the structure sheaf  $\mathcal{O}_{X}$  is a dualizing complex for X.

Indeed, condition (iv) of the proposition is trivial, because  $\underline{\operatorname{Ext}}^{\mathbf{i}}(\mathscr{O}_{X},\mathscr{O}_{X})=\mathscr{O}_{X}'$  for  $\mathbf{i}=0$ , and 0 otherwise. Clearly  $\mathscr{O}_{X}'\in \operatorname{D}_{\mathbf{c}}^{+}(X)$ . To show that  $\mathscr{O}_{X}'$  has finite injective dimension, we use condition  $(\underline{iii})_{\mathbf{c}}'$  of [I.7.20]. Let  $\mathbf{n}_{\mathbf{o}}'$  be the Krull dimension of X. Then for every coherent sheaf F on X,  $\underline{\operatorname{Ext}}^{\mathbf{i}}(F,\mathscr{O}_{X}')=0$  for  $\mathbf{i}>\mathbf{n}_{\mathbf{o}}'$ , because  $\underline{\operatorname{Ext}}^{\mathbf{i}}'$  commutes with taking stalks, and the local rings  $\mathscr{O}_{X}'$  all have cohomological dimension  $\leq \mathbf{n}_{\mathbf{o}}'$ , since they are regular local rings [14 (28.2)].

Corollary 2.3. Let  $R^* \in D_{\mathbf{C}}^+(X)_{\mathrm{fid}}$ . Then  $R^*$  is dualizing if and only if for every  $x \in X$ ,  $R_{\mathbf{X}}^*$  is dualizing on the local scheme Spec  $\mathcal{O}_{\mathbf{X}}^*$ . Furthermore, it is sufficient to take the closed points  $\mathbf{x} \in X$ .

Proof. For  $x \in X$ , we see that the stalk  $R_x^*$  has finite injective dimension in  $D_c^+(\operatorname{Spec} \ \mathcal{O}_X)$  by using [II 7.20 (i) $_{\operatorname{qc}}$ ] and [II.7.17 (iii)]. Thus the result follows from condition (iv) of the Proposition.

Proposition 2.4. Let  $f: X \longrightarrow Y$  be a finite morphism of locally noetherian preschemes, and let  $R^*$  be a dualizing complex on Y. Then  $f^{\dagger}R^*$  is a dualizing complex on X (cf. [III §6]).

<u>Proof.</u> We may assume that R is a bounded complex of quasi-coherent injective sheaves on Y. Then

$$f^{\flat}(R^{\bullet}) = \underline{\text{Hom}}_{Y}(f_{*}\mathscr{O}_{X},R^{\bullet})^{\sim}$$
,

which is a bounded complex of quasi-coherent injectives on X. Hence  $f^{\flat}(R^{\bullet}) \in D^{b}_{\mathbf{C}}(X)_{\mathrm{fid}}$ . To see that  $f^{\flat}(R^{\bullet})$  is dualizing, we apply condition (iv) of the previous proposition, and consider the map

$$\eta\colon \mathscr{O}_{X} \longrightarrow_{\underline{R}} \underline{\operatorname{Hom}}_{X}^{\bullet}(\underline{R} \underline{\operatorname{Hom}}_{X}^{\bullet}(\mathscr{O}_{X}, f^{\flat}(R^{\bullet})), f^{\flat}(R^{\bullet})).$$

Applying  $\mathbb{R}f_*$  to this map, and using duality for a finite morphism [III 6.7] twice, we see that  $\mathbb{R}f_*(\eta)$  is an isomorphism. But we are dealing with quasi-coherent sheaves, and  $f_*$  is faithful, so  $\eta$  is an isomorphism.

Remarks. 1. We will see later that if f is a smooth morphism, then f\* of a dualizing complex is dualizing (Theorem 8.3 below).

2. This result, joined with the example above, shows that any closed subscheme of a regular prescheme of finite Krull dimension admits a dualizing complex.

<u>Proposition 2.5.</u> A complex  $R^* \in D_{\mathbf{C}}^+(X)_{\text{fid}}$  is dualizing if and only if for every closed point  $\mathbf{x} \in X$ , the sheaf  $\mathbf{k}(\mathbf{x})$ , consisting of the residue field  $\mathbf{k}(\mathbf{x})$  at the point  $\mathbf{x}$  and zero elsewhere, is reflexive.

Proof. 1) Using Corollary 2.3, we reduce to the case where X is the spectrum of a local noetherian ring A, with residue field k. The assumption is then that k is reflexive, and we wish to show for every A-module of finite type M (in particular, for M = A), that M is reflexive on X.

2) Using induction on the length, we show first that every A-module M of finite length is reflexive. Indeed, for length M = 1, we have assumed it. For length M > 1, one can write a short exact sequence

$$0 \longrightarrow M' \longrightarrow M \longrightarrow M'' \longrightarrow 0$$

where M' and M" have length < length M. Then by the induction hypothesis M' and M" are reflexive, and by long exact sequences

(DD is a d-functor!) and the five-lemma, M is reflexive.

7) Now we show that any module of finite type M is reflexive, using induction on the dimension of M. If dim M = O, then M has finite length, and M is reflexive by 2) above. Let M be a module of finite type. Let M' be the submodule of elements with support M, where M is the maximal ideal of A. Then M' has finite length, so it is sufficient to consider M/M'. In other words, we have reduced to the case M \(\frac{1}{2}\) Ass M.

Let t \(\epsilon\) be an element which is not a zero-divisor in M, so that we have an exact sequence

$$0 \longrightarrow M \xrightarrow{t} M \longrightarrow M/tM \longrightarrow 0$$
.

Now dim M/tM < dim M, so by the induction hypothesis M/tM is reflexive. Therefore, for each  $i \neq 0$ , we have an exact sequence

$$H^{i}(DD(M)) \xrightarrow{t} H^{i}(DD(M)) \longrightarrow 0.$$

Now these  $H^{i}$  are A-modules of finite type, and  $t \in M$ , so by Nakayama's lemma,  $H^{i}(DD(M)) = 0$  for  $i \neq 0$ .

Consider the commutative diagram

$$\begin{array}{cccccccccccccccccccccccccccccccccccc$$

with exact rows. A diagram chase shows that

$$H^{O}(DD(M)) = \alpha(M) + tH^{O}(DD(M))$$
,

so by Nakayama's Lemma,  $\alpha$  is surjective. To show that  $\alpha$  is injective, let  $x \in M$ . Choose n so large that  $x \notin t^nM$ , and draw the same diagram as above, but with  $t^n$  in place of t. Then x does not become 0 in  $M/t^nM$ , and  $M/t^nM \cong H^O(DD(M/t^nM))$ , so  $\alpha(x) \neq 0$ .

Thus M is reflexive. Taking M = A, we find that R' is a dualizing complex. q.e.d.

Proposition 2.6. Let X be a locally noetherian prescheme, let  $R^* \in D^+_{\mathbf{C}}(X)_{\text{fid}}$  be a dualizing complex, and let D be the functor  $\mathbb{R} \ \underline{\text{Hom}}^*(\cdot,R^*)$ . Then

- a). A complex  $G' \in D_{\mathbf{C}}^{\mathbf{b}}(X)$  has finite Tor-dimension [II 4.2] if and only if D(G') has finite injective dimension.
  - b). There is a functorial isomorphism

$$D(R \text{ Hom}^{\cdot}(F^{\cdot},G^{\cdot})) \xrightarrow{\sim} F^{\cdot} \otimes D(G^{\cdot})$$

for  $F^* \in D_{\mathbf{C}}^-(X)$  and  $G^* \in D^+(X)$ , or for  $F^* \in D_{\mathbf{C}}(X)$  and  $G^* \in D^+(X)_{fid}$ .

c). There is a functorial isomorphism

$$D(F^{\bullet} \otimes G^{\bullet}) \xrightarrow{\sim} R \xrightarrow{Hom^{\bullet}} (F^{\bullet}, D(G^{\bullet}))$$

for F and G  $\in D_{\mathbf{C}}(X)$ , or for F  $\in D_{\mathbf{C}}(X)$  and G  $\in D_{\mathbf{C}}^{\mathbf{b}}(X)_{\mathbf{fTd}}$ .

Proof. The natural map of sheaves

$$F \otimes Hom(G,R) \longrightarrow Hom(Hom(F,G),R)$$

gives rise to a morphism of functors on the derived category,

(\*) 
$$F' \otimes R \underline{\text{Hom}}^*(G',R') \longrightarrow R \underline{\text{Hom}}^*(R \underline{\text{Hom}}^*(F',G'),R'),$$

provided either

- 1)  $F^* \in D^{-}(X)$ ,  $G^* \in D^{+}(X)$  and  $R^* \in D^{+}(X)_{fid}$ , or
- 2)  $F^* \in D(X)$ ,  $G^*, R^* \in D^+(X)$ , and  $R = Hom^*(G^*, R^*) \in D^b(X)_{fTd}^*$ . If under the set of conditions 1), we assume furthermore that  $F^* \in D^-_C(X)$ , then by [I.7.1], the morphism (\*) is an isomorphism. Indeed, we reduce to the case  $F = \mathcal{O}_X$ , which is trivial. Taking the inverse isomorphism gives b) under the first set of hypotheses. As a corollary, we see that if  $G^* \in D^+(X)$  has finite injective

As a corollary, we see that if  $G^* \in D^+(X)$  has finite injective dimension, then  $D(G^*)$  has finite Tor-dimension. Indeed, by the Remark following [II 4.2] it is enough to show that there is an integer  $n_0$  such that  $\underline{Tor}_i(F,G^*) = 0$  for all  $i > n_0$ 

and all coherent sheaves F on X, and this follows from b). Thus we have established one half of a). Now if  $G^* \in D^+(X)_{fid}$ , then as just remarked,  $D(G^*) \in D^b(X)_{fTd}$ , so by 2) and [I.7.1] again, we obtain the isomorphism b) under the second set of conditions.

For statement c), let  $F^*,G^*\in D^-_{\bf C}(X)$ , apply b) to  $F^*$  and  $D(G^*)$ , and apply D to the resulting isomorphism. Then since  $D^2={\rm id}$  on  $D^-_{\bf C}(X)$ , we have the required isomorphism under the first set of conditions. As a corollary we deduce (using [II 7.20  $(\underline{{\rm iii}})_{\bf C}$ ]) that if  $G^*\in D^{\rm b}_{\bf C}(X)$  has finite Tor-dimension, then  $D(G^*)$  has finite injective dimension. This gives the other half of a), and applying D to the second half of b) gives the second half of c).

§3. The Uniqueness of the Dualizing Complex.

Theorem 3.1. Let X be a connected, locally noetherian prescheme, and let R' be a dualizing complex on X. Let  $R'' \in D_C^+(X)$  be any other complex. Then R' is a dualizing complex if and only if there exists an invertible sheaf L on X, and an integer n, such that

$$R'' \cong R' \otimes L[n]$$
.

Furthermore, L and n are determined uniquely to within isomorphism.

Proof. 1) Observe that such an R' is a dualizing complex. Indeed, we may assume that R' is a bounded complex of quasicoherent injectives. Then R' & L[n] is also a bounded complex of injectives, since the property of being injective is local [II 7.16], and L is locally free. R' is dualizing by Corollary 2.3.

- 2) Observe that L and n are uniquely determined by the identity  $L[n] \cong R$  Hom'(R',R'').
- 3) Now we show that existence of L and n, assuming that R' is a dualizing complex. Let D and D' be the dualizing

functors corresponding to R' and R'. Define

$$L' = D'D(O_X) = \mathbb{R} \operatorname{Hom}'(R',R'')$$
.

We will prove that L' is isomorphic, in  $D^+(X)$ , to a complex of the form L[n], where L is an invertible sheaf, and that  $R' \cdot \cong R \cdot \boxtimes L'$ .

Lemma 3.2. There is a natural functorial isomorphism, for all  $M^{\bullet} \in D_{\mathbf{C}}^{-}(X)$ ,

$$M. \otimes \Gamma. \xrightarrow{\sim} D.D(W.)$$

(Note that this tensor product makes sense since  $L^* \in D^-_{\mathbf{C}}(X)$ , cf. [II §4].)

<u>Proof.</u> As in Lemma 1.2 above, one defines a functorial homomorphism

$$M^{\bullet} \otimes \underline{R} \xrightarrow{\text{Hom}^{\bullet}} (R^{\bullet}, R^{\bullet}) \xrightarrow{} \underline{R} \xrightarrow{\text{Hom}^{\bullet}} (\underline{R} \xrightarrow{\text{Hom}^{\bullet}} (M^{\bullet}, R^{\bullet}), R^{\bullet}).$$

Since it is an isomorphism for  $M^{\bullet} = \mathcal{O}_{X}^{\bullet}$ , by the lemma on way-out functors, it is an isomorphism for all  $M^{\bullet} \in D_{C}^{\bullet}(X)$ .

We now define L' = DD'( $\theta_X'$ ), and use the lemma to deduce that

$$L^* \overset{\otimes}{=} L'^* = D'D(L'^*) = D'DDD'(O_X) = O_X^*$$

Lemma 3.3. Let X be a connected locally noetherian prescheme, and let L',L''  $\in D_{\mathbf{C}}^{-}(X)$  be such that L'  $\cong$  L''  $\cong$   $\mathscr{O}_{X}$ . Then L' = L[n] for some invertible sheaf L, and L'' = L'[-n].

Proof. Since X is connected, we reduce immediately to the case where X is the spectrum of a local noetherian ring A, and we wish to show that  $L' = \mathcal{O}_X[n]$  for some n. Let p be the largest integer such that  $H^p(L') \neq 0$ , and let q be the largest integer such that  $H^q(L'') \neq 0$ . Then one sees easily that p+q is the largest integer for which  $H^n(L' \otimes L'') \neq 0$ , and  $H^{p+q}(L' \otimes L'') = H^p(L') \otimes H^q(L'')$ . Therefore p+q = 0, and  $H^p(L') \otimes H^q(L'') = \mathcal{O}_X$ . It follows, by a simple lemma on modules of finite type over a local noetherian ring [cf. EGA, Ch. 0, 5.4.3], that  $H^p(L') \cong H^q(L'') \cong \mathcal{O}_X$ . Now since  $\mathcal{O}_X$  is locally free, one shows that  $L' = L_1' \oplus \mathcal{O}_X[-p]$ , where  $L_1'$  has cohomology only in dimensions < p. Similarly,  $L'' = L_1'' \oplus \mathcal{O}_X[p]$ . Thus from  $L' \otimes L'' \cong \mathcal{O}_X$  we deduce

$$L_{1}^{\bullet}[p] \oplus L_{1}^{\bullet}[-p] \oplus (L_{1}^{\bullet} \oplus L_{1}^{\bullet}) = 0$$

from which it follows that  $L_1$  and  $L_1'$  are 0 in  $D_C(X)$ , so that  $L' \cong \mathcal{O}_X[-p]$ , and  $L' \cong \mathcal{O}_X[p]$ , as required.

This proves the lemma, so we have only to show that  $R'' = R^* \underset{=}{\otimes} L^*$ . Indeed,  $R^* \in D^b_{\bf c}(X)$ , so applying Lemma 3.2,

$$R \stackrel{\bullet}{\underset{=}{\otimes}} L^{\bullet} = D'D(R^{\bullet}) = D'(\mathcal{O}_{X}) = R'^{\bullet}$$
 q.e.d. Theorem.

We now give an application of the uniqueness theorem.

<u>Proposition 3.4</u>. Let A be a noetherian local ring with residue field k, and let  $R^* \in D^+_{\bf c}(A)$ . Then  $R^*$  is dualizing if and only if there is an integer d such that

$$\operatorname{Ext}^{\mathbf{i}}(k,R^{*}) = \begin{cases} 0 & \text{for } i \neq d \\ k & \text{for } i = d. \end{cases}$$

(Here we write D<sup>+</sup>(A) for the derived category of the category of A-modules. The subscript c denotes complexes whose cohomology modules are of finite type. We carry over the definitions and results of the previous sections to this case. (Cf. [II.7.19] which ensures that we will not get into trouble.))

<u>Proof.</u> First suppose that R' is dualizing, and let  $j: Spec k \longrightarrow Spec A$  be the inclusion. Then by Proposition 2.4,

$$j^{\flat}(R^{\bullet}) = \underline{\underline{R}} \text{ Hom}^{\bullet}(k,R^{\bullet})$$

is a dualizing complex on k. But k itself is a dualizing complex on k, so by the Uniqueness Theorem above,  $j^{\frac{1}{k}}(R^{\bullet}) \cong k[-d] \text{ for some d. This d will do.}$ 

For the converse, it is clear that k is reflexive, so by Proposition 2.5 we have only to show that  $R^*$  has finite injective dimension. Indeed, we will show by induction on  $r = \dim M$ , for any A-module M of finite type, that

$$\operatorname{Ext}^{i}(M,R^{\bullet}) = 0$$
 for  $i \notin [d-r,d]$ .

Indeed, for dim M = 0, M is of finite length, and our statement follows from the case M = k by induction on the length of M.

For dim M = r > 0, we induct as in the proof of Proposition 2.5. First we may assume that  $M \notin Ass M$ , where M is the maximal ideal of A. Then choosing  $t \in M$  with t a non-zero-divisor in M, we have

$$0 \longrightarrow M \xrightarrow{t} M \longrightarrow M/tM \longrightarrow 0$$

and dim M/tM < r. Then for i  $\notin [d-r+1,d]$  we have  $Ext^i(M/tM,R^*)=0$ , hence for i  $\notin [d-r,d]$  we have from the long exact sequence of  $Ext^is$ ,

$$\operatorname{Ext}^{i}(M,R^{\bullet}) \xrightarrow{t} \operatorname{Ext}^{i}(M,R^{\bullet}) \longrightarrow 0$$
.

It follows by Nakayama's lemma that  $Ext^{i}(M,R^{\bullet}) = 0$ . q.e.d.

Corollary 3.5. Let A be a noetherian local ring, and let  $R^* \in D^+_{\mathbf{C}}(A)$ . Then  $R^*$  is dualizing on A if and only if  $R^* \otimes_{\widehat{A}} \hat{A}$  is dualizing on the completion  $\hat{A}$  of A.

<u>Proof.</u> Clearly  $R^* \otimes_{\hat{A}} \hat{A} \in D_{\hat{C}}^{+}(\hat{A})$ . Furthermore,

$$\operatorname{Ext}_{\hat{A}}^{i}(k, R^{\bullet} \otimes_{\hat{A}} \hat{A}) = \operatorname{Ext}_{\hat{A}}^{i}(k, R^{\bullet}) \otimes_{\hat{A}} \hat{A}$$

for all i. Thus the "only if" implication is clear. For the "if" implication, note that the functor  $\otimes_{\hat{A}} \hat{A}$  is faithfully flat, so if M is a non-zero A-module, then M  $\otimes_{\hat{A}} \hat{A}$  is non-zero. Furthermore, if M is an A-module, such that  $M \otimes_{\hat{A}} \hat{A} \cong k$ , then  $M \cong k$ . (Indeed, map M to k via the natural map  $M \longrightarrow M \otimes_{\hat{A}} \hat{A}$ . This map becomes an isomorphism upon tensoring with  $\hat{A}$ , hence was an isomorphism). The result thus follows from the proposition.

#### §4. Local Cohomology on a Prescheme.

Let X be a prescheme, Y a closed subset, and F a sheaf of  $\mathcal{O}_X$ -modules. We interpret the local cohomology groups  $H_Y^i(F)$  in terms of Ext's.

For each  $n \geq 1$ , let  $Y_n$  be the subscheme of X defined by the sheaf of ideals  $I_Y^n$ , where  $I_Y$  is the sheaf of ideals of some scheme structure on Y. Then for each n we have a natural map

$$\text{Hom}_{\mathcal{O}_{\mathbf{X}}}(\mathcal{O}_{\mathbf{Y}_{\mathbf{n}}}, F) \longrightarrow \Gamma_{\mathbf{Y}}(F)$$
 ,

since an element of the first group is given by a global section of F which is annihilated by  $I_Y^n$ , and hence has support on Y. Taking the direct limit as n varies, we deduce a map

$$\xrightarrow[n]{\text{lim }} \text{Hom}(\sigma_{Y_n}, F) \longrightarrow \Gamma_{Y}(F).$$

Taking derived functors, we deduce a map of functors from  $D^{+}(X)$  to  $D^{+}(Ab)$ 

(\*) 
$$\underset{=}{\mathbb{R}} \xrightarrow{\lim} \operatorname{Hom}(\mathscr{O}_{Y_n}, F^{\bullet}) \longrightarrow \underset{=}{\mathbb{R}} \Gamma_{Y}(F^{\bullet}) .$$

Theorem 4.1. If X is a noetherian prescheme, and  $F' \in D^+_{qc}(X)$ , i.e., the complex F' has quasi-coherent cohomology (cf. [II §17]), then (\*) is an isomorphism.

Remarks. 1. Since there are enough flasque  $\mathcal{O}_X$ -modules,  $\underline{\underline{R}} \Gamma_{\underline{Y}}(F^*)$  is the same as if one had calculated it in the category  $\underline{D}^+$  (abelian sheaves on X).

2. The derived category does not have direct limits, so we cannot write  $\lim_{n \to \infty} \mathbb{R}^n \to \mathbb{R}^n$  Hom $(\mathcal{O}_{Y_n}, F^*)$ , as one is tempted to. However, upon descending from the derived category this difficulty disappears, and we have the Corollary below.

Corollary 4.2. Under the hypotheses of the theorem, the map induced on cohomology,

$$\xrightarrow[n]{\text{lim}} \operatorname{Ext}^{i}(\mathscr{O}_{Y_{n}}, F^{\bullet}) \longrightarrow H_{Y}^{i}(F^{\bullet})$$

is an isomorphism, for all i.

Proofs. If X is noetherian, and F quasi-coherent, then
the map

$$\xrightarrow{\text{lim}} \text{Hom}(\mathcal{O}_{\mathbf{Y}_{\mathbf{n}}}, \mathbf{F}) \longrightarrow \Gamma_{\mathbf{Y}}(\mathbf{F})$$

is an isomorphism, since every section of F with support on Y will be annihilated by some power of  $I_Y$ . Therefore, by the lemma on Way-Out Functors [I.7.1], the morphism of derived functors (\*) is an isomorphism for  $F^* \in D^+_{GC}(X)$ .

For the Corollary, just observe that taking cohomology of complexes commutes with direct limits.

Corollary 4.3. If X is locally noetherian, and  $F^* \in D^+_{gc}(X)$ , then the analogous maps

$$\underset{=}{\mathbb{R}} \xrightarrow{\text{lim}} \xrightarrow{\text{Hom}} (\mathscr{O}_{Y_n}, F^*) \longrightarrow \underset{=}{\mathbb{R}} \underline{\Gamma}_{Y}(F^*)$$

and

$$\underset{n}{\underset{\longrightarrow}{\text{lim}}} \xrightarrow{\text{Ext}^{i}} (\mathscr{O}_{Y_{n}}, F^{*}) \xrightarrow{\longrightarrow} \underline{H}_{Y}^{i}(F^{*})$$

are isomorphisms.

<u>Proof.</u> By definition of the derived category, it is sufficient to prove the second. This follows from Corollary 4.2, since  $\underline{\text{Ext}}$  and  $\underline{\text{H}}_{\underline{\text{Y}}}$  are sheaves associated to presheaves given by  $\underline{\text{Ext}}$  and  $\underline{\text{H}}_{\underline{\text{Y}}}$ .

## §5. Dualizing functors on a local noetherian ring.

In this section we recall without proof the definition and some properties of dualizing functors on a local noetherian ring A, with maximal ideal 4M. For proofs, see [LC,84].

Proposition 5.1. Let I be an injective hull of the residue field k of A, and denote by T the functor Hom(·,I). Then for every A-module M of finite length, the natural map

$$M \longrightarrow T T(M)$$

is an isomorphism.

Definition. A contravariant additive functor T from the category  $C_f$  of A-modules of finite length into itself is called a <u>dualizing functor for A at M</u> if there exists an injective hull I of k and an isomorphism of functors  $T \cong Hom(\cdot, I)$ .

Proposition 5.2. A contravariant additive functor T from  $\mathcal{C}_f$  into itself is a dualizing functor if and only if it is exact, and  $T(k) \cong k$ . In that case one can take  $I = \underset{n}{\text{lim}} T(A/M^n)$ , and then there is a canonical isomorphism  $T \cong \text{Hom}(\cdot, I)$ .

Proposition 5.3. If I is an injective hull of k, then the functor Hom(·,I) gives an anti-isomorphism of the category (dcc) of A-modules with descending chain condition (we call them A-modules of co-finite type) and the category (acc) of modules of finite type over the completion of A.

# §6. Local Duality.

Throughout this section we let A be a noetherian local ring, with maximal ideal M, and residue field k, and let R' be a dualizing complex on  $X = \operatorname{Spec} A$  (cf. §2). Recall Proposition 3.4 which gives a necessary and sufficient condition for a complex  $R' \in D^+_C(A)$  to be dualizing.

<u>Definition</u>. We say that the dualizing complex R° is normalized if the integer d of Proposition 3.4 is zero.

Remark. Since the translate of a dualizing complex is again one, we can normalize by translation.

Proposition 6.1. If R° is normalized, then  $\mathbb{R}^{\Gamma}_{\mathbf{X}}(\mathbf{R}^{\bullet})$ , where  $\mathbf{x}$  is the closed point of Spec A, is isomorphic in the derived category to an injective hull I of k.

<u>Proof.</u> The cohomology of  $\underline{\underline{R}} \Gamma_{\mathbf{x}}(\mathbf{R}^*)$  is

$$H_{\mathbf{X}}^{\mathbf{i}}(\mathbf{R}^{\bullet}) \cong \underset{\mathbf{n}}{\overset{\mathbf{lim}}{=}} \operatorname{Ext}^{\mathbf{i}}(\mathbf{A}/\mathbf{m}^{\mathbf{n}},\mathbf{R}^{\bullet})$$

by Corollary 4.2 above. On the other hand, we saw from the proof of Proposition 3.4 that  $\operatorname{Ext}^{\mathbf{i}}(M,R^*)=0$  for  $\mathbf{i}\neq 0$  and all M of finite length. Furthermore, by Proposition 5.2, the functor  $\operatorname{Ext}^{\mathbf{0}}(\cdot,R^*)$  is a dualizing functor, and corresponds to

the injective hull of k given by

$$I = \underset{n}{\underline{\lim}} \operatorname{Ext}^{O}(A/m^{n}, R^{\bullet}).$$

So we see that  $H_{\mathbf{X}}^{\mathbf{i}}(\mathbf{R}^*) = 0$  for  $\mathbf{i} \neq 0$ , and  $H_{\mathbf{X}}^{\mathbf{o}}(\mathbf{R}^*) = \mathbf{I}$ . Therefore  $\mathbf{R} \Gamma_{\mathbf{X}}(\mathbf{R}^*) \cong \mathbf{I}$  in the derived category [1.4.3].

Now let M be an A-module. Then there is a natural homomorphism

$$\Gamma_{\mathbf{x}}(M) \longrightarrow \text{Hom}(\text{Hom}(M,R^{\bullet}), \Gamma_{\mathbf{x}}(R^{\bullet})).$$

This gives rise to a morphism of functors on  $D^+(A)$ ,

$$\underline{\underline{R}} \Gamma_{\mathbf{x}}(\mathbf{M}^{\bullet}) \longrightarrow \underline{\underline{R}} \operatorname{Hom}(\underline{\underline{R}} \operatorname{Hom}(\mathbf{M}^{\bullet}, \mathbf{R}^{\bullet}), \underline{\underline{R}} \Gamma_{\mathbf{x}}(\mathbf{R}^{\bullet}))$$
,

since we can take R° to be an injective complex, in which case  $\underset{=}{\mathbb{R}} \Gamma_{\mathbf{X}}(\mathbf{R}^*) = \Gamma_{\mathbf{X}}(\mathbf{R}^*)$  is also injective. Indeed, whenever J is an injective A-module, and Y a closed subset of Spec A, then  $\Gamma_{\mathbf{Y}}(\mathbf{J})$  is injective (cf. [II §7] for the structure of injective A-modules). We now assume (without loss of generality) that R° is normalized, and so, by the Proposition, have a morphism of functors

$$\Theta\colon \ \underline{\mathbb{R}} \ \Gamma_{\mathbf{x}}(M^{\bullet}) \longrightarrow \operatorname{Hom}(\underline{\mathbb{R}} \ \operatorname{Hom}(M^{\bullet},\mathbb{R}^{\bullet}), \ \mathbf{I}).$$

(Following the usual conventions, we do not write R before a functor which is already exact.)

Theorem 6.2 (Local Duality). Let A be a local noetherian ring, let R' be a normalized dualizing complex, let I be the corresponding injective hull of k, and let  $M^* \in D^+_C(A)$  (i.e., the cohomology modules of M' are of finite type). Then  $\Theta$  as defined above is an isomorphism.

Corollary 6.3. With A, R', I as above, let M be a module of finite type. Then the homomorphisms

$$\Theta^{i}: H_{\mathbf{x}}^{i}(M) \longrightarrow \text{Hom } (Ext^{-i}(M,R^{\bullet}), I)$$

induced by  $\Theta$  are isomorphisms.

<u>Proof.</u> Using the Lemma on Way-out Functors [I.7.1] one sees that the Corollary is equivalent to the theorem. To prove the Corollary, note that  $\theta^{i}$  is an isomorphism for M = k, because  $H_{\mathbf{X}}^{i}(\mathbf{k}) = 0$  for  $i \neq 0$ , and  $H_{\mathbf{X}}^{O}(\mathbf{k}) = \mathbf{k}$ ; note also that for all M of finite type, both sides are modules with support at  $\mathbf{x}$ . Thus we are reduced to proving the following

<u>LEMMA 6.4</u>. Let  $\theta^i$ :  $S^i \longrightarrow T^i$  be a morphism of covariant cohomological functors on the category of modules over a noetherian ring A. Assume

- (i) for every maximal ideal  $_{MM} \subseteq A$ ,  $\Theta^{i}(A/_{MM})$  is an isomorphism, and
- (ii) for every non-maximal prime ideal  $p \subseteq A$ ,  $S^{i}(A/p)$  and  $T^{i}(A/p)$  have support < Supp A/p.

Then  $\Theta^{i}(M)$  is an isomorphism for every A-module M of finite type.

<u>Proof.</u> By assumption,  $\Theta^{i}(A/w)$  is an isomorphism for every maximal ideal w. If M is any module of finite type, then M admits a finite filtration each of whose quotients is of the form A/p with p prime. Thus by the 5-lemma we reduce to the case M = A/p with p not maximal. By noetherian induction, we may assume that  $\Theta^{i}(M')$  is an isomorphism for every M' of finite type with support < Supp (A/p).

Now for each  $f \in M = A/\mathcal{P}$ ,  $f \neq 0$ , we consider the exact sequence

$$0 \longrightarrow M \xrightarrow{f} M \longrightarrow M/fM \longrightarrow 0 ,$$

and apply the functors Si, Ti to it, splitting it as follows:

$$0 \longrightarrow K_{f} \longrightarrow S^{i}(M) \xrightarrow{f} S^{i}(M) \longrightarrow \cdots$$

$$\downarrow^{\alpha} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{\beta} \qquad \downarrow^{$$

and

$$\begin{array}{cccccccccccccccccccccccccccccccccccc$$

Now by our induction hypothesis,  $\delta$  is an isomorphism, so  $\alpha$  is surjective. Since Supp  $S^i(M) <$  Supp M by our assumption (ii), each element of  $S^i(M)$  is annihilated by some non-zero  $f \in M$ . Thus  $S^i(M) = \bigcup K_f$  as f ranges over the non-zero elements of M. Similarly  $T^i(M) = \bigcup L_f$ . Therefore  $\beta$  is surjective. This is true for each i, so also  $\gamma$  is surjective. But that implies  $\alpha$  is injective, so  $\alpha$  is an isomorphism. Then, as above,  $\beta$  is also an isomorphism.

Corollary 6.5. For M of finite type, the modules  $H_X^i(M)$  are of co-finite type (see Proposition 5.3), and we have a functorial isomorphism

$$\operatorname{Ext}^{\mathbf{i}}(M,R^{*})^{\wedge} \longrightarrow \operatorname{Hom}(H_{\mathbf{x}}^{-\mathbf{i}}(M), I)$$

of A-modules.

<u>Proof.</u> Apply the functor Hom  $(\cdot,I)$  to the isomorphism  $\theta^{i}$ , and use the fact that for any A-module of finite type M, this functor applied twice gives the completion  $\hat{M}$ . [LC p. 61].

Remark. If A is a regular local ring, then A itself is a dualizing complex for A (see Example 2.2), and we recover the old local duality theorem [LC 6.3]. This is also true more generally for Gorenstein local rings (Theorem 9.1 below).

#### §7. Application to Dualizing Complexes.

Let X be a locally noetherian prescheme, and let R' be a dualizing complex on X. Then for each point  $x \in X$ ,  $R_X^*$  is a dualizing complex for the local ring  $\mathcal{O}_X$  (Corollary 2.3). Thus by Proposition 3.4 we can find an integer d(x) such that

$$\operatorname{Ext}_{\mathcal{O}_{\mathbf{x}}}^{\mathbf{i}}(\mathbf{k}(\mathbf{x}), \mathbf{R}_{\mathbf{x}}^{\bullet}) = \begin{cases} 0 & \text{for } \mathbf{i} \neq d(\mathbf{x}) \\ \mathbf{k}(\mathbf{x}) & \text{for } \mathbf{i} = d(\mathbf{x}) \end{cases}.$$

Proposition 7.1. With the hypotheses above, if  $x \longrightarrow y$  is an immediate specialization, then

$$d(y) = d(x) + 1.$$

Proof. Since the question is local around y, we may assume that  $X = \text{Spec } \mathcal{O}_{Y}$ .

Let Z be the reduced induced subscheme structure on  $\{x\}$ , and let  $j: Z \longrightarrow X$  be the inclusion. Then  $j^{\flat}R^{\bullet}$  is dualizing on Z by Proposition 2.4, and for any  $\mathscr{O}_Z$ -module F we have

$$\operatorname{Ext}_{0_{\mathbb{Z}}}^{i}(F, j^{\flat}R^{\bullet}) = \operatorname{Ext}_{0_{\mathbb{X}}}^{i}(j_{*}F, R^{\bullet})$$

by duality for j [III 6.7]. Thus d(x), d(y) are the same if calculated on Z with  $j^{b}R^{*}$ , and so we reduce to the case X = Z integral local of dimension 1, with generic point x and closed point y.

By translating, we may assume that R' is normalized, i.e., d(y) = 0. To calculate d(x) we consider  $\operatorname{Ext}_{k(x)}^i(k(x),R') = \operatorname{Ext}_{A}^i(A,R') \otimes_{A} k(x)$ , where  $X = \operatorname{Spec} A$ . Now by the local duality theorem,  $\operatorname{Ext}_{A}^i(A,R')$  is dual to  $\operatorname{H}_{Y}^{-i}(A)$ . Since A is a domain,  $\operatorname{H}_{Y}^{0}(A) = 0$ . For  $p \neq 0,1$ ,  $\operatorname{H}_{Y}^{p}(A) = 0$  since A is of dimension 1 [LC 1.12]. Thus  $\operatorname{Ext}^i(A,R') = 0$  for  $i \neq -1$ , and so d(x) = -1, as required.

<u>Definition</u>. An integer-valued function d on a prescheme X with the property of the proposition will be called a <u>codimension</u> function on X.

<u>Definition</u>. A prescheme X is <u>catenary</u> if whenever  $Z \subseteq Z'$  are irreducible closed subsets of X, then every maximal chain

$$Z = Z_0 < Z_1 < \cdots < Z_n = Z'$$

of irreducible closed subsets between Z and Z' has the same length n.

Corollary 7.2. A locally noetherian prescheme X which admits a dualizing complex is catenary, and has finite Krull dimension.

<u>Proof.</u> Indeed, the existence of a codimension function d on X implies that X is catenary. On the other hand, since R° is quasi-isomorphic to a bounded complex of injective sheaves, the function d is bounded in both directions, so X has finite Krull dimension.

Definition. Let X be a locally noetherian prescheme, and let R' be a dualizing complex on X. We define the <u>filtration</u>
Z' associated to R' by

$$z^{p} = \{x \in X | d(x) > p\}$$

for each p. Then by virtue of the previous proposition and corollary, Z is a finite filtration of X, and each  $x \in Z^p_{-Z}^{p+1}$  is maximal.

Proposition 7.3. Let X be a locally noetherian prescheme, let R' be a dualizing complex on X, and let Z' be the associated filtration. Then R' is Gorenstein with respect to Z' (cf. [IV §3]). Moreover, for each  $x \in X$ , the injective hull J(x) of k(x) over  $O_X$  occurs exactly once as a direct summand of the (injective) complex  $E(R^*)$ .

Proof. Using condition (ii) of [IV 3.1] and [IV.1.F], it\nis sufficient to show that

$$H_{\mathbf{x}}^{\mathbf{i}}(\mathbf{R}^{\bullet}) = \begin{cases} 0 & \text{for } \mathbf{i} \neq d(\mathbf{x}) \\ J(\mathbf{x}) & \text{for } \mathbf{i} = d(\mathbf{x}). \end{cases}$$

But this follows from Proposition 6.1 above.

# §8. Pointwise dualizing complexes and f#.

In this section we give a generalization of the notion of dualizing complex, which may exist on a locally noetherian prescheme of infinite Krull dimension. We apply this notion to show that f<sup>#</sup> of a dualizing complex is dualizing, where f is a smooth morphism. Throughout this section, X will denote a locally noetherian prescheme.

Definition. A complex  $R^* \in D_{\mathbf{C}}^+(X)$  has pointwise finite injective dimension (pfid) if for every  $\mathbf{x} \in X$ ,  $R_{\mathbf{x}}^* \in D_{\mathbf{C}}^+(Spec \mathcal{O}_{\mathbf{x}}^*)$  has finite injective dimension.

Proposition 8.1. Let  $R^* \in D_{\mathbf{C}}^+(X)$  have pointwise finite injective dimension. Then conditions (i)-(iv) of Proposition 2.1 are equivalent.

<u>Proof.</u> The same as loc. cit. since one can check reflexivity pointwise.

<u>Definition</u>. A complex  $R^* \in D^+_C(X)$  with pfid is <u>pointwise</u> dualizing if it satisfies the equivalent conditions of the proposition.

Remarks. 1. Since fid implies pfid, we see that any dualizing complex is pointwise dualizing.

2. If X = Spec A where A is a local ring, then
fid pfid, so a complex is dualizing if and only if it is

pointwise dualizing.

- 3. We say a complex  $F^* \in D(X)$  is <u>pointwise bounded</u>

  <u>below</u> if for every  $x \in X$ ,  $F_X^* \in D^+(Spec\ \mathcal{O}_X)$ , and we write  $F^* \in D^{p+}(X)$ . Similarly we define  $D^{p-}(X)$  and  $D^{pb}(X)$ . These are full subcategories of D(X) (cf. [I §§4,5]). Now if  $R^* \in D_C^+(X)$  is pointwise dualizing, then the functor  $R \to D^{p-}(X)$  gives an anti-isomorphism of  $D^{p-}$  and  $D^{p+}$ , and an auto-anti-isomorphism of  $D^{pb}(X)$ .
- 4. If R° is a pointwise dualizing complex on X, we can define as in \$7 the associated codimension function d: X  $\longrightarrow$  Z, and the associated filtration Z°. Proposition 7.1 holds in this case, so the filtration Z° satisfies the conditions of [IV \$3], in particular, it is separated. Thus we see as in Corollary 7.2 that X is catenary.
- 5. If R' is pointwise dualizing on X, and if R'  $\in D_{\mathbb{C}}^{\mathbb{D}}(X)$ , then R' is Gorenstein with respect to the filtration Z' (cf. Proposition 7.3). The boundedness hypothesis is necessary for [IV 3.1].

Example. If X is a regular prescheme, then  $\mathcal{O}_X$  is a pointwise dualizing complex for X. Indeed, for each  $x \in X$ ,

Spec  $\mathcal{O}_{\mathbf{x}}$  is a regular prescheme of finite Krull dimension, so we apply Example 2.2 above.

Proposition 8.2. Let  $R' \in D_{\mathbf{C}}^{+}(X)$  be pointwise dualizing, and assume that X is noetherian and of finite Krull dimension. Then R' has finite injective dimension and so is dualizing (by Proposition 2.3).

<u>Proof.</u> Since X is noetherian and of finite Krull dimension, the codimension function d associated to R' is bounded. But we saw in the proof of Proposition 3.4 that for every  $x \in X$ , and every module M of finite type over  $\mathcal{O}_{x}$ ,

Ext
$$_{\mathcal{O}_{\mathbf{x}}}^{\mathbf{i}}(M, R_{\mathbf{x}}^{\bullet}) = 0$$
 for  $\mathbf{i} \notin [d(\mathbf{x})-\dim M, d(\mathbf{x})].$ 

Thus in particular for every coherent sheaf F on X,

$$\underbrace{\operatorname{Ext}}_{X}^{i}(F,R^{*}) = 0 \qquad \text{for } i > \sup_{x \in X} d(x) ,$$

and so R° has finite injective dimension [II 7.20  $(\underline{iii})_{c}$ ].

Theorem 8.3. Let  $f: X \longrightarrow Y$  be a smooth morphism of locally noetherian preschemes, and let  $R^{\bullet} \in D^{+}_{\mathbf{C}}(Y)$  be pointwise dualizing. Then  $f^{\sharp}(R^{\bullet})$  (cf. [III §2]) is pointwise dualizing on X. If furthermore Y is noetherian, f of finite type, and  $R^{\bullet}$  dualizing, then  $f^{\sharp}(R^{\bullet})$  is also dualizing.

<u>Proof.</u> For the first statement, the question is local on X and Y, so we reduce immediately to the case Y = Spec A, with A a local ring, and X of finite type, affine over Y. Then X admits a closed immersion into a suitable affine space  $\mathbf{A}_{\mathbf{Y}}^{\mathbf{n}}$ , so using [III 8.4] and Proposition 2.4 (which is valid also for "pointwise dualizing"), we reduce to the case X =  $\mathbf{A}_{\mathbf{Y}}^{\mathbf{n}}$ .

Case 1. A is a regular local ring. Then R' is dualizing, since A is local, and by uniqueness (Theorem 3.1) we may assume, after shifting if necessary, that  $R' \cong A$ . Then  $f^*(R') \cong \omega_{X/Y} = \Omega_{X/Y}^n$ , which is locally free of rank one, and hence pointwise dualizing (Example 2.2, since X is regular if Y is).

Case 2. A is a quotient of a regular local ring A'. Let Y' = Spec A'. Then X is obtained from the morphism  $A_{Y'}^{n} \longrightarrow Y'$  by the base extension  $Y \longrightarrow Y'$ , and we reduce to the previous case by means of [III.6.4], Proposition 2.4, the uniqueness (Theorem 3.1) on Y.

General case. A is an arbitrary noetherian local ring.

Let  $\hat{A}$  be the completion of A, and let Y' = Spec  $\hat{A}$ . We make the base extension u: Y'  $\longrightarrow$  Y, and then  $u^*(R^*)$  is dualizing on Y' by Corollary 3.5. But  $\hat{A}$  is a quotient of a regular local

ring by Cohen's structure theorem [ 14,(31.1)], so  $f^{'*}(u^*(R^*))$  is dualizing on  $X' = X \times_{Y} Y'$ , by Case 2. Now for any point  $x \in X$ , the completion  $\hat{\mathcal{O}}_{X}$  of its local ring is also the completion of the ring  $\mathcal{O}_{X} \otimes_{A} \hat{A}$ , which is the semilocal ring of the points of X' lying over x, and so applying Corollary 3.5 once in each direction, and [III 2.1] we see that  $f^{*}(R^*)$  is pointwise dualizing on X.

Now if Y is noetherian, f of finite type, and R° dualizing, then Y has finite Krull dimension by Corollary 7.2, hence X has finite Krull dimension, and so  $f^*(R^*)$  is dualizing by Proposition 8.2.

Corollary 8.4. Under the hypotheses of the theorem, let  $d_{Y}$  and  $d_{X}$  be the codimension functions associated with the pointwise dualizing complexes R' and  $f^{\#}(R^{\bullet})$ , respectively. Then for each  $x \in X$ ,

$$d_{x}(x) = d_{y}(y) + tr.d. k(x)/k(y)$$

where y = f(x).

<u>Proof.</u> Chasing through the reductions above (and noting that this formula holds trivially for a finite morphism and  $f^{\flat}(R^{*})$ ), we reduce to the case Y = Spec A, A a regular local

ring,  $R^* = A$ , and  $X = AA_Y^n$ . Then  $f^*(R^*) = \omega_{X/Y}$ , which is locally free of rank one, so for any  $x \in X$  we have  $d_X(x) = \dim \mathcal{O}_X$ , and for any  $y \in Y$ ,  $d_Y(y) = \dim \mathcal{O}_Y$ . [LC §4]. Our formula is then the usual dimension formula for a local homomorphism of local rings (cf. [EGA  $O_{IV}$  17.3.3]).

Remark. Using Proposition 2.4, the result of the theorem can be extended to show that for any embeddable morphism f of noetherian preschemes [III §8], f' takes dualizing complexes to dualizing complexes. The formula of the Corollary also extends to this case.

<u>Proposition 8.5.</u> Let  $f: X \longrightarrow Y$  be an embeddable morphism of locally noetherian preschemes, let  $R^* \in D^+_C(Y)$  be a dualizing complex on Y, and let D denote the functor  $\frac{R}{L} \xrightarrow{Hom^*_Y}(\cdot, R^*)$  or  $\frac{R}{L} \xrightarrow{Hom^*_X}(\cdot, f^!R^*)$  (the one meant will be clear from the context). Then there is a functorial isomorphism

$$f'(F') \cong D(\underline{L}f^*(D(F')))$$

for all  $F^* \in D_{C}^{+}(Y)$ .

Proof. Apply [III 8.8, 7)] to D(F') and R'.

Corollary 8.6. Under the hypotheses of the proposition, assume furthermore that f is flat, of finite type, and that Y is noetherian. Then there is a functorial isomorphism

$$f'(F'\otimes G') \xrightarrow{\sim} f'(F') \otimes f'(G')$$

for 
$$F^* \in D_{\mathbf{C}}^+(Y)$$
 and  $G^* \in D_{\mathbf{C}}^{\mathbf{b}}(Y)_{\mathbf{fTd}}$ .

Proof. Note first that Theorem 8.3 and the Remark following apply to show that f'(R') is dualizing on X. The result now follows from the Proposition, using [II 5.8] and Proposition 2.6 above.

### \$9. Gorenstein preschemes.

Theorem 9.1. Let A be a noetherian local ring. Then the following conditions are equivalent:

- (i) A is a dualizing complex for itself.
- (ii) A has a finite injective resolution.
- (iii) A is Cohen-Macaulay-1 (i.e., A is Cohen-Macaulay, and whenever  $x_1, \dots, x_n$  is a maximal A-sequence, then the ideal  $(x_1, \dots, x_n)$  is irreducible.)
  - (iv) There is an integer d such that

$$\operatorname{Ext}^{\mathbf{i}}(k,A) = \left\{ \begin{array}{l} 0 & \text{for } i \neq d \\ \\ k & \text{for } i = d \end{array} \right.$$

where k is the residue field of A.

- (v) A is Gorenstein with respect to a suitable
  filtration Z\* of Spec A (cf. [IV \$3]).
  - (vi) There is an integer d such that

$$H_{\mathbf{X}}^{\mathbf{i}}(\mathbf{A})$$
 { = 0 for  $\mathbf{i} \neq \mathbf{d}$  is injective for  $\mathbf{i} = \mathbf{d}$ 

where x is the closed point of Spec A.

- Proofs. (i)  $\Longrightarrow$  (ii) By definition of dualizing complex.
- (ii) ←→ (iii) ←→(iv) Proved by Bass
  [2, Theorem 4.1]. This article, incidentally, is a good
  summary of all previous occurrences of Gorenstein rings in
  the literature.
  - (iv) (i) This is Proposition 3.4 above.
  - (i)  $\Longrightarrow$  (v) This is Proposition 7.3 above.
- $(v) \Longrightarrow (vi)$  By [IV 3.4], E(A) is an injective resolution of A, and furthermore, for each  $p \in \mathbb{Z}$ ,  $E^p(A)$  is a direct sum of constant (injective) sheaves on subspaces  $\{y\}^-$  of Spec A with  $y \in Z^p Z^{p+1}$ . We can calculate  $H_X^i(A)$  as  $H^i(\Gamma_X(E(A)))$ . But  $\Gamma_X(E(A))$  by what we have just seen, consists of a single injective sheaf in some degree (say d), since x is a minimal point of Spec A.
- $(vi) \longrightarrow (iii)$  First note by [LC 6.4, part 4] that  $H_X^n(A) \neq 0$ , where  $n = \dim A$ , so n = d. (The hypothesis in loc. cit. that A is a quotient of a regular local ring can be circumvented by passing to the completion [LC 5.9].) Therefore A is Cohen-Macaulay [LC 3.10]. Let  $(x_1, \dots, x_n)$  be a maximal A-sequence, and let  $(x_1, \dots, x_n)$ . Then

 $H_X^n(A)$  is an essential extension of A/N [11, proof of Prop. 2], and so is irreducible, since A/N is a simple A-module, and hence irreducible. We conclude that  $H_X^n(A)$  is an irreducible injective A-module with support at x, and so is an injective hull of k [II 7.4].

Now for any A-module M,

Hom 
$$(k,M) = \text{Hom } (k, \Gamma_{\mathbf{x}}(M)).$$

Furthermore, the functor  $\Gamma_{\mathbf{x}}$  takes injectives into injectives, so we have a spectral sequence of derived functors, which degenerates in this case to give

$$\operatorname{Ext}^{i}(k,A) = \operatorname{Hom}(k, H_{X}^{n}(A)) = \begin{cases} 0 & i \neq n \\ k & i = n \end{cases}$$

<u>Definition</u>. A local noetherian ring satisfying the equivalent conditions of the theorem is called a (local) Gorenstein ring.

Remark. For a local ring, regular --> complete intersection --> Gorenstein --> Cohen-Macaulay, and these implications are all strict [2].

<u>Definition</u>. A prescheme is <u>Gorenstein</u> if all of its local rings are Gorenstein local rings.

Corollary 9.2. A localization of a Gorenstein local ring is Gorenstein.

<u>Proof.</u> Follows from condition (i) of the Theorem, and
Corollary 2.3 above.

Proposition 9.3. Let  $f: X \longrightarrow Spec k$  be an embeddable morphism, where k is a field. Then X is Gorenstein if and only if f'(k) is isomorphic, in  $D^+(X)$ , to an invertible sheaf on X.

<u>Proof.</u> Indeed, by the remark at the end of the last section, f'(k) is a dualizing complex on X. But X is Gorenstein if and only if  $O_X'$  is a dualizing complex on X. So the result follows from the uniqueness of the dualizing complex (Theorem 3.1 above).

Corollary 9.4. Let X be a Gorenstein prescheme of finite type over a field k, and let  $k \subseteq K$  be a field extension. Then  $X \otimes_k K$  is also Gorenstein.

<u>Proof.</u> The question is local on X, and f' is compatible with flat base extension [III 8.7, 5)].

Corollary 9.5. Let K,L be extension fields of a field k, and assume that one of them is finitely generated. Then  $K \otimes_k L$  is a Gorenstein ring (i.e., every localization of it is a local Gorenstein ring).

Proof. Similar to the above. One can also give a direct proof, by induction on the number of generators. This generalizes [EGA IV 6.7.1.1] which says that K&L is Cohen-Macaulay.

<u>Proposition 9.6.</u> Let  $f: X \longrightarrow Y$  be a flat morphism of locally noetherian preschemes, with Y Gorenstein (but no finiteness assumption on f). Then X is Gorenstein if and only if all the fibres  $X_{Y}$ , for  $Y \in Y$ , are Gorenstein preschemes.

<u>Proof.</u> The question is local, so we reduce to the following: let  $A \longrightarrow B$  be a local homomorphism of local rings, with A Gorenstein, and B flat over A. Then B is Gorenstein if and only if  $B/M_AB$  is Gorenstein.

To prove this, we use condition (iv) of Theorem 9.1. By flatness.

$$\operatorname{Ext}_{B}^{i}(B/m_{A}B, B) = \begin{cases} 0 & \text{for } i \neq d \\ B/m_{A}B & \text{for } i = d \end{cases}$$

for a suitable d. Thus the spectral sequence of Ext's for the

change of ring from B to  $B/M_AB$  degenerates, and we have

$$\operatorname{Ext}_{B}^{i}(k_{B}, B) \cong \operatorname{Ext}_{B/M_{A}B}^{i-d}(k_{B}, B/M_{A}B)$$

for each i, whence the result.

Exercise 9.7. Let  $f: X \longrightarrow Y$  be a flat morphism of finite type of locally noetherian preschemes. Show that  $f'(O'_Y)$  (which is defined locally on X) is isomorphic in  $D^+(X)$  to an invertible sheaf if and only if all the fibres  $X_Y$  of Y, for  $Y \in Y$ , are Gorenstein preschemes. Also show that Y has a unique non-zero cohomology sheaf, which is flat over Y, if and only if all the fibres of Y are Cohen-Macaulay preschemes. Such morphisms are called Gorenstein morphisms (resp. Cohen-Macaulay morphisms).

Compare [EGA IV 6.3 and 6.7] for statements analogous to Corollary 9.5 and Proposition 9.6 for Cohen-Macaulay.

### §10. Existence of Dualizing Complexes.

We now draw together the experience gained in this chapter to make some remarks about the existence of a dualizing complex on a locally noetherian prescheme X.

(We leave the analogous discussion for pointwise dualizing complexes to the reader.)

Sufficient conditions. 1. If X is Gorenstein and of finite Krull dimension, then  $\mathcal{O}_X$  is a dualizing complex for X. In particular, any regular prescheme of finite Krull dimension has a dualizing complex.

- 2. If f: X
- 3. In particular, any prescheme of finite type over a field k admits a dualizing complex.
- 4. If X is the spectrum of a complete local ring A, then X admits a dualizing complex. Indeed, A is a quotient of a regular local ring by the Cohen structure theorem [14, (31.1)].

Necessary conditions. 1. If X admits a dualizing complex, then X has finite Krull dimension (Corollary 7.2).

- 2. If X admits a dualizing complex, then X is catenary (in fact universally catenary since any prescheme of finite type over X admits a dualizing complex, at least locally).
  - 3. More precisely, X admits a codimension function d.
- 4. If A is a local noetherian ring admitting a dualizing complex, and if  $p \subseteq A$  is a prime ideal, then  $\widehat{A} \otimes_{\widehat{A}} k(p)$  is a Gorenstein ring. This follows from the following

Proposition 10.1. If A is a local noetherian domain, with quotient field K, which admits a dualizing complex, then  $\hat{A} \otimes_A K$  is a Gorenstein ring.

Proof. Let R' be a dualizing complex on A. Then  $R^* \otimes_A \widehat{A}$  is dualizing on  $\widehat{A}$  by Corollary 3.5, and so by localization,  $(R^* \otimes_A \widehat{A}) \otimes_A K$  is dualizing on  $\widehat{A} \otimes_A K$ . But  $R^* \otimes_A K$  is dualizing on K, so by Theorem 3.1 we may assume  $R^* \otimes_A K \cong K$  after translating if necessary. But  $(R^* \otimes_A \widehat{A}) \otimes_A K \cong (R^* \otimes_A K) \otimes_K (\widehat{A} \otimes_A K)$  so  $\widehat{A} \otimes_A K$  is a dualizing complex for itself, and we are done (Theorem 9.1 (i)).

Example. There are local noetherian domains of dimension 3 which are not catenary, and local noetherian domains of dimension 2 which are not universally catenary, and which therefore have no dualizing complexes [14, Appendix Al, Ex. 2].

Problems. 1. We do now know if  $\hat{A} \otimes_{\hat{A}} K$  is a Gorenstein ring, even if A is a local domain of dimension 1, hence we do not know whether every local domain of dimension 1 admits a dualizing complex.

2. If X is noetherian and of finite Krull dimension, and if it admits a dualizing complex locally, and if it admits a codimension function d, we do not know whether X admits a dualizing complex globally.

#### CHAPTER VI. RESIDUAL COMPLEXES

#### \$0. Introduction.

In this chapter we return to the problem of constructing a functor f' for a morphism of finite type, which should reduce to f' for a finite morphism, and f\* for a smooth morphism. We ran into difficulty earlier [III §8] because the derived category is not a local object — one cannot glue together elements of the derived category given locally. Now we overcome that difficulty in a special case by using residual complexes. The residual complex is a very special complex of quasi-coherent injective sheaves (see definition below) which is almost unique (it was called "residue complex" in the Edinburgh Congress talk [9]).

Modulo some technicalities arising from possibly infinite Krull dimension, this is how they work: To each dualizing complex  $R^* \in D^+_C(X)$  is associated functorially a residual complex  $K^* = E(R^*)$ , and  $Q(K^*)$  (which is the image of the complex  $K^*$  in  $D^+_C(X)$ ) is isomorphic to  $R^*$  in  $D^+_C(X)$ . Thus we will define  $f^*$  locally for a residual complex  $K^*$  by