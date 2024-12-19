# Week 1

- בקלאסית 2, בנינו את התאוריה לפי: אמפיריקה -> משוואות דינמיות -> משוואות מקסוול
- בקורס הזה, נלך בכיוון ההפוך: לגרנז'יאן -> משוואות דינמיות -> איך פותרים אותן ואמפיריקה
### חזרה על אנליטית
- חזרה על אנליטית:
	- מתחילים מחוקי ניוטון במרחב קרטזי ומפתחים מהן את עקרון המילטון בקורדינטות כלליות


> [!theorem] עקרון המילטון
> עבור מערכת דינמית משמרת עם N דרגות חופש בת"ל, הדינמיקה נקבעת ע"י הלגרנז'יאן:
> $$
> L = E_{\text{kinetic}} - E_{\text{potential}} = L(\vec{q}, \dot{\vec{q}}, t)
> $$
> עם הפעולה
> $$
> S = \int L \cdot dt = S[\vec{q}]
> $$
> עקרון המילטון אומר: המסלול הפיזיקלי של הקורידנטות $\vec{q}(t)$ הוא זה שעבורו:
> $$0=\delta{\mathcal{S}}_{\delta\xi}[\xi,t_{1},t_{0}]=\int_{t_{0}}^{t_{1}}\left({\frac{\partial{\mathcal{L}}}{\partial\mathbf{q}}}-{\frac{d}{d t}}{\frac{\partial{\mathcal{L}}}{\partial{\dot{\mathbf{q}}}}}\right)\delta\xi\,d t+{\frac{\partial{\mathcal{L}}}{\partial{\dot{\mathbf{q}}}}}\,\delta{\xi}{\Big|}_{t_{0}}^{t_{1}},$$
 כאשר $\delta\xi=\delta\xi(t)$ זה שדה וקטורי לאורך עקומה $\xi$ במרחב הקונפיגורציה
  
 בדר"כ מאפסים את תנאי השפה, אבל עכשיו נבחר לא לעשות זאת. נקבל עבור מסלול פיזיקלי:
 
 $$\delta{\mathcal{S}}_{\delta\xi}[\xi,t;t_{0}]={\frac{\partial{\mathcal{L}}}{\partial{\dot{\mathbf{q}}}}}{\Big|}_{{\dot{\mathbf{q}}}={\dot{\xi}}(t)}^{\mathbf{q}=\xi(t)}\ \delta\xi(t)$$
 שנותן:
 $$\left.\frac{\partial S}{\partial q^{i}}=\frac{\partial{\mathcal{L}}}{\partial{\dot{q}}^{i}}\right|_{\mathbf{q}=\mathbf{v}} = P_{i}$$

>[!theorem] Hamilton Equations
> $${\frac{\mathrm{d}q}{\mathrm{d}t}}={\frac{\partial{\mathcal{H}}}{\partial{\boldsymbol{p}}}},\quad{\frac{\mathrm{d}{\boldsymbol{p}}}{\mathrm{d}t}}=-{\frac{\partial{\mathcal{H}}}{\partial{\boldsymbol{q}}}}$$

פרטים חשובים מאנליטית:
- אם קורידנטה חסרה ב-L אז התנע הצמוד שלה שמור
- אם t לא מופיע במפורש ב-L (או ב-H) אז H גודל שמור
- משוואות התנועה אינן משתנות כאשר מוסיפים או כופלים בקבוע ל-L, או כאשר מוסיפים ל-L נגזרת שלמה בזמן של פונקציה $f(\vec{q})$. 

### הכללה של עיקרון המילטון עבור שדות

