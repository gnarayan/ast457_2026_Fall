# Prerequisite self-check: ASTR 457, week 1

Ten short items covering the math and Python this course assumes. **Self-scored,
never collected, zero stakes.** Do it before Thursday's class. If an item feels
shaky, use the refresher next to it. That's the whole point. If more than
three or four feel shaky, come talk to me in week 1 (not week 5): we will make
a plan, and it will be fine.

Answers are hidden under each item. Click to expand.

---

**1.** Star A is 5 magnitudes fainter than star B. What is the ratio of their
fluxes? *(Refresher: `help/astro_conventions.md`, magnitudes section.)*

<details><summary>Answer</summary>

F_B/F_A = 100. Five magnitudes is exactly a factor of 100 by definition
(each magnitude is a factor of 100^(1/5) ≈ 2.512).
</details>

**2.** Given m = −2.5 log₁₀(F/F₀), solve for F. *(Refresher: any algebra
review; `help/astro_conventions.md`.)*

<details><summary>Answer</summary>

F = F₀ · 10^(−m/2.5). If exponent/log manipulation felt slow, practice it.
It appears weekly.
</details>

**3.** For independent events A and B, what is P(A and B)? And in general,
when is P(A|B) = P(A)? *(Refresher: Ivezić et al. (ICVG) Ch. 3.1, or any
intro-probability source.)*

<details><summary>Answer</summary>

P(A∩B) = P(A)P(B) for independent events; P(A|B) = P(A) exactly when A and B
are independent. If "P(A|B) vs P(B|A)" feels blurry, flag it. Confusing the
two is one of the most common statistical errors in the published literature,
and we will weaponize it on a quiz.
</details>

**4.** You average N independent measurements, each with variance σ².
What is the variance of the mean? *(Refresher: ICVG Ch. 3, or Sivia &
Skilling Ch. 1.)*

<details><summary>Answer</summary>

σ²/N, so the error on the mean is σ/√N. This single fact underlies half of
observational astronomy.
</details>

**5.** For independent x and y: what is the uncertainty of s = x + y? And the
*fractional* uncertainty of p = x·y? *(Refresher: any error-propagation
primer; Sivia & Skilling.)*

<details><summary>Answer</summary>

σ_s = √(σ_x² + σ_y²). Add in quadrature. For products, fractional
uncertainties add in quadrature: (σ_p/p)² = (σ_x/x)² + (σ_y/y)².
</details>

**6.** Which of these can appear inside an exponential or a logarithm:
a flux in Jy, a time in days, or a ratio t/τ where τ is a timescale in days?
Why? *(Refresher: dimensional analysis, any physics text.)*

<details><summary>Answer</summary>

Only the ratio. Arguments of exp/log/sin must be dimensionless. Checking
this is a thirty-second way to catch broken formulas (yours or an AI's).
</details>

**7.** In numpy, what do `x[x > 3]` and `x[::2]` each return?
*(Refresher: `help/python3.pdf`; Thursday's in-class exercises drill this.)*

<details><summary>Answer</summary>

`x[x > 3]`: a new array holding only the elements greater than 3 (boolean
masking). `x[::2]`: every second element (slicing with a stride). You will
use boolean masks in every single lab.
</details>

**8.** An array of shape (10, 1) is multiplied by an array of shape (5,).
What is the result's shape? *(Refresher: numpy broadcasting docs;
`help/python_for_data_science.pdf`.)*

<details><summary>Answer</summary>

(10, 5). Broadcasting stretches the size-1 axis against the length-5 axis.
If this surprised you, skim the broadcasting rules once; it will save you
hours of shape-error debugging.
</details>

**9.** A CSV has a header line `t_days,rv_kms,sigma_rv_kms`. Write one line
of Python that loads it and one that pulls out the `rv_kms` column.
*(Refresher: Thursday's `matplotlib_demo.ipynb` does exactly this.)*

<details><summary>Answer</summary>

`d = np.genfromtxt('file.csv', delimiter=',', names=True)` then
`rv = d['rv_kms']`. (pandas `read_csv` is equally fine.)
</details>

**10.** You measured 30 data points, each with a known uncertainty. Should you
show them with `plt.scatter` or `plt.errorbar`, and what must every plot axis
carry? *(Refresher: Thursday's class; `help/python_for_data_science.pdf`.)*

<details><summary>Answer</summary>

`plt.errorbar`. Measured data without visible uncertainties is hiding
information (day one's demo turned on exactly this). Every axis carries a
label *with units*. This is graded style in every lab.
</details>

---

**Scoring yourself:** 8–10 comfortable → you're set. 5–7 → do the refreshers
this week; the course assumes these by Lab 02. Fewer → email me or come to
office hours *this week*; the earlier we know, the easier it is to fix.
