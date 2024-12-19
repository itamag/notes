Here’s the revised text with definitions of key terms for clarity and rigor:  

---

# Special Relativity and Lorentz Scalars  

> [!NOTE] **Key Points to Remember**  
> - **Postulates of Special Relativity**:  
>   1. The laws of physics are the same in all **inertial frames**.  
>   2. The speed of light \( c \) is constant in all inertial frames.  
> - **Inertial Frame**: A reference frame moving with constant velocity (no acceleration).  
> - **Lorentz Transformation**: Relates spacetime coordinates between inertial frames.  
> - **Lorentz Scalar**: A quantity invariant under Lorentz transformations.  

## Overview  

Special relativity, formulated by Einstein, describes the behavior of objects at high velocities, where Newtonian mechanics fails. It is based on two postulates:  

1. The laws of physics are identical in all **inertial frames**, which are reference frames moving with constant velocity (no acceleration).  
2. The speed of light \( c \) in vacuum is constant, independent of the motion of the source or the observer.  

## Lorentz Transformation  

The **Lorentz transformations** describe how spacetime coordinates \((t, x, y, z)\) in one inertial frame relate to those in another frame moving at velocity \( v \) relative to the first along the \( x \)-axis:  

$$ 
t' = \gamma \left( t - \frac{vx}{c^2} \right), \quad x' = \gamma (x - vt), \quad y' = y, \quad z' = z, 
$$  

where \( \gamma = \frac{1}{\sqrt{1 - \frac{v^2}{c^2}}} \) is the **Lorentz factor**.  

## Lorentz Scalars  

A **Lorentz scalar** is a physical quantity that remains unchanged under Lorentz transformations, ensuring the consistency of physical laws across all inertial frames. Common examples include:  

1. **Spacetime Interval**:  
   $$ s^2 = c^2t^2 - x^2 - y^2 - z^2, $$  
   which is invariant for all observers, representing the "distance" between two events in spacetime.  

2. **Dot Product of Four-Vectors**:  
   For four-vectors \( A^\mu = (A^0, \mathbf{A}) \) and \( B^\mu = (B^0, \mathbf{B}) \):  
   $$ A^\mu B_\mu = A^0 B^0 - \mathbf{A} \cdot \mathbf{B}, $$  
   which remains invariant under Lorentz transformations.  



Here’s a concise introduction to Minkowski spacetime in the requested format:

---

# Minkowski Spacetime  

> [!NOTE] **Key Points to Remember**  
> - **Minkowski Spacetime**: A four-dimensional spacetime combining space and time into a unified framework.  
> - **Metric Signature**:  
>   $$  
>   ds^2 = c^2 dt^2 - dx^2 - dy^2 - dz^2,  
>   $$  
>   where \( ds^2 \) is invariant under Lorentz transformations.  
> - **Events**: Points in spacetime specified by four coordinates \( (t, x, y, z) \).  
> - **Causal Structure**: Defines time-like, space-like, and light-like intervals.  
> - $$d t = \gamma_{v} d\tau$$
> - We get Newton's relativistic equation: $\dot{p} = \frac{d}{dt}(m \gamma_{v}v) = \frac{d}{dt}(m_{v}v)$

## Overview  

Minkowski spacetime, developed by Hermann Minkowski, is the mathematical framework for special relativity. It treats space and time as interwoven into a four-dimensional manifold, where each point, called an **event**, is described by coordinates \( (t, x, y, z) \).  

## Metric and Invariance  

The geometry of Minkowski spacetime is defined by the **metric tensor**:  

$$  
\begin{align}
 & ds^2 = c^2 dt^2 - d^2r \\
 & d \tau^2 = 1 - \left( \frac{v}{c} \right)^2
\end{align}
$$  

where \( ds^2 \) is the **spacetime interval**, a Lorentz scalar invariant under Lorentz transformations. The interval classifies events as:  
- **Time-like** (\( ds^2 > 0 \)): Events can be causally connected.  
- **Space-like** (\( ds^2 < 0 \)): Events are separated by distances greater than light can travel.  
- **Light-like** (\( ds^2 = 0 \)): Events connected by light signals.  

## Four-Vectors  

In Minkowski spacetime, physical quantities are described by **four-vectors** $A^\mu = (A^0, \mathbf{A})$, with components:  
- $A^0$: Time-like component, often multiplied by $c$$.  
- $\mathbf{A}$: Space-like components in $x, y, z$.  
Their dot product is defined as:  
$$  
A^\mu B_\mu = A^0 B^0 - \mathbf{A} \cdot \mathbf{B}.  
$$
> [!definition]- The Velocity Four-Vector
> $$
> U^\mu = \frac{dx^\mu}{d\tau} = \frac{1}{\gamma_{v}} \frac{dx^\mu}{dt}
> $$
## Causal Structure  

The causal relationship between two events is determined by \( ds^2 \):  
1. **Time-like Separation**: \( ds^2 > 0 \), within the light cone.  
2. **Space-like Separation**: \( ds^2 < 0 \), outside the light cone.  
3. **Light-like Separation**: \( ds^2 = 0 \), on the light cone.  

# חלקיק חופשי יחסותי במבט אנליטי

הנחות יסוד:
- באנליטית רגילה, הפעולה היא מספר.
- נניח שהפעולה היא סקלר במובן הטנזורי - אינווריאנטית לשינוי בסיס [[Tensor Analysis#In a Nutshell]]

יעד:
- למצוא פעולה/לגרנז'יאן שיתנו את הפיזיקה הרגילה בגבול של מהירויות נמוכות

פתרון:
ננחש שהאינטגרנד הוא [[Differential Forms|one-form]] ונקבל:

$$
S_0 = -mc \int_{t_{1}}^{t_{2}}ds
$$
כאשר $ds$ היא המרחק במרחב מינקובסקי. 

קשיים:
- למה הלגרנז'יאן הוא לא סקלר? יש כאן שקר כלשהו


יעד: פתרון משוואות התנועה מעקרון המילטון

דרך: 
1. קודם צריך לפתור את המד"ר  $ds = dx_{\mu}dx^{\mu}$  כדי להבין את הפונקציונל בקורדינטות הנכונות
2. אחרי זה גוזרים את  $\delta(ds)$ [[Calculus of Variation|בלי לדפוק חשבון]]
3. מגלים שהתאוצה מתאפסת ולכן התנע נשמר

יעד: עבור מסלול פיזיקלי, מה הנגזרת של הפעולה(נשכח מתנאי שפה)?

דרך: האינטגרל לא ישפיע על המסלול, רק איבר השפה:
$$
\delta S_{0} = -m U_{\mu} \delta x^\mu \implies \frac{ \partial S_{0} }{ \partial x^\mu }  = -m U_{\mu} = -P_{\mu}
$$

