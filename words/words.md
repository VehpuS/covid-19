```{=html5}
<fold>
```

"The only thing to fear is fear itself" was stupid advice.

והעיקר, אמרו לנו, לא לפחד כלל.

Sure, don't hoard toilet paper – but if policymakers fear fear itself, they'll downplay real dangers to avoid "mass panic". Fear's not the problem, it's how we *channel* our fear. Fear gives us energy to deal with dangers now, and prepare for dangers later.

אין צורך לאגור נייר טואלט, אבל יש מקום לקצת פחד בריא. השאלה היא איך משתמשים בפחד הזה כדי להתמודד עם הבעיות של עכשיו ולהתכונן למה שמצפה לנו.

Honestly, we (Marcel, epidemiologist + Nicky, art/code) are worried. We bet you are, too! That's why we've channelled our fear into making these **playable simulations**, so that *you* can channel your fear into understanding:

גם אנחנו (Marcel, epidemiologist + Nicky, art/code) מודאגים. לכן הכנו את הסימולטור הזה ואתם מוזמנים להשתמש בו כדי להפוך את הפחד שלכם להבנה:

* **החודשים האחרונים** (מבוא לאפידימיולוגיה, מודל SEIR, R ו R<sub>0</sub>)
* **החודשים הקרובים** (סגרים, מעקב מגעים, מסיכות)
* **השנים הקרובות** (איבוד חסינות? יהיה חיסון?)

* **The Last Few Months** (epidemiology 101, SEIR model, R & R<sub>0</sub>)
* **The Next Few Months** (lockdowns, contact tracing, masks)
* **The Next Few Years** (loss of immunity? no vaccine?)

This guide (published May 1st, 2020. click this footnote!→[^timestamp]) is meant to give you hope *and* fear. To beat COVID-19 **in a way that also protects our mental & financial health**, we need optimism to create plans, and pessimism to create backup plans. As Gladys Bronwyn Stern once said, *“The optimist invents the airplane and the pessimist the parachute.”*

המדריך הזה (פורסם בתחילת מאי 2020 →[^timestamp]) והוא מיועד לתת לכם תקווה *וגם* פחד. כדי לנצח את COVID-19 **בדרך שגם תשמור על הבריאות הנפשית והכלכלית שלנו** אנחנו צריכים אופטימיות כדי לתכנן תכניות, ופסימיות כדי לתכנן תכניות גיבוי. כמו שאמר Gladys Bronwyn *"האופטימי ממציא את המטוס והפסימי ממציא את המצנח."*

[^timestamp]: These footnotes will have sources, links, or bonus commentary. Like this commentary!
    
    **This guide was published on May 1st, 2020.** Many details will become outdated, but we're confident this guide will cover 95% of possible futures, and that Epidemiology 101 will remain forever useful.

So, buckle in: we're about to experience some turbulence.

נצא לדרך:

```{=html5}
<div class="section chapter">
    <div>
		<img src="banners/curve.png" height=480 style="position: absolute;"/>
        <div>החודשים האחרונים</div>
    </div>
</div>
```

Pilots use flight simulators to learn how not to crash planes.
טייסים מתשמשים בסימולטורים כדי ללמוד איך לרסק מטוסים ולצאת מזה בשלום.


**Epidemiologists use epidemic simulators to learn how not to crash humanity.**

**אפידימיולוגים משמשים בסימולטרים כדי ללמוד איך להוציא את האנושות בשלום ממגפות.**

So, let's make a very, *very* simple "epidemic flight simulator"! In this simulation, <icon i></icon> Infectious people can turn <icon s></icon> Susceptible people into more <icon i></icon> Infectious people:

 אז למה לא נבנה לנו סימולטור מגפות מאד *מאד* פשטני! בסימולטור הזה, <icon i></icon> אנשים מדבקים יכולים להפוך <icon s></icon> אנשים פגיעים למדבקים (פגיעים הם אנשים שאין להם חסינות והם גם לא חולים או מדבקים בעצמם כרגע).  

![](pics/spread.png)


It's estimated that, *at the start* of a COVID-19 outbreak, the virus jumps from an <icon i></icon> to an <icon s></icon> every 4 days, *on average*.[^serial_interval] (remember, there's a lot of variation)


מעריכים ש*בתחילת* ההתפרצות של COVID-19, הוירוס דילג מ <icon i></icon> ל <icon s></icon>  כל 4 ימים *בממוצע*. (כדאי לזכור שיש כאן שונות מאד גדולה)