בקונטקסט המקורי של אנליטית הפתרון הוא $\vec{q}(t)$, כלומר המערכת הפיזיקלית מתוארת ע"י אוסף של קורדינטות. בחשמליטית המערכת תתואר על ידי אוסף בדיד של קורדינטות עבור כל נקודה על יריעה ולכן הפתרון יהיה $\vec{q}(\vec{r}, t)$. אפשר לחשוב על כל נקודה במרחב כחלקיק פיזיקלי שמנסים לפתור (אינטואיציה בלבד).

 [[Lagrangian Mechanics#Hamilton's Principle and Euler-Lagrange Equations for Field Theory]]

### הפעולה של חלקיק יחסותי
[[Special Relativity#Metric and Invariance]]
כדי להבטיח את עקרון היחסות, נוכל לבחור פעולה שהיא סקלר לורנץ. הסקלר הכי מתבקש - האינטרוול/המרחק במרחב מינקובסקי!

# Week 2
### פעולה של חלקיק טעון בשדה א"מ
הנחות:
1. עקרון היחסות, וממנו נובע שהפעולה תהיה סקלר.
2. הפעולה צריכה להיות פרופורציונית לינארית לגודל המטען
3. הפוטנציאל הא"מ הוא איננו סקלר (בגלל היחסות של מהירות המטען), אז נניח ארבע-וקטור
4. עקרון הסופרפוזיציה - הפעולה אדיטיבית בפוטנציאל הא"מ

> [!theorem]
> $$
> S_{\text{int}} = -\frac{q}{c} \int A_{\mu}dx^\mu = -\frac{q}{c}\int[cA_{0} - \vec{A}\cdot \vec{v}]dt
> $$

[[Charged Relativistic Particle in EM Field]]
[[The Electromagnetic Field Tensor]]
[[Covariant Formulation of EM#^e46cdb]]
[[Covariant Formulation of EM#^e4f0a0]]

# Week 3

1. So far we've talked about the action of a particle under a given EM field but the phenomena aren't separate. Now we'd like to build a new action: [[Hamilton's Principle for the EM Field]]. It generalizes our work in two way: (1) we'll replace particles by continuous charge densities (2) we'll consider the generation of EM fields by the particles.
2. [[Charged Relativistic Particle in EM Field#Reworking the interaction action for charge densities]]
3. [[Hamilton's Principle for the EM Field]] - Finding the field action
4. 

# Week 4 - EM field Lagrangian, CFT
![[Pasted image 20241209104648.png]]
 ([pdf](zotero://open-pdf/library/items/UJIRB2VR?page=1&annotation=IF334PZV))

# Week 5 - EM-statics as superposition problems

- [[Maxwell Equations#Maxwell's Static Equations]]
	- [[Maxwell Equations#Superposition Problems for Static Maxwell]]
	- [[The EM Field Potential#^27e14d]] 
	- [[Hamilton's Principle for the EM Field#Summary]]
		- [[Hamilton's Principle for the EM Field#^93d106]] 
		- [[Hamilton's Principle for the EM Field#^d5e94f]] 
	- $${\cal F}_{\mathrm{mag}}=\frac{I}{c}\int d{\boldsymbol{l}}\times{\boldsymbol{B}}=\frac{1}{c}\int{\boldsymbol{J}}\left({\boldsymbol{r}}\right)\times{\boldsymbol{B}}\left({\boldsymbol{r}}\right)d^{3}{\boldsymbol{r}}$$ 
# Week 6 - Multipole Expansion
- [[Multipole Expansion]]
	- [[Multipole Expansion#^facfa1]] 
	- And more
- [[Electrostatic Energy#Under external field]]

## Rec 1
### Tensors, Differential Geometry

Subscripts represent column index, superscripts represent row index. So, $a_{i}$ is a row vector, and $a^i$ is a column vector. For a matrix $M$, its entry $M_{ij} \iff M_{j}^i$ and the equation $\mathbf{y} = M \mathbf{x} \iff y^i = M^i_{j}x^j$

The symbol $e$ represents a basis **matrix**, and $\hat{e}_{j}$ is a column vector of this matrix. Our rule for change of basis is: $r^i \hat{e}_{i} = {r'}^i \hat{e'}_{i} \iff \hat{e} \mathbf{r} = \hat{e'} \mathbf{r'}$. If $\mathbf{r'} = O \mathbf{r} \iff {r'}^i = O^i_{j}r^j$, then $\hat{e'} = \hat{e}O^{-1} \iff \hat{e'}^{i}_{j} =\hat{e}^i_{k}{O^{-1}}^k_{j} \iff \hat{e'}_{j} =\hat{e}_{k}{O^{-1}}^k_{j}$

>[!warning] Reading and writing tensor products
>When reading matrix products in index notation, the order of reading should be
>$$
>X^a_{b} \cdot Y^b_{c} \cdot Z^c_{d} \cdots
>$$
>![[Pasted image 20241112131455.png]]
>$$
{T'}^{i_{1}\dots}_{j_{1}\dots} = O^{i_{1}}_{{a_{i}}}\cdot(O^{-1})^{b_{1}}_{{j_{1}}} \cdots T^{a_{1}\dots}_{b_{1}\dots}
$$






>[!note]
>In tensor analysis, we have column/contravariant/coordinate/superscript vectors and row/covariant/tangent/subscript vectors



# 