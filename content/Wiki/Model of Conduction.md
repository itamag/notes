# מודל דרודה

## כיתה
מודל פנומנולוגי כדי להסביר את חוק אוהם $\vec{j} = \sigma\vec{{E}}$
- הנחות:
	- האלקטרונים הם גז חופשי טעון (סטטיסטית)
	- האלקטרון מתפזר (לא מסבירים איך או ממה). בפיזור, התנע שלו מתאפס.
	- ההסתברות לפיזור בפרק זמן $dt$ היא $\frac{dt}{\tau}$
	- בין פיזורים האלקטרון נתון להשפעת כוחות חיצוניים לא ידועים
- יעד: לגזור את חוק אוהם
- דרך:
	- מחשבים את התנע הממוצע בזמן $t+dt$ עד כדי דיפרנציאל ראשון (אם אין התנגשות התנע לא משתנה, אם יש התנגשות אז בממוצע מקבלים תוספת) 
	- מקבלים מד"ר שתלויה בכוח
	- מציבים כוח קולון $-e \vec{E}$
	- $\vec{j} = -en \vec{v} = -\frac{en}{m}\vec{p}$
	- שוב קיבלנו סקלה - מוליכות דרודה. במקרה הזה היא אשכרה המוליכות לפי המודל
		- נשים לב שככל שזמן הפיזור הממוצע גדל, המוליכות גדלה
	- עוברים לסקאלת אורך - $v \tau$ כאשר המהירות היא [[חוק החלוקה השווה#מהירות תרמית]] (זאת הנחה שגויה)
	- 




> [!theorem] חישוב ההסתברות
> $$\mathbf{p}(t_{0}+d t)=\left(1-{\frac{d t}{\tau}}\right)\left[\mathbf{p}(t_{0})+\mathbf{f}(t)d t+O(d t^{2})\right]+{\frac{d t}{\tau}}\left(\mathbf{g}(t_{0})+\mathbf{f}(t)d t+O(d t^{2})\right)$$
> $${\frac{d}{d t}}\mathbf{p}(t)=\mathbf{f}(t)-{\frac{\mathbf{p}(t)}{\tau}}$$




## מרמין
![[Pasted image 20241128130418.png]]

“BASIC ASSUMPTIONS OF THE DRUDE MODEL” ([pdf](zotero://open-pdf/library/items/2CHG866D?page=26&annotation=92HFFDX3)):
1. בין התנגשויות/פיזורים, האינטרקציות בין אלקטרון לאלקטרונים האחרים והן בינו לבין היונים/גרעינים זניחות. לכן, אם לא מופעלים על המתכת כוחות חיצוניים האלקטרונים ינועו במהירות קבועה בין פיזורים.
2. ההתנגשויות הן מאורע מיידי (שינוי מיידי במהירות). 
3. ההסתברות שאלקטרון יחווה התנגשות בפרק זמן $dt$ היא $\frac{dt}{\tau}$, ולכן הזמן הממוצע בין התנגשויות הוא $\tau$. לשים לב: $\tau$/זמן הרגיעה לא תלוי במיקום או במהירות של האלקטרון
4. מגיעים לש"מ באופן הבא: באיזורים עם טמפ' גבוהה, המהירות הממוצעת לאחר התנגשות תהיה גבוהה יותר. ככה אלקטרונים יזרמו מאזור חם לאזור קר עד שיווי משקל.

“DC ELECTRICAL CONDUCTIVITY OF A METAL” ([pdf](zotero://open-pdf/library/items/2CHG866D?page=30&annotation=MIUBFE5S))
“HALL EFFECT AND MAGNETORESISTANCE” ([pdf](zotero://open-pdf/library/items/2CHG866D?page=35&annotation=U7E8B7BM))
“THERMAL CONDUCTIVITY OF A METAL” ([pdf](zotero://open-pdf/library/items/2CHG866D?page=43&annotation=DXNZF2GH))


# Drude-Sommerfeld

>[!note]
>“We shall find that room temperature, for the electron gas at metallic densities, is a very low temperature indeed, for many purposes indistinguishable from T = 0." ([pdf](zotero://open-pdf/library/items/2CHG866D?page=54&annotation=MPAE7SBY)) Remember that Sommerfeld approximation is near T=0.

במודל דרודה הקלאסי, קיבלנו קיבול חום שלא מסתדר עם ניסויים. אם מחליפים את ההתפלגות הקלאסית של האנרגיות בהתפלגות קוונטית לפי פרמי-דיראק, זה מסתדר.

“הבדל לעומת [[Model of Conduction#מודל דרודה|מודל דרודה]]  טמון בכך שמיד לאחר כל פיזור, גודל המהירות שבה האלקטרון מתפזר (בכיוון אקראי) נקבע לא לפי התפלגות בולצמן, אלא לפי התפלגות פרמי-דיראק” ([pdf](zotero://open-pdf/library/items/863SHVRM?page=1&annotation=W6AAJEGX)). הערה שלי: הוספנו הנחות קוונטיות על אלקטרונים: ספין חצי ואנרגיה $$\xi(\mathbf{k})=\frac{\;\;\hbar^{2}\mathbf{k}^{2}}{2m}$$

>[!theorem] Speed distribution after scattering in Drude-Sommerfeld
>By assuming the above dispersion relation for the electrons and remembering $\vec{v}=\hbar \frac{\vec{k}}{m}$, we can calculate the microstate density in velocity space from the microstate density in the k-space, which we already know:
>$$P(v)\propto{\frac{1}{e^{\beta\left({\frac{1}{2}}m v^{2}-\mu\right)}+1}}$$

בעצם הוספנו התייחסות לקוונטוט של האנרגיות. עכשיו כשעברנו להתפלגות פרמי-דיראק, אפשר להשתמש [[Sommerfeld Approximation|בקירוב זומרפלד]]. בשבילו אנחנו רק צריכים לדעת את צפיפות מצבי המיקרו ברמת אנרגיה ליחידת נפח (של החומר/מתכת):
$$g(\mathcal{E})=\frac{3}{2}\frac{n}{\mathcal{E}_{F}}\left(\frac{\mathcal{E}}{\mathcal{E}_{F}}\right)^{1/2},\qquad\mathcal{E}>0;$$
מה שנותן:
$$\mu=\varepsilon_{F}\left[1-\frac13\left(\frac{\pi k_{B}T}{2\varepsilon_{F}}\right)^{2}\right]$$
ותחת הנחות המודל שלנו (גז אלקטרונים *חופשיים*):
$$c_{v}=\frac{\pi^{2}}{2}\left(\frac{k_{B}T}{{\mathcal E}_{F}}\right)n k_{B}$$
בטמפרטורת החדר זה יוצא בערך 1% מקיבול החום של [[Model of Conduction#מודל דרודה|מודל דרודה המקורי]]. במילים אחרות, כמעט כל קיבול החום הסגולי של המתכת לא מגיע מהאלקטרונים החופשיים, אלא מרמות האנרגיה הקשורות / האלקטרונים הקשורים (מקוונטים 1 ו[[The Hydrogen Atom Model]] אנחנו יודעים שהרמות הנמוכות מתאימות לרדיוסים קטנים סביב גרעין האטום). מרמין אומר:

>[!note] Mermin's take on the Sommerfeld heat capacity
>“If one is willing to dispense with the precise numerical coefficient, one can understand this behavior of the specific heat quite simply from the temperature dependence of the Fermi function itself. The increase in energy of the electrons when the temperature is raised from T = 0 comes about entirely because some electrons with energies within O(kBT) / below E_F (the darkly shaded region of Figure 2.4) have been excited to an energy range of O(kBT) / above E_F (the lightly shaded region of Figure 2.4). The number of electrons per unit volume that have been so excited is the width, kBT , of the energy interval times the density of levels per unit volume g .EF /. Furthermore, the excitation energy is of order kBT , and hence the total thermal energy density is of order g .EF / .kBT /2 above the ground-state energy. This misses the precise result (2.79) by a factor of 2=6, but it gives a simple physical picture, and is useful for rough estimates.” ([pdf](zotero://open-pdf/library/items/2CHG866D?page=68&annotation=XMDAAJA8))


>[!theorem] Cheatsheet
>Thermal Conductivity:$$\kappa={\frac{1}{3}}v^{2}\tau c_{v}$$
>
>$${\frac{\kappa}{\sigma T}}={\frac{\pi^{2}}{3}}\left({\frac{k_{B}}{e}}\right)^{2}=2.44\times10^{-8}\,{\mathrm{walt\,ohm/K}}^{2}$$
>Thermopower:
>$$Q=-\frac{\pi^{2}}{6}\frac{k_{B}}{e}\left(\frac{k_{B}T}{{\mathcal E}_{F}}\right)=-1.42\left(\frac{k_{B}T}{{\mathcal E}_{F}}\right)\times10^{-4}\,\mathrm{volt/K}$$
> ([pdf](zotero://open-pdf/library/items/2CHG866D?page=73&annotation=MTYB27A5))

“THERMAL PROPERTIES OF THE FREE ELECTRON GAS: APPLICATIONS OF THE FERMI-DIRAC DISTRIBUTION” ([pdf](zotero://open-pdf/library/items/2CHG866D?page=64&annotation=9IJ7MUNW))