[^serial_interval]: “The mean [serial] interval was 3.96 days (95% CI 3.53–4.39 days)”. [Du Z, Xu X, Wu Y, Wang L, Cowling BJ, Ancel Meyers L](https://wwwnc.cdc.gov/eid/article/26/6/20-0357_article) (Disclaimer: Early release articles are not considered as final versions)

If we simulate "double every 4 days" *and nothing else*, on a population starting with just 0.001% <icon i></icon>, what happens? 

אם אנחנו מכניסים לסימולטור שלנו "הכפלה כל 4 ימים" *ושום דבר אחר* על אוכלוסיה שמתחילה עם 0.001% <icon i></icon>, מה יקרה?

**Click "Start" to play the simulation! You can re-play it later with different settings:** (technical caveats: [^caveats])

**לחצו "הפעל" כדי להתחיל את הסימולציה! תוכלו להפעילו אותה שוב אחרי שתסתיים וגם לשחק עם ההגדרות! (הסתייגויות טכניות: [^caveats])

****

[^caveats]: **Remember: all these simulations are super simplified, for educational purposes.**
    
    One simplification: When you tell this simulation "Infect 1 new person every X days", it's actually increasing # of infected by 1/X each day. Same for future settings in these simulations – "Recover every X days" is actually reducing # of infected by 1/X each day.
    
    Those *aren't* exactly the same, but it's close enough, and for educational purposes it's less opaque than setting the transmission/recovery rates directly.

```{=html5}
```{=html5}
<div class="sim">
		<iframe src="sim?stage=epi-1" width="800" height="540"></iframe>
</div>
```
This is the **exponential growth curve.** Starts small, then explodes. "Oh it's just a flu" to "Oh right, flus don't create *mass graves in rich cities*". 

זה **הגידול האקספוננציאלי**. מתחיל קטן, ואז מתפוצץ. "זאת רק שפעת" ואז "משפעת לא נהיים קברים המוניים בערים גדולות של מדינות מפותחות".

![](pics/exponential.png)

But, this simulation is wrong. Exponential growth, thankfully, can't go on forever. One thing that stops a virus from spreading is if others *already* have the virus:

אבל הסימולציה הזו לא נכונה. גידול אקספוננציאלי, למרבה המזל, לא יכול להמשך לנצח. אחד הדברים שעוצר את ההתפשטות של הוירוס הוא כשלאחרים *כבר יש אותו*:

![](pics/susceptibles.png)

The more <icon i></icon>s there are, the faster <icon s></icon>s become <icon i></icon>s, **but the fewer <icon s></icon>s there are, the *slower* <icon s></icon>s become <icon i></icon>s.**

ככל שיש יותר <icon i></icon> מי שהוא <icon s></icon> נהיה <icon i></icon> מהר יותר, **אבל, ככל שיש פחות <icon s></icon>, מי שהוא <icon s></icon> נהיה <icon i></icon> *לאט יותר*.**


How's this change the growth of an epidemic? Let's find out:

איך זה משפיע על התפשטות המגיפה? בואו נראה:

```{=html5}
```{=html5}
<div class="sim">
		<iframe src="sim?stage=epi-2" width="800" height="540"></iframe>
</div>

This is the "S-shaped" **logistic growth curve.** Starts small, explodes, then slows down again.

זו **העקומה הלוגיסטית**. מתחילה בקטן, מתפוצצת, ואז שוב דועכת.

But, this simulation is *still* wrong. We're missing the fact that <icon i></icon> Infectious people eventually stop being infectious, either by 1) recovering, 2) "recovering" with lung damage, or 3) dying.

אבל הסימולציה הזו עדיין לא נכונה. אנחנו מפספסים את העובדה ש  <icon i></icon> אנשים מדבקים בסופו של דבר מפסיקים להדביק. או שהם מחלימים, או שהם "מחלימים" עם נזק לריאות, או שהם מתים.

For simplicity's sake, let's pretend that all <icon i></icon> Infectious people become <icon r></icon> Recovered. (Just remember that in reality, some are dead.) <icon r></icon>s can't be infected again, and let's pretend – *for now!* – that they stay immune for life.

לשם הפשטות, נניח שכל  <icon i></icon> המדביקים נהיים <icon r></icon> מחלימים. (רק נזכור שבמציאות חלק מהם מתים) <icon r></icon> לא יכולים להדביק שוב, ונניח *לעת עתה* שהם נשארים חסינים לשארית חייהם.

With COVID-19, it's estimated you're <icon i></icon> Infectious for 10 days, *on average*.[^infectiousness] That means some folks will recover before 10 days, some after. **Here's what that looks like, with a simulation *starting* with 100% <icon i></icon>:**

ההערכה היא שעם COVID-19 אתה <icon i></icon>מדבק למשך 10 ימים *בממוצע*. זה אומר שחלק יחלימו לפני שיעברו 10 ימים, וחלק אחרי.

[^infectiousness]: “The median communicable period \[...\] was 9.5 days.” [Hu, Z., Song, C., Xu, C. et al](https://link.springer.com/article/10.1007/s11427-020-1661-4) Yes, we know "median" is not the same as "average". For simplified educational purposes, close enough.

```{=html5}
```{=html5}
<div class="sim">
		<iframe src="sim?stage=epi-3" width="800" height="540"></iframe>
</div>

This is the opposite of exponential growth, the **exponential decay curve.**

זה ההפך מגידול אקפוננציאלי - זו עקומה של **דעיכה אקספוננציאלית**.

Now, what happens if you simulate S-shaped logistic growth *with* recovery?

עכשיו, מה יקרה אם נעשה סימולציה של עקומה לוגיסטית *עם* התאוששות?

![](pics/graphs_q.png)

Let's find out.

בואו נראה.

<b style='color:#ff4040'>העקומה האדומה</b> היא מספר המקרים *הנוכחי* <icon i></icon>,    
<b style='color:#999999'>העקומה האפורה</b> היא *סך כל* המקרים (נוכחי + מחלימים <icon r></icon>),
מתחילה בסך הכל ב 0.001% <icon i></icon>:

```{=html5}
<div class="sim">
		<iframe src="sim?stage=epi-4" width="800" height="540"></iframe>
</div>

And *that's* where that famous curve comes from! It's not a bell curve, it's not even a "log-normal" curve. It has no name. But you've seen it a zillion times, and beseeched to flatten.

וזה המקור של העקומה שאנחנו רואים בכל מקום! זו לא עקומת פעמון, זו לא עקומה שאנחנו מכירים ממקום אחר, אבל זו העקומה שהשתלטה על החיים של כולנו ואותה אנחנו מנסים לשטח!

This is the the **SIR Model**,[^sir]    
(<icon s></icon>**S**usceptible <icon i></icon>**I**nfectious <icon r></icon>**R**ecovered)      
the *second*-most important idea in Epidemiology 101:

זה המודל המכונה **SIR Model**
(<icon s></icon>**S**usceptible - פגיעים <icon i></icon>**I**nfectious - מדבקים <icon r></icon>**R**ecovered - מחלימים) 

the *second*-most important idea in Epidemiology 101:
הרעיון *השני* הכי חשוב במבוא לאפידמיולוגיה:


[^sir]: For more technical explanations of the SIR Model, see [the Institute for Disease Modeling](https://www.idmod.org/docs/hiv/model-sir.html#) and [Wikipedia](https://en.wikipedia.org/wiki/Compartmental_models_in_epidemiology#The_SIR_model)

![](pics/sir.png)

**NOTE: The simulations that inform policy are way, *way* more sophisticated than this!** But the SIR Model can still explain the same general findings, even if missing the nuances.

**שימו לב: הסימולציות שמשמשות לקבלת החלטות הרבה*הרבה* יותר מורכבות מזה!** אבל מודל SIR יכול עדיין להסביר כמה ממצאים מרכזיים, אפילו אם הוא מתעלם מכמה ניואנסים.

Actually, let's add one more nuance: before an <icon s></icon> becomes an <icon i></icon>, they first become <icon e></icon> Exposed. This is when they have the virus but can't pass it on yet – infect*ed* but not yet infect*ious*.

למעשה, בואו נוסיף עוד קצת ניואנס: לפני ש<icon s></icon> נהיה <icon i></icon>, הוא נהיה <icon e></icon>נשא (הערת המתרגם: אני לא רופא או אפידמיולוג ולא בטוח שהמונחים פה מדוייקים. עובדים עם מה שיש). זה השלב שבו הוא כבר *נדבק* בוירוס, אבל הוא עדיין לא *מדביק* אחרים.

![](pics/seir.png)

(This variant is called the **SEIR Model**[^seir], where the "E" stands for <icon e></icon> "Exposed". Note this *isn't* the everyday meaning of "exposed", when you may or may not have the virus. In this technical definition, "Exposed" means you definitely have it. Science terminology is bad.)

הגרסה הזו של המודל מכונה **SEIR Model*** והאות "E" פירושה "Exposed" <icon e></icon>. (שימו לב שהמילה Exposed משמשת בשפה היום יומית לתאר מישהו שנחשף לנגיף אבל אולי לא נדבק. כאו הכוונה היא למישהו שנדבק בוודאות אבל עדיין לא מדבק)

[^seir]: For more technical explanations of the SEIR Model, see [the Institute for Disease Modeling](https://www.idmod.org/docs/hiv/model-seir.html) and [Wikipedia](https://en.wikipedia.org/wiki/Compartmental_models_in_epidemiology#The_SEIR_model)

For COVID-19, it's estimated that you're <icon e></icon> infected-but-not-yet-infectious for 3 days, *on average*.[^latent] What happens if we add that to the simulation?

ל COVID-19, ההערכה היא שאתה <icon e></icon> למשך 3 ימים, *בממוצע* נשא-אבל-לא-מדבק.
מה יקרה אם נוסיף את זה לסימולציה?


[^latent]: “Assuming an incubation period distribution of mean 5.2 days from a separate study of early COVID-19 cases, we inferred that infectiousness started from 2.3 days (95% CI, 0.8–3.0 days) before symptom onset” (translation: Assuming symptoms start at 5 days, infectiousness starts 2 days before = Infectiousness starts at 3 days) [He, X., Lau, E.H.Y., Wu, P. et al.](https://www.nature.com/articles/s41591-020-0869-5)

העקומות <b style='color:#ff4040'> האדומה <b style='color:#FF9393'>+ הוורודה</b> ביחד</b> הן כמות המקרים *הנוכחית* (מדבקים <icon i></icon> + נשאים <icon e></icon>),    
<b style='color:#888'>העקומה האפורה</b> היא *סך כל* המקרים (כמות מקרים נוכחית + מחלימים <icon r></icon>):

```{=html5}
<div class="sim">
		<iframe src="sim?stage=epi-5" width="800" height="540"></iframe>
</div>
```

Not much changes! How long you stay <icon e></icon> Exposed changes the ratio of <icon e></icon>-to-<icon i></icon>, and *when* current cases peak... but the *height* of that peak, and total cases in the end, stays the same.

לא הרבה השתנה. משך הזמן שבו אתה נשאר <icon e></icon> נשא משנה את היחס בין <icon e></icon>-ל-<icon i></icon>, ו*מתי* כמות המקרים תגיע לשיא, אבל אבל *הגובה* של השיא הזה, וכמות המקרים הכללית בסופו של דבר, לא משתנה.

Why's that? Because of the *first*-most important idea in Epidemiology 101:

למה? בגלל העיקרון *הראשון* של מבוא לאפידימיולוגיה:

![](pics/r.png)

Short for "Reproduction number". It's the *average* number of people an <icon i></icon> infects *before* they recover (or die).

שמסמל את ה "Reproduction number". המספר הממוצע של אנשים ש<icon i></icon> מדביק *לפני* שהוא מחלים (או נפטר).

![](pics/r2.png)

**R** changes over the course of an outbreak, as we get more immunity & interventions.

**R** הוא זה שמשנה את הכיוון של ההתפרצות כשאנחנו מפתחים יותר חסינות או מתערבים במצב בכל מני דרכים.

**R<sub>0</sub>** (pronounced R-nought) is what R is *at the start of an outbreak, before immunity or interventions*. R<sub>0</sub> more closely reflects the power of the virus itself, but it still changes from place to place. For example, R<sub>0</sub> is higher in dense cities than sparse rural areas.


**R<sub>0</sub>** הןא הערך של R *בתחילת ההתפרצות, לפני שאנשים התחילו לפתח עמידות ולפני שהתחלנו לנקוט באמצעים לריסון ההתפרצות*. R<sub>0</sub> משקף טוב יותר את העוצמה של הנגיף עצמו, ועדיין הוא עשוי להשתנות ממקום למקום. למשל, R<sub>0</sub> גבוה יותר ערים צפופות מאשר ביישובים חקלאיים.

(Most news articles – and even some research papers! – confuse R and R<sub>0</sub>. Again, science terminology is bad)

(רוב כתבות החדשות - ואפילו חלק מהמאמרים האקדמיים! - מבלבלים בין R ל R<sub>0</sub>)

The R<sub>0</sub> for "the" seasonal flu is around 1.28[^r0_flu]. This means, at the *start* of a flu outbreak, each <icon i></icon> infects 1.28 others *on average.* (If it sounds weird that this isn't a whole number, remember that the "average" mom has 2.4 children. This doesn't mean there's half-children running about.)

הערך של R<sub>0</sub> לשפעת העונתית הוא בערך 1.28[^r0_flu]. זה אומר, ש*בתחילת* התפרצות של שפעת, כל <icon i></icon> מדביק  1.28 אחרים *בממוצע*. (אם נשמע לכם מוזר שהמספר הזה הוא לא מספר שלם, לאמא הממוצעת יש 2.4 ילדים. זה לא אומר שמסתובבים ברחוב כל מני חצאי ילדים.)


[^r0_flu]: “The median R value for seasonal influenza was 1.28 (IQR: 1.19–1.37)” [Biggerstaff, M., Cauchemez, S., Reed, C. et al.](https://bmcinfectdis.biomedcentral.com/articles/10.1186/1471-2334-14-480)

The R<sub>0</sub> for COVID-19 is estimated to be around 2.2,[^r0_covid] though one *not-yet-finalized* study estimates it was 5.7(!) in Wuhan.[^r0_wuhan]

מעריכים ש R<sub>0</sub> ל COVID-19 הוא בערך 2.2,[^r0_covid] למרות שמחקר אחד *לא סופי* מעריך אותו ב !5.7(!) בווהאן.[^r0_wuhan]


[^r0_covid]: “We estimated the basic reproduction number R0 of 2019-nCoV to be around 2.2 (90% high density interval: 1.4–3.8)” [Riou J, Althaus CL.](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC7001239/)

[^r0_wuhan]: “we calculated a median R0 value of 5.7 (95% CI 3.8–8.9)” [Sanche S, Lin YT, Xu C, Romero-Severson E, Hengartner N, Ke R.](https://wwwnc.cdc.gov/eid/article/26/7/20-0282_article)

In our simulations – *at the start & on average* – an <icon i></icon> infects someone every 4 days, over 10 days. "4 days" goes into "10 days" two-and-a-half times. This means – *at the start & on average* – each <icon i></icon> infects 2.5 others. Therefore, R<sub>0</sub> = 2.5. (caveats:[^r0_caveats_sim])

בסימולציה שלנו - *בתחילת ההתפרצות, בממוצע* - <icon i></icon> מדביק מישהו כל 4 ימים, למשך 10 ימים. "4 ימים" נכנס לתוך "10 ימים" פעמיים וחצי. זה אומר ש - *בתחילת ההתפרצות, בממוצע* - כל <icon i></icon> ידביק 2.5 אחרים. לכן R<sub>0</sub> = 2.5. (הסתייגויות:[^r0_caveats_sim])


[^r0_caveats_sim]: This is pretending that you're equally infectious all throughout your "infectious period". Again, simplifications for educational purposes.

**Play with this R<sub>0</sub> calculator, to see how R<sub>0</sub> depends on recovery time & new-infection time:**

** שחקו עם מחשבון R<sub>0</sub> הזה כדי לראות איך R<sub>0</sub> מושפע מזמן ההחלמה והזמן להדבקות חדשות:**

```{=html5}
<div class="sim">
		<iframe src="sim?stage=epi-6a&format=calc" width="285" height="255"></iframe>
</div>
```

But remember, the fewer <icon s></icon>s there are, the *slower* <icon s></icon>s become <icon i></icon>s. The *current* reproduction number (R) depends not just on the *basic* reproduction number (R<sub>0</sub>), but *also* on how many people are no longer <icon s></icon> Susceptible. (For example, by recovering & getting natural immunity.)

אבל צריך לזכור, ככל שיש פחות <icon s></icon>, לוקח יותר זמן ל <icon s></icon> להפוך להיות <icon i></icon>. הערך של R תלוי *עכשיו* לא רק בערך *הבסיסי* שלו (R<sub>0</sub>) אלא *גם* בכמה אנשים כבר לא <icon s></icon> פגיעים (למשל, אנשים שהחלימו ופיתחו חסינות טבעית)

```{=html5}
<div class="sim">
		<iframe src="sim?stage=epi-6b&format=calc" width="285" height="390"></iframe>
</div>
```

When enough people have immunity, R < 1, and the virus is contained! This is called **herd immunity**. For flus, herd immunity is achieved *with a vaccine*. Trying to achieve "natural herd immunity" by letting folks get infected is a *terrible* idea. (But not for the reason you may think! We'll explain later.)


כשלמספיק אנשים יש חסינות, R < 1, והמגיפה נעצרת! המצב הזה נקרא **חסינות עדר**. במקרה של שפעת, חסינות עדר מושגת *באמצעות חיסון*. לנסות לתת לאנשים להידבק כדי להשיג "חסינות עדר טבעית" זה רעיון *איום ונורא*. (אבל אולי לא מהסיבות שאתם חושבים! תיכף נסביר.) 

Now, let's play the SEIR Model again, but showing R<sub>0</sub>, R over time, and the herd immunity threshold:

בואו נשחק שוב עם מודל SEIR, אבל הפעם נראה את R<sub>0</sub>, ערך R, והסף שממנו אנחנו משיגים חסינות עדר:

```{=html5}
<div class="sim">
		<iframe src="sim?stage=epi-7" width="800" height="540"></iframe>
</div>
```

**NOTE: Total cases *does not stop* at herd immunity, but overshoots it!** And it crosses the threshold *exactly* when current cases peak. (This happens no matter how you change the settings – try it for yourself!)

** שימו לב: המספר הכללי של המקרים *לא מפסיק לעלות* כשמגיעים לחסינות עדר. הוא ממשיך לטפס ** והוא חוצה את הסף של חסינות העדר בדיוק כשכמות המקרים מגיעה לשיא שלה. (ולא משנה איך תשנו את ההגדרות - נסו בעצמכם)

This is because when there are more non-<icon s></icon>s than the herd immunity threshold, you get R < 1. And when R < 1, new cases stop growing: a peak.

זה קורה בגלל שכשיש יותר אנשים שאינם <icon s></icon> מהכמות שדרושה לחסינות עדר, אנחנו מקבלים R < 1. וכש R < 1 כמות המקרים החדשים מפסיקה לגדול - וזה השיא.

**If there's only one lesson you take away from this guide, here it is** – it's an extremely complex diagram so please take time to fully absorb it:

** אם תצאו מהמאמר הזה אם דבר אחד - הנה הדבר הזה ** - זו דיאגרמה מסובכת במיוחד אז קחו כמה דקות להפנים אותה:

![](pics/r3.png)

**This means: we do NOT need to catch all transmissions, or even nearly all transmissions, to stop COVID-19!**

**זה אומר שאנחנו לא חייבים לעצור את כל ההדבקות, או אפילו קרוב לזה, כדי לעצור את המגיפה!**

It's a paradox. COVID-19 is extremely contagious, yet to contain it, we "only" need to stop more than 60% of infections. 60%?! If that was a school grade, that's a D-. But if R<sub>0</sub> = 2.5, cutting that by 61% gives us R = 0.975, which is R < 1, virus is contained! (exact formula:[^exact_formula])

זה מרגיש פרדוקסלי. COVID-19 היא מחלה מדבקת ביותר, אבל כדי לעצור אותה, אנחנו צריכים לעצור יותר מ 60% מההדבקות. 60% זה אולי לא ציון מרשים במיוחד בבית הספר אבל אם R<sub>0</sub> = 2.5, ונצליח להקטין אותו ב 61% נקבל R = 0.975, וזה פחות מ 1, המגיפה נעצרה! (הנוסחא המדוייקת:[^exact_formula])


[^exact_formula]: Remember R = R<sub>0</sub> * the ratio of transmissions still allowed. Remember also that ratio of transmissions allowed = 1 - ratio of transmissions *stopped*.
    
    Therefore, to get R < 1, you need to get R<sub>0</sub> * TransmissionsAllowed < 1. 
    
    Therefore, TransmissionsAllowed < 1/R<sub>0</sub>
    
    Therefore, 1 - TransmissionsStopped < 1/R<sub>0</sub>
    
    Therefore, TransmissionsStopped > 1 - 1/R<sub>0</sub>
    
    Therefore, you need to stop more than **1 - 1/R<sub>0</sub>** of transmissions to get R < 1 and contain the virus!

![](pics/r4.png)

(If you think R<sub>0</sub> or the other numbers in our simulations are too low/high, that's good you're challenging our assumptions! There'll be a "Sandbox Mode" at the end of this guide, where you can plug in your *own* numbers, and simulate what happens.)

(אם נראה לכם שהערך של R0 או מספר אחר בסימולציה הזו נמוך/גבוה מדי, זה מצויין! בסוף המאמר יש סימולטור בוא תוכלו להזין את המספרים *שלכם* ולראות מה יוצא)

*Every* COVID-19 intervention you've heard of – handwashing, social/physical distancing, lockdowns, self-isolation, contact tracing & quarantining, face masks, even "herd immunity" – they're *all* doing the same thing:

*כל* מה שאנחנו עושים כדי להתמודד עם המגיפה הזו - שטיפת ידיים, ריחוק חברתי, סגרים, בידוד, מעקב מגעים, מסיכות ואפילו "חסינות עדר" *כולם* מנסים להשיג אותה מטרה:

Getting R < 1.

להגיע ל R < 1.

So now, let's use our "epidemic flight simulator" to figure this out: How can we get R < 1 in a way **that also protects our mental health *and* financial health?**

עכשיו, בואו נשתמש בסימולטור שלנו כדי לבדוק איך אנחנו יכולים להגיע ל R < 1 בדרך ש**שומרת על הבריאות הנפשית והפיננסית שלנו**.

Brace yourselves for an emergency landing...

היכנו לנחיתת חירום...

```{=html5}
<div class="section chapter">
    <div>
		<img src="banners/curve.png" height=480 style="position: absolute;"/>
        <div>The Next Few Months</div>
	    <div>החודשים הקרובים</div>
    </div>
</div>
```

...could have been worse. Here's a parallel universe we avoided:

...יכלו להיות יותר גרועים. הנה כמה יקומים מקבילים שלא הגענו אליהם:

###Scenario 0: Do Absolutely Nothing

###תרחיש 0: לא לעשות שום דבר

Around 1 in 20 people infected with COVID-19 need to go to an ICU (Intensive Care Unit).[^icu_covid] In a rich country like the USA, there's 1 ICU bed per 3400 people.[^icu_us] Therefore, the USA can handle 20 out of 3400 people being *simultaneously* infected – or, 0.6% of the population.

בערך 1 מכל 20 נדבקים ב COVID-19 מגיע לטיפול נמרץ.[^icu_covid] במדינה עשירה כמו ארצות הברית, יש מיטת טיפול נמרץ אחת לכל 3,400 אנשים.[^icu_us] לכן בארצות הברית אפשר לטפל במצב שבו 20 מכל 3,400 אנשים נדבקים - או 0.6% מהאוכלוסיה. 

[^icu_covid]: ["Percentage of COVID-19 cases in the United States from February 12 to March 16, 2020 that required intensive care unit (ICU) admission, by age group"](https://www.statista.com/statistics/1105420/covid-icu-admission-rates-us-by-age-group/). Between 4.9% to 11.5% of *all* COVID-19 cases required ICU. Generously picking the lower range, that's 5% or 1 in 20. Note that this total is specific to the US's age structure, and will be higher in countries with older populations, lower in countries with younger populations.

[^icu_us]: “Number of ICU beds = 96,596”. From [the Society of Critical Care Medicine](https://sccm.org/Blog/March-2020/United-States-Resource-Availability-for-COVID-19) USA Population was 328,200,000 in 2019. 96,596 out of 328,200,000 = roughly 1 in 3400. 

Even if we *more than tripled* that capacity to 2%, here's what would've happened *if we did absolutely nothing:*

הנה מה שהיה קורה אם לא היינו עושים כלום, בהנחה שהיינו מגדילים את כמות המיטות ל 2% מהאוכלוסיה (יותר מפי 3):

```{=html5}
<div class="sim">
		<iframe src="sim?stage=int-1&format=lines" width="800" height="540"></iframe>
</div>
```

Not good.

לא טוב.

That's what [the March 16 Imperial College report](http://www.imperial.ac.uk/mrc-global-infectious-disease-analysis/covid-19/report-9-impact-of-npis-on-covid-19/) found: do nothing, and we run out of ICUs, with more than 80% of the population getting infected. 
(remember: total cases *overshoots* herd immunity)


זה מה שגילה [המחקר של אימפיריאל קולג' מה-16 למרץ](http://www.imperial.ac.uk/mrc-global-infectious-disease-analysis/covid-19/report-9-impact-of-npis-on-covid-19/) אם לא נעשה כלום יגמרו לנו המיטות במצב שבו 80% מהאוכלוסיה נדבקה.


Even if only 0.5% of infected die – a generous assumption when there's no more ICUs – in a large country like the US, with 300 million people, 0.5% of 80% of 300 million = still 1.2 million dead... *IF we did nothing.*

אפילו אם רק 0.5% מהנדבקים מתים - הנחה נדיבה במצב שבו נגמרו המיטות בטיפול נמרץ - במדינה כמו ארצות הברית, עם 300 מיליון אנשים, 0.5% מתוך 80% מתוך 300 מיליון = 1.2 מיליון מתים...

(Lots of news & social media reported "80% will be infected" *without* "IF WE DO NOTHING". Fear was channelled into clicks, not understanding. *Sigh.*)

(הרבה אתרי חדשות ופוסטים במדיה החברתית אומרים "80%" ידבקו *בלי* להוסיף את ההסתייגות: "אם לא נעשה כלום". הופכים פחד לקליקים.)

###Scenario 1: Flatten The Curve / Herd Immunity

###תרחיש 1: משטחים את העקומה/חסינות עדר

The "Flatten The Curve" plan was touted by every public health organization, while the United Kingdom's original "herd immunity" plan was universally booed. They were *the same plan.* The UK just communicated theirs poorly.[^yong]

התכנית "לשטח את  העקומה" והתכנית הברטית של "חסינות עדר" היו בעצם *אותה תכנית*. הבריטים פשוט לא הסבירו אותה בצורה מוצלחת.[^yong] 

[^yong]: “He says that the actual goal is the same as that of other countries: flatten the curve by staggering the onset of infections. As a consequence, the nation may achieve herd immunity; it’s a side effect, not an aim. [...] The government’s actual coronavirus action plan, available online, doesn’t mention herd immunity at all.”
    
    From a [The Atlantic article by Ed Yong](https://www.theatlantic.com/health/archive/2020/03/coronavirus-pandemic-herd-immunity-uk-boris-johnson/608065/)

Both plans, though, had a literally fatal flaw.

שתי התכניות הללו סובלות מפגם קטלני.

First, let's look at the two main ways to "flatten the curve": handwashing & physical distancing.

קודם כל, בואו נסתכל על שתי הדרכים המרכזיות "לשטח את העקומה": שטיפת ידיים וריחוק חברתי.

Increased handwashing cuts flus & colds in high-income countries by ~25%[^handwashing], while the city-wide lockdown in London cut close contacts by ~70%[^london]. So, let's assume handwashing can reduce R by *up to* 25%, and distancing can reduce R by *up to* 70%:

שטיפת ידיים מוגברת מורידה את התפשטות נגיפי השפעת בערך ב 25% במדינות מפותחות[^handwashing], וסגר בלונדון הוריד את כמות המגעים הקרובים בערך ב 70%. בואו נניח ששטיפת ידיים יכולה לצמצם את R ב*עד* 25%, וריחוק חברתי יכול לצמצם את R ב *עד* [^london]70%:

[^handwashing]: “All eight eligible studies reported that handwashing lowered risks of respiratory infection, with risk reductions ranging from 6% to 44% [pooled value 24% (95% CI 6–40%)].” We rounded up the pooled value to 25% in these simulations for simplicity. [Rabie, T. and Curtis, V.](https://onlinelibrary.wiley.com/doi/full/10.1111/j.1365-3156.2006.01568.x) Note: as this meta-analysis points out, the quality of studies for handwashing (at least in high-income countries) are awful.

[^london]: “We found a 73% reduction in the average daily number of contacts observed per participant. This would be sufficient to reduce R0 from a value from 2.6 before the lockdown to 0.62 (0.37 - 0.89) during the lockdown”. We rounded it down to 70% in these simulations for simplicity. [Jarvis and Zandvoort et al](https://cmmid.github.io/topics/covid19/comix-impact-of-physical-distance-measures-on-transmission-in-the-UK.html)

**Play with this calculator to see how % of non-<icon s></icon>, handwashing, and distancing reduce R:** (this calculator visualizes their *relative* effects, which is why increasing one *looks* like it decreases the effect of the others.[^log_caveat])

**שחקו עם המחשבון הזה כדי לראות איך אחוז שטיפת היידים אצל אנשים שאינם <icon s></icon>, וריחוק חברתי מצמצמים את R:** (החישוב הזה מציג את ההשפעה *היחסית* ולכן הגדלה של אחד הגורמים *נראית* כאילו היא מקטינה את האחרים.[^log_caveat])

[^log_caveat]: This distortion would go away if we plotted R on a logarithmic scale... but then we'd have to explain *logarithmic scales.*

```{=html5}
<div class="sim">
		<iframe src="sim?stage=int-2a&format=calc" width="285" height="260"></iframe>
</div>
```

Now, let's simulate what happens to a COVID-19 epidemic if, starting March 2020, we had increased handwashing but only *mild* physical distancing – so that R is lower, but still above 1:

בואו נבדוק מה היה קורה אם בתחילת מרץ 2020 היינו מגבירים את שטיפת הידיים אבל מפעילים רק ריחוק חברתי *קל* - כך ש R היה נמוך יותר אבל עדיין מעל 1:

```{=html5}
<div class="sim">
		<iframe src="sim?stage=int-2&format=lines" width="800" height="540"></iframe>
</div>
```

Three notes:

שלוש הערות:

1. This *reduces* total cases! **Even if you don't get R < 1, reducing R still saves lives, by reducing the 'overshoot' above herd immunity.** Lots of folks think "Flatten The Curve" spreads out cases without reducing the total. This is impossible in *any* Epidemiology 101 model. But because the news reported "80%+ will be infected" as inevitable, folks thought total cases will be the same no matter what. *Sigh.*

1. הגישה הזו מפחיתה את *סך הכל המקרים*! **אפילו אם לא הצלחנו להגיע ל R < 1, הקטנת R עדיין מצילה חיים על ידי הפחתת כמות האנשים שיחלו מעבר לנקודה של חסינות עדר.** הרבה אנשים חושבים שאם "נשטח את העקומה" נפזר את המקרים על יותר זמן אבל לא נקטין את סך הכל המקרים. זה לא יכול להיות *בשום* מודל אפידימיולוגי.

2. Due to the extra interventions, current cases peak *before* herd immunity is reached. In fact, in this simulation, total cases only overshoots *a tiny bit* above herd immunity – the UK's plan! At that point, R < 1, you can let go of all other interventions, and COVID-19 stays contained! Well, except for one problem...

2. בזכות הריחוק המצומצם ושטיפת הידיים, מספר המקרים מגיע לשיא *לפני* הגעה לחסינות עדר. למעשה, מספר המקרים הכולל עובר את המספר שדרוש לחסינות עדר רק במעט! זו התכנית הבריטית! בנקודה הזו R < 1, אפשר להסיר את כל ההגבלות וההתפרצות לא תחזור!, תכנית מצויינת! למעט בעיה קטנה אחת...

3. You still run out of ICUs. For several months. (and remember, we *already* tripled ICUs for these simulations)

3. אנחנו עדיין עוברים את כמות במיטות בטיפול נמרץ. למשך כמה חודשים. (זכרו שהכפלנו את כמות המיטות פי שלוש לייתר ביטחון)

That was the other finding of the March 16 Imperial College report, which convinced the UK to abandon its original plan. Any attempt at **mitigation** (reduce R, but R > 1) will fail. The only way out is **suppression** (reduce R so that R < 1).

זה היה עוד ממצא של המחקר של אימפיריאל קולג' מה 16 למרץ ששכנע את הבריטים לוותר על התכנית הזו. כל ניסיון "לשטח את העקומה" (להקטין את R אבל עדיין R > 1) ייכשל. הדרך היחידה היא "לשבור את העקומה". (להקטין את R כך ש R < 1)


![](pics/mitigation_vs_suppression.png)

That is, don't merely "flatten" the curve, *crush* the curve. For example, with a...

למשל...

###Scenario 2: Months-Long Lockdown

###תרחיש 2: סגר למשך כמה חודשים

Let's see what happens if we *crush* the curve with a 5-month lockdown, reduce <icon i></icon> to nearly nothing, then finally – *finally* – return to normal life:

בואו נראה מה קורה אם אנחנו "מרסקים" את העוקמה עם סגר של חמישה חודשים, מקטינים את <icon i></icon> כמעט לאפס ואז *סוף סוף* חוזרים לחיים נורמאליים:

```{=html5}
<div class="sim">
		<iframe src="sim?stage=int-3&format=lines" width="800" height="540"></iframe>
</div>
```

Oh.

אה...

This is the "second wave" everyone's talking about. As soon as we remove the lockdown, we get R > 1 again. So, a single leftover <icon i></icon> (or imported <icon i></icon>) can cause a spike in cases that's almost as bad as if we'd done Scenario 0: Absolutely Nothing.

זה "הגל השני" שכולם מדברים עליו. ברגע שאנחנו מסירים את הסגר, אנחנו מקבלים שוב R > 1. מספיק שישאר לנו <icon i></icon> אחד (או <icon i></icon> אחד שמגיע מחו"ל) כדי לגרום להתפרצות חמורה כמעט כמו תרחיש 0: לא עושים כלום.

**A lockdown isn't a cure, it's just a restart.**

**סגר לא יכול להיות תרופה לבעיה. מה שהוא עושה זה "מאפס" את המצב ומחזיר אותנו לנקודת ההתחלה.**

So, what, do we just lockdown again & again?

אז מה? סגר ועוד סגר ועד סגר עד אין סוף?

###Scenario 3: Intermittent Lockdown

###תרחיש 3: סגר לחלופין

This solution was first suggested by the March 16 Imperial College report, and later again by a Harvard paper.[^lockdown_harvard]

התרחיש הזה הוצע בנייר של האימפריאל קולג' מה 16 למרץ ושוב בנייר של הארוורד. [^lockdown_harvard]

[^lockdown_harvard]: “Absent other interventions, a key metric for the success of social distancing is whether critical care capacities are exceeded. To avoid this, prolonged or intermittent social distancing may be necessary into 2022.” [Kissler and Tedijanto et al](https://science.sciencemag.org/content/early/2020/04/14/science.abb5793)

**Here's a simulation:** (After playing the "recorded scenario", you can try simulating your *own* lockdown schedule, by changing the sliders *while* the simulation is running! Remember you can pause & continue the sim, and change the simulation speed)

**הנה הסימולציה:** (אחרי שהתרחיש המוקלט יסתיים, תוכלו לקבוע את הפרמטרים שלכם וגם לשחק עם הנתונים *תוך כדי* שהסימולציה פועלת! אפשר גם לעצור ולהמשיך את הסימולטור ולשנות את המהירות)

```{=html5}
<div class="sim">
		<iframe src="sim?stage=int-4&format=lines" width="800" height="540"></iframe>
</div>
```

This *would* keep cases below ICU capacity! And it's *much* better than an 18-month lockdown until a vaccine is available. We just need to... shut down for a few months, open up for a few months, and repeat until a vaccine is available. (And if there's no vaccine, repeat until herd immunity is reached... in 2022.)

הצלחנו לשמור את כמות המקרים החמורים *מתחת* לקיבולת של הטיפול הנמרץ! וזה הרבה יותר טוב מסגר של 18 חודשים עד שיהיה חיסון זמין. אנחנו צריכים רק... להטיל סגר לכמה חודשים, לפתוח לכמה חודשים, ולחזור על זה עד שיהיה חיסון זמין. (ואם לא יהיה חיסון זמין, עד שנגיע לחסינות עדר... ב 2022)

Look, it's nice to draw a line saying "ICU capacity", but there's lots of important things we *can't* simulate here. Like:

כמה שנחמד לנו למתוח קווים של "קיבולת טיפול נמרץ" יש עדיין כמה דברים שהסימולטור שלנו לא תופס. למשל:

**Mental Health:** Loneliness is one of the biggest risk factors for depression, anxiety, and suicide. And it's as associated with an early death as smoking 15 cigarettes a day.[^loneliness]

**בריאות נפשית:** בדידות היא אחד מגורמי הסיכון לדיכאון, חרדה והתאבדויות, והיא קשורה למוות מוקדם כמו עישון של 15 סיגריות ליום.[^loneliness] 

[^loneliness]: See [Figure 6 from Holt-Lunstad & Smith 2010](https://journals.sagepub.com/doi/abs/10.1177/1745691614568352). Of course, big disclaimer that they found a *correlation*. But unless you want to try randomly assigning people to be lonely for life, observational evidence is all you're gonna get.

**Financial Health:** "What about the economy" sounds like you care more about dollars than lives, but "the economy" isn't just stocks: it's people's ability to provide food & shelter for their loved ones, to invest in their kids' futures, and enjoy arts, foods, videogames – the stuff that makes life worth living. And besides, poverty *itself* has horrible impacts on mental and physical health.

**איתנות כלכלית:** "מה עם הכלכלה" נשמע כאילו אכפת לך יותר מכמה גרושים מאשר מחיי אדם, אבל "הכלכלה" היא לא רק משחקים במניות: היא היכולת של אנשים לספק אוכל וקורת גג למשפחה שלהם, להשקיע בעתיד של הילדים שלהם, להינות מאומנות, אוכל ומשחקי מחשב - הדברים שמרכיבים את מה שאנחנו קוראים לו החיים שלנו. חוץ מזה, גם לעוני בעצמו יש השפעה נוראית על בריאות פיזית ונפשית.

Not saying we *shouldn't* lock down again! We'll look at "circuit breaker" lockdowns later. Still, it's not ideal.

זה לא אומר שלא נצטרך לעשות סגר שוב! נראה איך אפשר להשתמש בסגר בהמשך, אבל זה לא אידיאלי.

But wait... haven't Taiwan and South Korea *already* contained COVID-19? For 4 whole months, *without* long-term lockdowns?

רגע... אבל טיוואן ודרום קוריאה הצליחו לעצור את התפשטות המגפה כבר 4 חודשים בלי סגר ארוך?

How?

איך?

###Scenario 4: Test, Trace, Isolate

###תרחיש 4: בדיקות, מעקב מגעים, בידודים

*"Sure, we \*could've\* done what Taiwan & South Korea did at the start, but it's too late now. We missed the start."*

*"יכולנו אולי לעשות מה שהם עשו מההתחלה אבל עכשיו מאוחר מדי. פספסנו את ההתחלה."*

But that's exactly it! “A lockdown isn't a cure, it's just a restart”... **and a fresh start is what we need.**

אבל זה בדיוק העניין. "סגר לא פותר את הבעיה - הוא מחזיר אותנו לנקודת ההתחלה"... **וזה בדיוק מה שאנחנו צריכים - לחזור לנקודת ההתחלה!**

To understand how Taiwan & South Korea contained COVID-19, we need to understand the exact timeline of a typical COVID-19 infection[^timeline]:

כדי להבין איך טיוואן וקוריאה הדרומית עצרו את התפשטות המגיפה, אנחנו צריכים להבין את לוח הזמנים של חולה COVID-19 טיפוסי[^timeline]:


[^timeline]: **3 days on average to infectiousness:** “Assuming an incubation period distribution of mean 5.2 days from a separate study of early COVID-19 cases, we inferred that infectiousness started from 2.3 days (95% CI, 0.8–3.0 days) before symptom onset” (translation: Assuming symptoms start at 5 days, infectiousness starts 2 days before = Infectiousness starts at 3 days) [He, X., Lau, E.H.Y., Wu, P. et al.](https://www.nature.com/articles/s41591-020-0869-5)  
    
    **4 days on average to infecting someone else:** “The mean [serial] interval was 3.96 days (95% CI 3.53–4.39 days)” [Du Z, Xu X, Wu Y, Wang L, Cowling BJ, Ancel Meyers L](https://wwwnc.cdc.gov/eid/article/26/6/20-0357_article)
    
    **5 days on average to feeling symptoms:** “The median incubation period was estimated to be 5.1 days (95% CI, 4.5 to 5.8 days)” [Lauer SA, Grantz KH, Bi Q, et al](https://annals.org/AIM/FULLARTICLE/2762808/INCUBATION-PERIOD-CORONAVIRUS-DISEASE-2019-COVID-19-FROM-PUBLICLY-REPORTED)

![](pics/timeline1.png)

If cases only self-isolate when they know they're sick (that is, they feel symptoms), the virus can still spread:

אם אנשים נכנסים לבידוד כשהם יודעים שהם חולים (כלומר מרגישים סימפטומים), הוירוס יכול להמשיך להתפשט:

![](pics/timeline2.png)

And in fact, 44% of all transmissions are like this: *pre*-symptomatic! [^pre_symp]

למעשה, 44% מכל ההדבקות הן הדבקות כאלו - *פרה-סימפטומטיות*! [^pre_symp]

[^pre_symp]: “We estimated that 44% (95% confidence interval, 25–69%) of secondary cases were infected during the index cases’ presymptomatic stage” [He, X., Lau, E.H.Y., Wu, P. et al](https://www.nature.com/articles/s41591-020-0869-5)

But, if we find *and quarantine* a symptomatic case's recent close contacts... we stop the spread, by staying one step ahead!

אבל אם נמצא *ונבודד* את כל המגעים הקרובים של מי שפיתח סימפטומים... נהיה צעד אחד קדימה ונוכל לעצור את התפשטות המגפה.

![](pics/timeline3.png)

This is called **contact tracing**. It's an old idea, was used at an unprecedented scale to contain Ebola[^ebola], and now it's core part of how Taiwan & South Korea are containing COVID-19!

זה נקרא **מעקב מגעים**. זה רעיון שקיים כבר זמן ארוך, השתמשו בו כדי לעצור את התפרצות האבולה[^ebola], ועכשיו טיוואן וקוריאה הדרומית משתמשות בו כחלק ממלחמה שלהן במגיפה.

[^ebola]: “Contact tracing was a critical intervention in Liberia and represented one of the largest contact tracing efforts during an epidemic in history.” [Swanson KC, Altare C, Wesseh CS, et al.](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC6152989/)

(It also lets us use our limited tests more efficiently, to find pre-symptomatic <icon i></icon>s without needing to test almost everyone.)

(השיטה הזו מאפשרת לנו גם להשתמש בבדיקות שיש לנו בצורה יעילה יותר ולמצוא נשאים בלי סימפטומים <icon i></icon> בלי לבדוק את כל האוכלוסיה.)

Traditionally, contacts are found with in-person interviews, but those *alone* are too slow for COVID-19's ~48 hour window. That's why contact tracers need help, and be supported by – *NOT* replaced by – contact tracing apps.

בעבר, איתור מגעים נעשה באמצעות ראיונות עם חולים סימפטומטים אבל ראיונות כאלו איטיים מדי בשביל חלון ההדבקה של הקורונה (48 שעות) ולכן נדרשת עזרה של אפליקציות לאיתור מגעים.

(This idea didn't come from "techies": using an app to fight COVID-19 was first proposed by [a team of Oxford epidemiologists](https://science.sciencemag.org/content/early/2020/04/09/science.abb6936).)

(הרעיון של שימוש באפליקציות לאיתור מגעים לא בא מעולם ביטחון או ההיי טק הוא הוצע לראשונה על ידי [צוות של אפידימיולוגים מאוקספורד](https://science.sciencemag.org/content/early/2020/04/09/science.abb6936).)

Wait, apps that trace who you've been in contact with?... Does that mean giving up privacy, giving in to Big Brother?

רגע, רגע, אפליקציות שרושמות עם מי הייתי במגע?... זה אומר לוותר לגמרי על הפרטיות שלי?

Heck no! **[DP-3T](https://github.com/DP-3T/documents#decentralized-privacy-preserving-proximity-tracing)**, a team of epidemiologists & cryptographers (including one of us, Marcel Salathé) is *already* making a contact tracing app – with code available to the public – that reveals **no info about your identity, location, who your contacts are, or even *how many contacts* you've had.**

ממש לא! **[DP-3T](https://github.com/DP-3T/documents#decentralized-privacy-preserving-proximity-tracing)**, קבוצה של אפידימיולוגים ומומחי הצפנה (כולל אחד ממחברי המאמר הזה, Marchel Salathé) כבר עובדים על אפליקציה למעקב אחרי מגעים - שהקוד שלה פתוח לציבור - **שלא חושפת את הזהות והמיקום שלך, מי היו המגעים שלך ואפילו לא *כמה מגעים היו לך*.** 

Here's how it works:

ככה זה עובד:

![](pics/dp3t.png)

(& [here's the full comic](https://ncase.me/contact-tracing/))

(& [והנה הקומיקס המלא (באנגלית)](https://ncase.me/contact-tracing/))

Along with similar teams like TCN Protocol[^tcn] and MIT PACT[^pact], they've inspired Apple & Google to bake privacy-first contact tracing directly into Android/iOS.[^gapple] (Don't trust Google/Apple? Good! The beauty of this system is it doesn't *need* trust!) Soon, your local public health agency may ask you to download an app. If it's privacy-first with publicly-available code, please do!

הפרוייקט הזה, ופרוייקטים דומים כמו TCN Protocol[^tcn] ו MIT PACT[^pact], היוו השראה ל Google ו Apple להכניס איתור מגעים  מבוסס פרטיות לתוך Android/iOS.[^gapple] (לא סומכים על גוגל ואפל? מעולה! היופי של המערכת הזו הוא שלא צריך לסמוך על אף אחד!) בקרוב ראשויות הבריאות יבקשו מכם להוריד אפליקציה. אם הקוד פתוח וזמין והיא מבוססת על הרעיונות האלו, הורידו אותה!

[^tcn]: [Temporary Contact Numbers, a decentralized, privacy-first contact tracing protocol](https://github.com/TCNCoalition/TCN#tcn-protocol)

[^pact]: [PACT: Private Automated Contact Tracing](https://pact.mit.edu/)

[^gapple]: [Apple and Google partner on COVID-19 contact tracing technology ](https://www.apple.com/ca/newsroom/2020/04/apple-and-google-partner-on-covid-19-contact-tracing-technology/). Note they're not making the apps *themselves*, just creating the systems that will *support* those apps.

But what about folks without smartphones? Or infections through doorknobs? Or "true" asymptomatic cases? Contact tracing apps can't catch all transmissions... *and that's okay!* We don't need to catch *all* transmissions, just 60%+ to get R < 1.

אבל מה עם אנשים שאין להם טלפון חכם? או הדבקות דרך ידיות של דלתות וכפתורים של מעליות? או מקרים שלא יפתחו סימפטומים בכלל? אפליקציות לאיתור מגעים לא יכולות לתפוס את כל ההדבקות... *וזה בסדר גמור!* אנחנו לא צריכים לתפוס את *כל* ההדבקות, רק 60% כדי לקבל R < 1.

(Rant about the confusion about pre-symptomatic vs "true" asymptomatic. "True" asymptomatics are rare:[^rant])

[^rant]: Lots of news reports – and honestly, many research papers – did not distinguish between "cases who showed no symptoms when we tested them" (pre-symptomatic) and "cases who showed no symptoms *ever*" (true asymptomatic). The only way you could tell the difference is by following up with cases later.
   
    Which is what [this study](https://wwwnc.cdc.gov/eid/article/26/8/20-1274_article) did. (Disclaimer: "Early release articles are not considered as final versions.") In a call center in South Korea that had a COVID-19 outbreak, "only 4 (1.9%) remained asymptomatic within 14 days of quarantine, and none of their household contacts acquired secondary infections."
    
    So that means "true asymptomatics" are rare, and catching the disease from a true asymptomatic may be even rarer!

Isolating *symptomatic* cases would reduce R by up to 40%, and quarantining their *pre/a-symptomatic* contacts would reduce R by up to 50%[^oxford]:

בידוד חולים *עם סימפטומים* יכול להוריד את R ב עד 40%, ובידוד המגעים שלהם יכול להוריד את R ב עד 50%[^oxford]:

[^oxford]: From the same Oxford study that first recommended apps to fight COVID-19: [Luca Ferretti & Chris Wymant et al](https://science.sciencemag.org/content/early/2020/04/09/science.abb6936/tab-figures-data) See Figure 2. Assuming R<sub>0</sub> = 2.0, they found that:    
    
    * Symptomatics contribute R = 0.8 (40%)
    * Pre-symptomatics contribute R = 0.9 (45%)
    * Asymptomatics contribute R = 0.1 (5%, though their model has uncertainty and it could be much lower)
    * Environmental stuff like doorknobs contribute R = 0.2 (10%)

    And add up the pre- & a-symptomatic contacts (45% + 5%) and you get 50% of R!

```{=html5}
<div class="sim">
		<iframe src="sim?stage=int-4a&format=calc" width="285" height="340"></iframe>
</div>
```

Thus, even without 100% contact quarantining, we can get R < 1 *without a lockdown!* Much better for our mental & financial health. (As for the cost to folks who have to self-isolate/quarantine, *governments should support them* – pay for the tests, job protection, subsidized paid leave, etc. Still way cheaper than intermittent lockdown.)

לכן, אפילו אם לא נצליח לבודד 100% מהמגעים, אנחנו יכולים להגיע ל R < 1 *בלי סגר!* הרבה יותר טוב לבריאות הנפשית והכלכלית שלנו. (לגבי מי שצריך להיכנס לסגר/בידוד - הממשלות צריכות לתמוך בהם. ימי מחלה וכד' יעלו הרבה פחות מסגרים חוזרים)

We then keep R < 1 until we have a vaccine, which turns susceptible <icon s></icon>s into immune <icon r></icon>s. Herd immunity, the *right* way:

אנחנו שומרים על R < 1 עד שיש לנו חיסון שיכול להפוך <icon s></icon> אנשים חשופים ל <icon i></icon> אנשים חסינים. חיסון עדר בדרך *הנכונה*:

```{=html5}
<div class="sim">
		<iframe src="sim?stage=int-4b&format=calc" width="285" height="230"></iframe>
</div>
```

(Note: this calculator pretends the vaccines are 100% effective. Just remember that in reality, you'd have to compensate by vaccinating *more* than "herd immunity", to *actually* get herd immunity)

(שימו לב: המחשבון הזה מניח שחיסון יעיל ב 100%, בפועל נצטרך לחסן *יותר* אנשים כדי לקבל חסינות עדר.)

Okay, enough talk. Here's a simulation of:

1. A few-month lockdown, until we can...
2. Switch to "Test, Trace, Isolate" until we can...
3. Vaccinate enough people, which means...
4. We win.


OK, בואו נראה, הנה סימולציה של:

1. כמה חודשים של סגר, עד שנוכל...
2. לעבור למעקב ובידוד של מגעים, עד שנוכל...
3. לחסן מספיק אנשים ואז...
4. ניצחנו.

```{=html5}
<div class="sim">
		<iframe src="sim?stage=int-5&format=lines" width="800" height="540"></iframe>
</div>
```

So that's it! That's how we make an emergency landing on this plane.

זהו ככה אנחנו מנחיתים את הסימולטור שלנו.

That's how we beat COVID-19.

ככה ננצח את COVID-19.

...

But what if things *still* go wrong? Things have gone horribly wrong already. That's fear, and that's good! Fear gives us energy to create *backup plans*.

 אבל מה אם זה לא יעבוד כמו שאנחנו מקווים?

The pessimist invents the parachute.

###Scenario 4+: Masks For All, Summer, Circuit Breakers

###תרחיש 4+: נשף מסכות, קיץ, איפוסים

What if R<sub>0</sub> is way higher than we thought, and the above interventions, even with mild distancing, *still* aren't enough to get R < 1?

מה אם R<sub>0</sub> הרבה יותר גדול ממה שהערכנו, וכל הצעדים שתוארו עד עכשיו, כולל הרחקה חברתית, *עדיין* לא מספיקים כדי להגיע ל R < 1?

Remember, even if we can't get R < 1, reducing R still reduces the "overshoot" in total cases, thus saving lives. But still, R < 1 is the ideal, so here's a few other ways to reduce R:

שימו לב, בכל מקרה הקטנה של R מקטינה את כמות המקרים הכללית ולכן חוסכת חיי אדם. אבל R < 1 היא עדיין המטרה שלנו לכן הנה עוד כמה צעדים להקטנת R:

**Masks For All:**

**נשף מסכות:**

*"Wait,"* you might ask, *"I thought face masks don't stop you from getting sick?"*

*"רגע,"* אתם אומרים, *"חשבתי שמסכות לא מונעות ממך להדבק?"*

You're right. Masks don't stop you from getting sick[^incoming]... they stop you from getting *others* sick.

נכון. מסכות לא מונעות ממך להדבק[^incoming]... הן מונעות ממך להדביק אחרים.

[^incoming]: “None of these surgical masks exhibited adequate filter performance and facial fit characteristics to be considered respiratory protection devices.” [Tara Oberg & Lisa M. Brosseau](https://www.sciencedirect.com/science/article/pii/S0196655307007742)

[^outgoing]: “The overall 3.4 fold reduction [70% reduction] in aerosol copy numbers we observed combined with a nearly complete elimination of large droplet spray demonstrated by Johnson et al. suggests that surgical masks worn by infected persons could have a clinically significant impact on transmission.” [Milton DK, Fabian MP, Cowling BJ, Grantham ML, McDevitt JJ](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC3591312/)

[^homemade]: [Davies, A., Thompson, K., Giri, K., Kafatos, G., Walker, J., & Bennett, A](https://www.cambridge.org/core/journals/disaster-medicine-and-public-health-preparedness/article/testing-the-efficacy-of-homemade-masks-would-they-protect-in-an-influenza-pandemic/0921A05A69A9419C862FA2F35F819D55) See Table 1: a 100% cotton T-shirt has around 2/3 the filtration efficiency as a surgical mask, for the two bacterial aerosols they tested.

![](pics/masks.png)

To put a number on it: surgical masks *on the sick person* reduce cold & flu viruses in aerosols by 70%.[^outgoing] Reducing transmissions by 70% would be as large an impact as a lockdown!

או במספרים: מסיכה על *אדם חולה* מקטינה את נגיפי השפעת ברסס ב 70%.[^outgoing] הקטנה של 70% בהדבקה שקולה להשפעה של סגר!

However, we don't know for sure the impact of masks on COVID-19 *specifically*. In science, one should only publish a finding if you're 95% sure of it. (...should.[^replication]) Masks, as of May 1st 2020, are less than "95% sure".

על כל פנים, אנחנו עדיין לא יודעים מה ההשפעה הספציפית של מסכות על COVID-19. במחקרים מדעיים מקובל לפרסם תוצאות רק בביטחון של 95% (מקובל...) נכון ל1 במאי 2020 מסכות עדיין לא וודאיות ב 95%.

[^replication]: Any actual scientist who read that last sentence is probably laugh-crying right now. See: [p-hacking](https://en.wikipedia.org/wiki/Data_dredging), [the replication crisis](https://en.wikipedia.org/wiki/Replication_crisis))

However, pandemics are like poker. **Make bets only when you're 95% sure, and you'll lose everything at stake.** As a recent article on masks in the British Medical Journal notes,[^precautionary] we *have* to make cost/benefit analyses under uncertainty. Like so:

בכל מקרה, פנדמיות הן כמו משחק פוקר. **אם תהמר רק כשאתה בטוח ב 95% תפסיד בכל סיבוב.** כמו שמציין מאמר על מסכות ב British Medical Journal,[^precautionary] אנחנו *חייבים* לעשות ניתוחים של עלות/תועלת בתנאים של אי-וודאות. ולכן:

[^precautionary]: “It is time to apply the precautionary principle” [Trisha Greenhalgh et al \[PDF\]](https://www.bmj.com/content/bmj/369/bmj.m1435.full.pdf)

Cost: If homemade cloth masks (which are ~2/3 as effective as surgical masks[^homemade]), super cheap. If surgical masks, more expensive but still pretty cheap.

עלות: אם מסכות בד ביתיות (ביעילות של 2/3~ ממסכות מנתחים [^homemade]), זולות מאד. אם מסכות מנתחים יותר יקרות אבל עדיין זולות למדי.

Benefit: Even if it's a 50–50 chance of surgical masks reducing transmission by 0% or 70%, the average "expected value" is still 35%, same as a half-lockdown! So let's guess-timate that surgical masks reduce R by up to 35%, discounted for our uncertainty. (Again, you can challenge our assumptions by turning the sliders up/down)

תועלת: אפילו אם יש סיכוי של 50-50 שמסכות מקטינות את שיעור ההדבקה ב 0% או ב 70%, ממוצע התוחלת הוא עדיין 35%, כמו חצי סגר! אז בואו נניח שההשפעה היא 35% כפיצוי על אי הוודאות שלנו. (שוב, שחקו עם המספרים ובידקו את התסריט שלכם)

```{=html5}
<div class="sim">
		<iframe src="sim?stage=int-6a&format=calc" width="285" height="380"></iframe>
</div>
```

(other arguments for/against masks:[^mask_args])

(:[^mask_args]עוד טיעונים בעד ונגד מסכות)

[^mask_args]: **"We need to save supplies for hospitals."** *Absolutely agreed.* But that's more of an argument for increasing mask production, not rationing. In the meantime, we can make cloth masks.

   **"They're hard to wear correctly."** It's also hard to wash your hands according to the WHO Guidelines – seriously, "Step 3) right palm over left dorsum"?! – but we still recommend handwashing, because imperfect is still better than nothing.
   
   **"It'll make people more reckless with handwashing & social distancing."** Sure, and safety belts make people ignore stop signs, and flossing makes people eat rocks. But seriously, we'd argue the opposite: masks are a *constant physical reminder* to be careful – and in East Asia, masks are also a symbol of solidarity!
    
    

Masks *alone* won't get R < 1. But if handwashing & "Test, Trace, Isolate" only gets us to R = 1.10, having just 1/3 of people wear masks would tip that over to R < 1, virus contained!

מסכות *לבדן* לא יביאו אותנו ל R < 1.  אבל אם שטיפת ידים ובידוד מגעים יבאו אותנו ל R = 1.10, אפילו אם רק שליש מהאנשים יחבשו מסכות הם יעבירו אותנו מעבר ל R < 1, המגיפה נעצרה!

**Summer:**

**קיץ:**

Okay, this isn't an "intervention" we can control, but it will help! Some news outlets report that summer won't do anything to COVID-19. They're half right: summer won't get R < 1, but it *will* reduce R.

OK, קיץ זה לא משהו שאנחנו יכולים לעשות, אבל הקיץ יעזור! חלק מאתרי החדשות מדווחים שהקיץ לא יעשה כלום ל COVID-19. הם חצי צודקים: הקיץ לא יגרום ל R < 1 אבל הוא יוריד את R.

For COVID-19, every extra 1° Celsius (2.2° Fahrenheit) makes R drop by 1.2%.[^heat] The summer-winter difference in New York City is 15°C (60°F), so summer will make R drop by 18%.

עבור COVID-19, כל עליה של 1° מביאה לירידה של 1.2% ב R[^heat]. הפרש הטמפרטורות בין הקיץ לחורף בישראל הוא בערך 10° ולכן אנחנו יכולים לצפות לירידה של 12% ב R. 

[^heat]: “One-degree Celsius increase in temperature [...] lower[s] R by 0.0225” and “The average R-value of these 100 cities is 1.83”. 0.0225 ÷ 1.83 = ~1.2%. [Wang, Jingyuan and Tang, Ke and Feng, Kai and Lv, Weifeng](https://papers.ssrn.com/sol3/Papers.cfm?abstract_id=3551767)

```{=html5}
<div class="sim">
		<iframe src="sim?stage=int-6b&format=calc" width="285" height="220"></iframe>
</div>
```

Summer alone won't make R < 1, but if we have limited resources, we can scale back some interventions in the summer – so we can scale them *higher* in the winter.

הקיץ לבדו לא יביא ל R < 1 אבל אם יש לנו אמצעים מוגבלים, אנחנו יכולים לשחרר חלק מההגבלות בקיץ ולהחזיר אותן בחורף.

**A "Circuit Breaker" Lockdown:**
**איפוסים:*

And if all that *still* isn't enough to get R < 1... we can do another lockdown.

ואם כל זה *עדיין* לא מספיק, אנחנו יכולים לעשות עוד סגר.

But we wouldn't have to be 2-months-closed / 1-month-open over & over! Because R is reduced, we'd only need one or two more "circuit breaker" lockdowns before a vaccine is available. (Singapore had to do this recently, "despite" having controlled COVID-19 for 4 months. That's not failure: this *is* what success takes.)

אבל בגלל ש R כבר מוקטן בכל מני צורות אחרות לא נצטרך לעשות חודש חופשי וחודשיים סגר במעגל אין סופי. נצטרך אולי עוד סגר או שניים עד שיהיה חיסון זמין. (סינגפור נאלצה לעשות סגר שני לאחרונה אחרי 4 חודשים של שליטה במגיפה. זה לא כישלון: ככה נראית מלחמה *מוצלחת* בנגיף)

Here's a simulation a "lazy case" scenario:

הנה סימולציה של תרחיש מעורב כזה:

1. Lockdown, then
2. A moderate amount of hygiene & "Test, Trace, Isolate", with a mild amount of "Masks For All", then...
3. One more "circuit breaker" lockdown before a vaccine's found.

1. סגר, ואז
2. קצת הגיינה משופרת, עם קצת איתור מגעים, עם קצת מסכות ואז...
3. עוד סגר לאיפוס לפני שנמצא החיסון

```{=html5}
<div class="sim">
		<iframe src="sim?stage=int-7&format=lines&height=620" width="800" height="620"></iframe>
</div>
```

Not to mention all the *other* interventions we could do, to further push R down:

וזה בלי לדבר על שאר הדברים שאנחנו יכולים לעשות כדי להנמיך את R:

* Travel restrictions/quarantines
* Temperature checks at malls & schools
* Deep-cleaning public spaces
* [Replacing hand-shaking with foot-bumping](https://twitter.com/V_actually/status/1233785527788285953)
* And all else human ingenuity shall bring

* הגבלות נסיעה ובידוד למגיעים לארץ
* בדיקות טמפרטורה בקניונים ובתי ספר
* ניקיון יסודי של איזורים ציבוריים
* [לחיצת רגלים במקום לחיצת ידיים](https://twitter.com/V_actually/status/1233785527788285953)
* וכל שאר הפטנטים שעוד נמציא

. . .

We hope these plans give you hope. 

אנחנו מקווים שהתכנית הזו נותנת לכם תקווה.

**Even under a pessimistic scenario, it *is* possible to beat COVID-19, while protecting our mental and financial health.** Use the lockdown as a "reset button", keep R < 1 with case isolation + privacy-protecting contract tracing + at *least* cloth masks for all... and life can get back to a normal-ish!

**גם תחת ההנחות הפסימיות יותר, *אפשר* לנצח את המגפה הזו ולשמור על הבריאות הנפשית והכלכלית שלנו.** נשתנש בסגר כדי לאפס את המצב כשנצטרך, נשמור על R < 1 עם בידוד מקרים + מעקב מגעים ששומר על הפרטיות שלנו + מסכות לכולנו... והחיים יכולים לחזור ל(סוג של) מסלולם.

Sure, you may have dried-out hands. But you'll get to invite a date out to a comics bookstore! You'll get to go out with friends to watch the latest Hollywood cash-grab. You'll get to people-watch at a library, taking joy in people going about the simple business of *being alive.*

אז נסבול מידיים יבשות. אבל נוכל לצאת לבלות בין הירקות ברמי לוי, נוכל ללכת לקולנוע לראות את הלהיט התורן, נוכל להמשיך לחיות את החיים שלנו.

Even under the worst-case scenario... life perseveres.

גם בתרחישים הקשים יותר... החיים ממשיכים.

So now, let's plan for some *worse* worst-case scenarios. Water landing, get your life jacket, and please follow the lights to the emergency exits:

אז עכשיו, בואו נתכנן כמה תרחישים *עוד יותר גרועים*:

```{=html5}
<div class="section chapter">
    <div>
		<img src="banners/curve.png" height=480 style="position: absolute;"/>
        <div>The Next Few Years</div>
    </div>
</div>
```

You get COVID-19, and recover. Or you get the COVID-19 vaccine. Either way, you're now immune...

חטפתם COVID-19 והבראתם או שקיבלתם חיסון. ברכות! עכשיו אתם מחוסנים. 

...*לכמה זמן?*

* COVID-19 is most closely related to SARS, which gave its survivors 2 years of immunity.[^SARS immunity]
* The coronaviruses that cause "the" common cold give you 8 months of immunity.[^cold immunity]
* There's reports of folks recovering from COVID-19, then testing positive again, but it's unclear if these are false positives.[^unclear]
* One *not-yet-peer-reviewed* study on monkeys showed immunity to the COVID-19 coronavirus for at least 28 days.[^monkeys]

* ממה שאנחנו מכירים, COVID-19 הכי דומה ל SARA שמעניק שנתיים של חסינות למבריאים .[^SARS immunity]
* וירוסים ממשפחת הקורונה שגורמים לצינון מעניקים 8 חודשי חסינות.[^cold immunity]
* ישנם דיווחים על מחלימים מ COVID-19 שנבדקו ונמצאו חיוביים שוב. לא ברור אם המקרים הללו הם טעות בבדיקה (false positive)..[^unclear]
* מחקר אחד, שלא עבר עדיין ביקורת עמיתים, הראה שקופים חסינים לפחות 28 ימים אחרי החלמה.[^monkeys]

But for COVID-19 *in humans*, as of May 1st 2020, "how long" is the big unknown.

לגבי בני אדם, נכון ל 1 במאי 2020, "לכמה זמן" היא שאלה פתוחה.

[^SARS immunity]: “SARS-specific antibodies were maintained for an average of 2 years [...] Thus, SARS patients might be susceptible to reinfection ≥3 years after initial exposure.” [Wu LP, Wang NC, Chang YH, et al.](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC2851497/) "Sadly" we'll never know how long SARS immunity would have really lasted, since we eradicated it so quickly.

[^cold immunity]: “We found no significant difference between the probability of testing positive at least once and the probability of a recurrence for the beta-coronaviruses HKU1 and OC43 at 34 weeks after enrollment/first infection.” [Marta Galanti & Jeffrey Shaman (PDF)](http://www.columbia.edu/~jls106/galanti_shaman_ms_supp.pdf)

[^unclear]: “Once a person fights off a virus, viral particles tend to linger for some time. These cannot cause infections, but they can trigger a positive test.” [from STAT News by Andrew Joseph](https://www.statnews.com/2020/04/20/everything-we-know-about-coronavirus-immunity-and-antibodies-and-plenty-we-still-dont/)

[^monkeys]: From [Bao et al.](https://www.biorxiv.org/content/10.1101/2020.03.13.990226v1.abstract) *Disclaimer: This article is a preprint and has not been certified by peer review (yet).* Also, to emphasize: they only tested re-infection 28 days later. 

For these simulations, let's say it's 1 year.

לסימולציה הבאה נניח שאנחנו חסינים לשנה.

**Here's a simulation starting with 100% <icon r></icon>**, exponentially decaying into susceptible, no-immunity <icon s></icon>s after 1 year, on *average*, with variation:

**הנה סימולציה שמתחילה ב 100% <icon r></icon>**, דועכת אקספוננציאלית לאנשים חשופים ללא חסינות <icon s></icon> אחרי שנה:

```{=html5}
<div class="sim">
		<iframe src="sim?stage=yrs-1&format=lines&height=600" width="800" height="600"></iframe>
</div>
```

Return of the exponential decay!

שובה של הדעיכה האקספוננציאלית.

This is the **SEIRS Model**. The final "S" stands for <icon s></icon> Susceptible, again.

זה ה**SERIRS Model**. ה S שנוספה בסוף היא אנשים שחוזרים להיות פגיעים <icon s></icon> Susceptible. 

![](pics/seirs.png)

Now, let's simulate a COVID-19 outbreak, over 10 years, with no interventions... *if immunity only lasts a year:*

בואו נעשה סימולציה של התפרצות COVID-19 בלי שום התערבות... *בהנחה שהחסינות מחזיקה מעמד שנה אחת:*

```{=html5}
<div class="sim">
		<iframe src="sim?stage=yrs-2&format=lines&height=600" width="800" height="600"></iframe>
</div>
```

In previous simulations, we only had *one* ICU-overwhelming spike. Now, we have several, *and* <icon i></icon> cases come to a rest *permanently at* ICU capacity. (Which, remember, we *tripled* for these simulations)

בסימולציות הקודמות היה לנו רק שיא אחד שעבר את הקיבולת של מערכת בטיפול הנמרץ. עכשיו יש לנו כמה כאלו *ו* <icon i></icon> מתייצבים *באופן קבוע* על שיא הקיבולת של הטיפול הנמרץ. (שאותו הכפלנו פי שלוש כזכור)

R = 1, it's **endemic.**

R = 1, היא כאן להישאר

Thankfully, because summer reduces R, it'll make the situation better:

למרבה המזל, בגלל שהקיץ מפחית את R, המצב ישתפר:

```{=html5}
<div class="sim">
		<iframe src="sim?stage=yrs-3&format=lines&height=640" width="800" height="640"></iframe>
</div>
```

Oh.

אוי.

Counterintuitively, summer makes the spikes worse *and* regular! This is because summer reduces new <icon i></icon>s, but that in turn reduces new immune <icon r></icon>s. Which means immunity plummets in the summer, *creating* large regular spikes in the winter.

הקיץ מחריף את הקפיצות *וגם* גורם להן לחזור בקביעות! זה קורה בגלל שהקיץ מפחית את <icon i></icon> החדשים, אבל אז גורם גם לירידה בכמות המחוסנים החדשים <icon r></icon> ולכן החסינות יורדת בקיץ וגורמת לקפיצה קבועה בחורף.

Thankfully, the solution to this is pretty straightforward – just vaccinate people every fall/winter, like we do with flu shots:

למרבה המזל, הפיתרון לזה פשוט - לחסן בכל סתיו/חורף, כמו שאנחנו עושים עכשיו עם השפעת:

**(After playing the recording, try simulating your own vaccination campaigns! Remember you can pause/continue the sim at any time)**

**(אחרי שתפעילו את ההקלטה נסו לעשות סימולציה של קמפיין החיסונים שלכם! אפשר לעצור ולהמשיך את הסימולציה מתי שרוצים)**

```{=html5}
<div class="sim">
		<iframe src="sim?stage=yrs-4&format=lines" width="800" height="540"></iframe>
</div>
```

But here's the scarier question:

אבל הנה השאלה המפחידה יותר:

What if there's no vaccine for *years*? Or *ever?*

מה אם לא יהיה חיסון במשך *שנים*? או *לעולם*?

**To be clear: this is unlikely.** Most epidemiologists expect a vaccine in 1 to 2 years. Sure, there's never been a vaccine for any of the other coronaviruses before, but that's because SARS was eradicated quickly, and "the" common cold wasn't worth the investment. 

** רק להבהיר: זה לא תרחיש סביר.** מרבית האפידימיולוגים מצפים לחיסון בתוך שנה או שנתיים. נכון שלא נמצא עד היום חיסון לאף נגיף ממשפחת הקורונה אבל זה בגלל שמגפת ה SARS נעצרה מהר ונגיף ההצטננות לא היה שווה את ההשקעה.

Still, infectious disease researchers have expressed worries: What if we can't make enough?[^vax_enough] What if we rush it, and it's not safe?[^vax_safe]

ועדיין, מומחים הביעו דאגות: מה אם לא נצליח לייצר מספיק?[^vax_enough] מה אם נעשה את זה בחיפזון, והחיסון לא יהיה בטוח?[^vax_safe]

[^vax_enough]: “If a coronavirus vaccine arrives, can the world make enough?” [by Roxanne Khamsi, on Nature](https://www.nature.com/articles/d41586-020-01063-8)

[^vax_safe]: “Don’t rush to deploy COVID-19 vaccines and drugs without sufficient safety guarantees” [by Shibo Jiang, on Nature](https://www.nature.com/articles/d41586-020-00751-9)

Even in the nightmare "no-vaccine" scenario, we still have 3 ways out. From most to least terrible:

אפילו אם נמצא את עצמנו בסיוט של "אין-חיסון", עדיין יהיו לנו שלושה קרשי הצלה:

1) Do intermittent or loose R < 1 interventions, to reach "natural herd immunity". (Warning: this will result in many deaths & damaged lungs. *And* won't work if immunity doesn't last.)

1) נעשה סדרה של צעדים להקטנת R שלא יהיו קשים מדי עד שנגיע לחסינות עדר. (זה יגמר בהרבה מתים ונזק לריאות, ולא יעבוד אם יתברר שהחסינות עוברת מהר)

2) Do the R < 1 interventions forever. Contact tracing & wearing masks just becomes a new norm in the post-COVID-19 world, like how STI tests & wearing condoms became a new norm in the post-HIV world.


2) נמשיך לעשות צעדים להקטנת R לנצח. מסיכות ובידוד מגעים יהיו חלק מהחיים בעידן שאחרי COVID-19.

3) Do the R < 1 interventions until we develop treatments that make COVID-19 way, way less likely to need critical care. (Which we should be doing *anyway!*) Reducing ICU use by 10x is the same as increasing our ICU capacity by 10x:

3) נעשה צעדים להקטנת R עד שנצליח לפתח טיפול שיגרום ל COVID-19 להיות מחלה שלא גורמת לכל כך הרבה טיפול נמרץ. (את זה אנחנו צריכים לעשות בכל מקרה) הקטנת היקף האישפוזים פי 10 שקולה להגדלת כמות מיטת טיפול נמרץ פי 10.

**Here's a simulation of *no* lasting immunity, *no* vaccine, and not even any interventions – just slowly increasing capacity to survive the long-term spikes:**

**הנה סימולציה שמניחה *שאין* חסינות ארוכת טווח, *אין* חיסון, ואין אפילו צעדי מניעה. רק הגדלה הדרגתית של קיבולת טיפול נמרץ כדי להתמודד עם השיאים**

```{=html5}
<div class="sim">
		<iframe src="sim?stage=yrs-5&format=lines" width="800" height="540"></iframe>
</div>
```

Even under the *worst* worst-case scenario... life perseveres.

גם במקרה *הכי גרוע* הזה... החיים ממשיכים.

. . .

Maybe you'd like to challenge our assumptions, and try different R<sub>0</sub>'s or numbers. Or try simulating your *own* combination of intervention plans!

אולי תרצו לנסות הנחות אחרות או לבדוק את את הדרך שלכם לצאת מהמצב הזה.

**Here's an (optional) Sandbox Mode, with *everything* available. (scroll to see all controls) Simulate & play around to your heart's content:**

**הנה סימולציה שבה תוכלו לשחק ב*כל* המספרים!**

```{=html5}
<div class="sim">
		<iframe src="sim?stage=SB&format=sb" width="800" height="540"></iframe>
</div>
```

This basic "epidemic flight simulator" has taught us so much. It's let us answer questions about the past few months, next few months, and next few years.

הסימולטור הבסיסי הזה לימוד אותנו כמה דברים, וענה לנו על כמה שאלות לגבי החודשים האחרונים, החודשים הקרובים והשנים הבאות.

So finally, let's return to...

אז בואו נחזור ל...

```{=html5}
<div class="section chapter">
    <div>
		<img src="banners/curve.png" height=480 style="position: absolute;"/>
        <div>עכשיו</div>
    </div>
</div>
```

Plane's sunk. We've scrambled onto the life rafts. It's time to find dry land.[^dry_land]

המטוס שקע, אנחנו על הרפסודה המתנפחת. הגיע הזמן למצוא יבשה.[^dry_land]

[^dry_land]: Dry land metaphor [from Marc Lipsitch & Yonatan Grad, on STAT News](https://www.statnews.com/2020/04/01/navigating-covid-19-pandemic/)

Teams of epidemiologists and policymakers ([left](https://www.americanprogress.org/issues/healthcare/news/2020/04/03/482613/national-state-plan-end-coronavirus-crisis/), [right](https://www.aei.org/research-products/report/national-coronavirus-response-a-road-map-to-reopening/ ), and [multi-partisan](https://ethics.harvard.edu/covid-roadmap)) have come to a consensus on how to beat COVID-19, while protecting our lives *and* liberties.

צוותים של קובעי מדינות ואפידימיולוגים הגיעו להסכמה לגבי הדרך שבה נביס את COVID-19 תוך כדי שמירה על החיים שלנו ועל החרויות שלנו.

Here's the rough idea, with some (less-consensus) backup plans:

הנה התמצית:

![](pics/plan.png)

So what does this mean for YOU, right now?

אז מה כל זה אומר *לנו* עכשיו?

**For everyone:** Respect the lockdown so we can get out of Phase I asap. Keep washing those hands. Make your own masks. Download a *privacy-protecting* contact tracing app when those are available next month. Stay healthy, physically & mentally! And write your local policymaker to get off their butt and...

**לכולם:** לכבד את הסגר כדי שנוכל לצאת מהשלב הראשון במהירות. להמשיך לשטוף ידיים. לחבוש מסיכות. להוריד את האפליקציות לאיתור מגעים כשיהיו מוכנות. לשמור על הבריאות, נפשית וגופנית!

**For policymakers:** Make laws to support folks who have to self-isolate/quarantine. Hire more manual contact tracers, *supported* by privacy-protecting contact tracing apps. Direct more funds into the stuff we should be building, like...

**לקובעי מדיניות:** דאגו לתמיכה באנשים שנאלצים להתבודד. דאגו למעקב אחרי מגעים, באמצעות אפליקציות רלוונטיות. עודדו השקעה בדברים שצריך לפתח כמו...

**For builders:** Build tests. Build ventilators. Build personal protective equipment for hospitals. Build tests. Build masks. Build apps. Build antivirals, prophylactics, and other treatments that aren't vaccines. Build vaccines. Build tests. Build tests. Build tests. Build hope. 

**לאנשים שבונים דברים:** אנחנו צריכים בדיקות, מכשירי הנשמה, ציוד מיגון אישי לבתי החולים, חיסונים, אפליקציות בידוד, טיפולים שאינם חיסונים, עוד בדיקות ועוד בדיקות ותקווה.

Don't downplay fear to build up hope. Our fear should *team up* with our hope, like the inventors of airplanes & parachutes. Preparing for horrible futures is how we *create* a hopeful future.

The only thing to fear is the idea that the only thing to fear is fear itself.

לא לפחד כלל זה קצת הרבה, עדיף אולי לפחד קצת ולחצות את הגשר הצר באופטימיות.

```{=html5}
</fold>
```