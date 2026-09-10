# ASTR 457: Foundations of Data Science in Astronomy

**Fall 2026 — University of Illinois Urbana-Champaign**

This page is the accessible (screen-reader-friendly) version of the syllabus.
It has the same content as [457_FDS_Syllabus.pdf](457_FDS_Syllabus.pdf); the version on GitHub is authoritative; this page and the PDF are updated together.

| | |
|---|---|
| Instructor | Prof. Gautham Narayan |
| Email | [gsn@illinois.edu](mailto:gsn@illinois.edu) |
| Phone | +1 (217) 300-7322 |
| Lecture | Astronomy 134, Tue & Thur, 12:30–13:50 |
| Office hours | Astronomy 129, by appointment |
| Course repo | <https://github.com/gnarayan/ast457_2026_Fall> |
| TA | Abha Vishwakarma (office hours Wed. 11:00–noon or by appointment, over Zoom; remote Sep. 12–20) |

## Course description and learning goals

This 16 week course (3 contact hours) will cover a number of statistical
techniques that are relevant to astrophysical studies. These include robust
statistics, regression, model building and hypotheses testing, MCMC methods,
parameter estimation, time series analysis, clustering and dimensionality
reduction, hierarchical modeling, and modern machine learning, including
neural networks, foundation models, and the large language models you are
already using. We will also cover best practices for writing code and version
control. These techniques are ubiquitous in science and industry. My goal is to
provide a survey of these techniques, together with realistic problems, so that
you see how they work and what their implicit assumptions are.

This course is built for the agentic AI era. AI
assistants can now produce a complete, plausible-looking analysis of most
well-specified problems in seconds. AI has inverted which skills matter. The scarce skill is no longer
producing a fit; it is knowing whether the fit is *right*: whether the
assumptions hold, whether the uncertainties are calibrated, and whether the
conclusions survive scrutiny. Accordingly, you will use AI tools openly and
document how you used them, and you will be graded on the judgment,
verification, and understanding that you yourself bring to the problem.

By the end of this semester you should be able to:

- Apply a variety of existing models in astronomy, and interpret the results
  and compare to existing literature.
- Identify when existing models are inadequate descriptions of the astrophysical
  circumstances under study, and develop new models using your knowledge of
  statistical and computational techniques.
- Report inferences from your models with appropriate uncertainties,
  visualizations that convey the robustness of the model you selected, and
  describe what you did in a manner appropriate for high-impact scientific
  journals.
- Critically evaluate an analysis produced by someone else (a collaborator, a
  published paper, or an AI system), identify its errors and unstated
  assumptions, and verify or refute its conclusions with quantitative
  evidence.

To achieve these outcomes, students enrolled for 3 credit hours are expected
to work 6 hours/week outside instruction time.

## Prerequisites

**Required:** ASTR 210 & 310, to provide the necessary background in modern
astronomy and Python programming. These have additional calculus & physics
prerequisites.

**Recommended:** Prior coursework in undergraduate statistics and
undergraduate linear algebra (e.g., MATH 227 or 257). You will also need a
computer with a working `conda` and `git` installation for much of the
coursework.

## Texts and readings

- ["Statistics, Data Mining, and Machine Learning in Astronomy"](https://press.princeton.edu/books/hardcover/9780691198309/statistics-data-mining-and-machine-learning-in-astronomy),
  Ž. Ivezić, A. Connolly, J. T. VanderPlas & A. Gray (Princeton University
  Press, ISBN 9780691198309) (**ICVG**)
- ["Python Data Science Handbook"](https://jakevdp.github.io/PythonDataScienceHandbook/),
  J. T. VanderPlas (O'Reilly Media) (**VdP**)

Copies of both books are available online (the previous edition for ICVG).
ICVG: through [O'Reilly](https://learning.oreilly.com/library/view/statistics-data-mining/9780691151687/)
(free registration with your illinois.edu email required) or through
[JSTOR](https://www.jstor.org/stable/j.ctt4cgbdj). VdP: on
[GitHub](https://jakevdp.github.io/PythonDataScienceHandbook/).

**Other resources:** "Modern Statistical Methods for Astronomy", E. Feigelson
with J. Babu (**FB**) is detailed, though focuses on using R, and is available
for free as an e-book through NASA ADS. You may also find "Bayesian Models for
Astrophysical Data", J. M. Hilbe, R. S. de Souza, & E. E. O. Ishida helpful
(1st edition, Cambridge University Press, ISBN 9781107133082). I recommend
"Data Analysis: A Bayesian Tutorial", D. S. Sivia and J. Skilling (2nd
edition, Oxford University Press) if you need a quick refresher on
prerequisite material, including the linear algebra we will lean on for
Gaussian processes and dimensionality reduction.

## Working with AI: the ground rules

Using AI assistants (Copilot, Claude, ChatGPT, Gemini, or whatever ships next
month) is **allowed and expected** on all labs and take-home exams. Professional research in 2026 involves these tools, and "realistic
research conditions," the founding ethos of this course, now includes them.
The University provides every student free access to Microsoft Copilot, so
every assignment is designed to be completable with free-tier tools; no one
needs to pay for a subscription to do well in this course.

The rules:

- **Document it.** Every lab and exam submission includes a short AI-use
  appendix: which tools you used, what you asked them for, what they got
  wrong, and how you found out. "I did not use AI for this assignment" is a
  perfectly acceptable appendix, if it's true.
- **You are the author.** You are graded on verification and judgment:
  checking the assumptions and catching the errors. Turning in unverified AI output is turning in
  someone else's work with your name on it. As you'll discover in this course,
  unverified AI output is frequently, confidently wrong.
- **You must be able to defend it.** Any submission can be selected for a
  short oral defense: you and your notebook, a few minutes of questions about why you made the choices you made. If you cannot explain your own submission, it isn't
  your submission, and it will be graded accordingly.
- **The line.** Discussing problems with classmates: encouraged. Using AI and
  documenting it: encouraged. Sharing solutions with each other: cheating.
  Misrepresenting AI work as verified, or fabricating your AI-use appendix:
  cheating, of the referral-to-the-Senate-Committee variety.

## Grading

Your grade combines two tracks. **Track A** (quizzes, oral components) is done
live and AI-free, and certifies the statistical reasoning you carry in your
own head. **Track B** (labs, take-home exam components, the capstone) is
open-book, open-AI, and documented, and certifies that you can do, and stand
behind, a real analysis. You need both to do well; neither can be delegated to
a machine. Attendance is at your own discretion. Extra credit is rare; the
one planned opportunity is the Sep. 8 Astronomy Colloquium (see Important
dates). This course awards 3 credit hours; graduate students may register for either
3 or 4 credit hours. At 3 credit hours, graduate students complete exactly the
same assessments as undergraduates; the 4 credit hour option adds an expanded
capstone (see below). **All
coursework uses Github, not a LM like Canvas, to replicate realistic research
conditions.** Periodic overall grade updates are sent via email. You are
welcome to discuss your grades and your work in the course with me during
office hours.

| Component | Weight |
|---|---|
| Labs (roughly weekly, AI-in-the-loop, documented) | 25% |
| In-class quizzes (short, written, AI-free) | 15% |
| Midterm (take-home 12% + oral defense 8%) | 20% |
| Final (take-home 12% + oral defense 8%) | 20% |
| Capstone (notebook, video & lightning talk) | 20% |

**Labs** (roughly ten, equally weighted). Each lab hands you a dataset generated specifically for you: your data, your
noise, your truth. Your grade depends on recovering parameters you cannot look
up and on whether your reported uncertainties actually cover the truth at the
rate they claim. Several labs include a supplied AI-generated analysis that is
subtly (or not so subtly) wrong; your job is the referee report: find the
flaws, demonstrate them quantitatively, and fix them. You may drop ONE lab
from your total, for whatever reason, no questions asked (and if you don't
elect to, I'll drop your lowest). Your lowest quiz is likewise dropped.

**The capstone** is a semester project applying a technique from this course
(or beyond it) to a real astronomical dataset. You deliver three things: a
worked Jupyter notebook; a recorded 10-minute presentation uploaded to YouTube
(an unlisted link is fine; turn captions on) and submitted with your notebook
by Noon on Mon Dec 7; and a 4-minute in-class lightning talk in the final week
(ten talks per session, Dec 3 and Dec 8). The video carries the depth; the
lightning talk is your elevator pitch, and questions on your capstone are fair
game at your final defense. Topics are chosen with me by mid-October. Graduate students taking the 4 credit hour
option additionally deliver a written survey of how their technique is used in
the current astrophysics and statistics literature, record a 15-minute video
(rather than 10) covering that survey, and are graded to a correspondingly
higher standard; this expanded capstone is the additional work that earns the
fourth credit hour.

This course (like every other one at UIUC...) uses a plus (+) and minus (−)
grading scale for course grades.
Grades are rounded up (i.e. `ceil()`) to the nearest integer.
97-100=A+; 93-96=A; 90-92=A-; 87-89=B+; 83-86=B; 80-82=B-; 77-79=C+; 73-76=C;
70-72=C-; 67-69=D+; 63-66=D; 60-62=D-; 0-59=F

## Course policies

I've outlined standards for this course below. Times listed in this syllabus
are US/Central throughout. If something is not covered by my policies, please
discuss it with me. My contact information is at the beginning of this
syllabus.

### Assignment and exam policies

Labs and the take-home components of the midterm and final are open book, open
AI (documented, per the ground rules above). You may work in groups, and may
discuss the assignments and ways to tackle them, but you must write/code your
solution independently and run your analysis on your own dataset. Your data
are unique to you, so your numbers and plots will not match anyone else's. If they do, we will be having a very short conversation.

Labs/exams will be posted to the course
[GitHub repo](https://github.com/gnarayan/ast457_2026_Fall) on Thursdays. Make
a fork of the repo, create a folder named for your NetID inside `submissions/`
for your work, write/code
up your solution as directed in the assignment, commit, and open a pull
request when you are satisfied with your work before Noon the following
Wednesday.

Quizzes (roughly six, equally weighted) are brief written checks (10–15 minutes) at the start of class, closed-everything, roughly every other week, covering the reasoning behind what we've done: reading a corner plot, or saying why an estimator misbehaves. No computation, no AI, no notes: these certify what you carry in your own head.

Oral defenses are short (5–10 minute) scheduled conversations with me or the
TA about work you submitted. Everyone defends their midterm, final, and capstone; lab defenses rotate so each of you does at least two during the semester. The questions are about your
choices and your checks. They are a rehearsal for every seminar, group meeting, and thesis defense you will ever attend.

The midterm and final take-home components will be posted online, and will be
due by Noon six days later, with defenses in the following week (for the
final, during finals week, Dec 15–17). If you have a
conflict with the exam dates, please contact me as soon as possible. Make up
examinations will have different questions. Exams include all material covered
prior, and will require a more substantial time commitment than the weekly
labs. While I am open to accommodating students who need to take these exams at different times for any reason, all grades for the course are due to
the Registrar by Dec. 22, 2026, and I cannot provide extensions beyond that
date, unless there are absolutely extenuating circumstances.

### Grades of Incomplete

Incomplete (I) grades follow College of LAS policies and procedures: the
authority to authorize an incomplete rests with the college, not with me.
Incompletes are appropriate only where unexpected emergencies prevent you from
completing the course and the remaining work can be completed the next
semester, and documentation must be provided.
Incomplete work must be finished by the 10th day of instruction in the Spring
2027 semester, else the "I" will automatically be recorded as a "F" on your
transcript.

### Late or missed assignments

Labs are assigned on Thursday and due the following Wednesday by Noon. If you
know that you will be turning an assignment in late please notify me in
advance. A full letter grade will be deducted for each day an assignment is
late until a "F" grade is achieved, unless you have a documented medical
excuse or you have notified me of other extenuating circumstances. Remember
that you may drop ONE lab and one quiz from your total, for whatever reason,
no questions asked. Missed quizzes cannot be made up (that's what the drop is
for); missed oral defenses can be rescheduled once with advance notice. Per
the university's [Student Code](https://studentcode.illinois.edu/), I will
reasonably accommodate class absences; if I ask for an absence letter, you can
obtain one from the Connie Frank CARE Center.

### Accessibility accommodation

It is my goal that this class be an accessible and welcoming experience for
all students, including those with disabilities that may impact learning in
this class. If the design of this course poses barriers to you effectively
participating and/or demonstrating learning in this course, please meet with
me, with or without an Accessibility Services accommodation letter, to discuss
reasonable options or adjustments. You are welcome to talk to me at any point
in the semester about course design concerns, but it is always best if we can
talk at least one week prior to the need for any modifications.

During our discussion, I may suggest the possibility/necessity of your
contacting the Office of Disability Resources and Educational Services (1207
S. Oak St., Champaign, IL 61820; 217-333-1970;
[disability@illinois.edu](mailto:disability@illinois.edu);
<http://disability.illinois.edu/>) to talk about academic accommodations.

### Academic integrity

Plagiarism: **Don't.** Copying a classmate's solution is cheating. Using AI is allowed; lying about it is not.
Fabricating your AI-use appendix, presenting unverified machine output as your
own verified analysis, or having someone (or something) else sit your quiz or
defense are all academic integrity violations, and will result at least in an
"F" for that work, possibly an "F" for the course, and referral to the Senate
Committee for Student Discipline. Read the University of Illinois' policy on
[plagiarism](https://studentcode.illinois.edu/article1/part4/1-402/).

I am confident in each of your ability to tackle the course work. The
assessment in this course is designed so that honest work is also the path of
least resistance: your dataset is yours alone, and documented AI use costs you nothing. If
you feel you need help with material, come see me during office hours.

### Classroom behavior

I expect you to live up to your roles as student-scholars. Students must
follow the University of Illinois' standards for personal and academic
conduct. Proper conduct entails creating a positive learning experience for
all students, regardless of sex, race, religion, sexual orientation, social
class, or any other feature of personal identification; therefore, sexist,
racist, prejudicial, homophobic, or other derogatory remarks will not be
tolerated.

### Syllabus amendment

This syllabus may be amended or modified in any way upon notice, with the
version on GitHub being authoritative. Most such changes will affect the
tentative schedule, but be sure that you know if any due dates change.

### Reaching me

The fastest ways to get help are office hours and any time my door is open.
Email works too: I respond promptly on weekdays, but I will not respond to
email over the weekend (6:00 pm Friday to 8:00 am Monday), though I will take
into account when you sent it. On the weeks I am traveling, expect Zoom office
hours and slower replies. This class should be fun, and the primary learning
outcome is that you grow as a scientist; if something is getting in the way of
that, tell me early.

## Important dates

- Aug. 25, 2026: First day of class
- Sep. 8, 2026: Astronomy Colloquium by Kareem El-Badry, who led the Gaia BH1
  black-hole discovery you'll meet on day one. **Extra credit, +5 points on
  Quiz 1:** attend (there will be a signup sheet) or watch the YouTube
  recording afterward, and turn in at least a page of notes including two
  questions you had, by Noon Tue Sep. 15
- Oct. 8, 2026: Midterm take-home posted (due Oct. 14 by Noon; defenses
  Oct. 19–23)
- Oct. 20, 2026: Capstone topics due (chosen with me)
- Nov. 24 & 26, 2026: Fall break, no class
- Dec. 3 & 8, 2026: Capstone lightning talks in class
- Dec. 7, 2026: Capstone notebooks & videos due by Noon
- Dec. 9, 2026: Last day of instruction
- Dec. 9, 2026: Final take-home posted (due Dec. 15 by Noon; defenses
  Dec. 15–17)

## Class schedule, Fall 2026 (subject to revision)

*Instructor travel:* I am at conferences or giving invited talks during the
weeks of Sep 1, Sep 8, Sep 29, Oct 13, Nov 3, and Nov 17 — marked *(travel)*
below (shaded grey in the PDF). The affected sessions will be led by a
substitute or held on Zoom; watch your email for the arrangements each week.

- **Aug 25, 27** — First steps, crash course in python; how this course
  treats AI, including a live demonstration of an AI agent solving (and
  botching) a problem set
- **Sep 1, 3** *(travel)* — Probability distributions, descriptive statistics, the
  Central Limit theorem and when it doesn't hold, robust statistics, and
  hypothesis testing (ICVG Ch. 3, FB Ch. 2)
- **Sep 8, 10** *(travel; the TA proctors Quiz 1 on Tue)* — Statistical inference, frequentist properties such as
  unbiasedness & the Cramér–Rao bound, consistency, asymptotic limits,
  mean-squared errors (ICVG Ch. 4, FB Ch. 3)
- **Sep 15, 17** — Maximum likelihood estimation and applications, ranting
  about minimizing chi-squared (ICVG Ch. 4)
- **Sep 22, 24** — Regression & Inference: ordinary least squares,
  generalized least squares, orthogonal distance regression vs generative
  modeling of data (ICVG Ch. 8, FB Ch. 7)
- **Sep 29, Oct 1** *(travel; GN via Zoom Sep 29; guest lecture Padma Venkatraman
  Oct 1)* — Bayes in practice, sampling and Markov Chain Monte Carlo methods
  (ICVG Ch. 5)
- **Oct 6, 8** — Building models, effective sampling techniques, estimating
  parameters & uncertainties, posterior predictive checks, other MCMC
  wizardry (ICVG Ch. 8). **Midterm posted Oct 8.**
- **Oct 13, 15** *(travel)* — Visualization as verification: plots that catch broken
  models before referees do (VdP Ch. 4). **Midterm due Oct 14 by Noon;
  defenses Oct 19–23.**
- **Oct 20, 22** — Time-series analysis (ICVG Ch. 10, FB Ch. 11), Gaussian
  processes (ICVG Ch. 8.10, readings from Rasmussen & Williams)
- **Oct 27, 29** — Probabilistic Graphical Models (PGMs) & hierarchical Bayes
  (readings from Hilbe, de Souza & Ishida)
- **Nov 3, 5** *(travel; on Zoom, the TA proctors Quiz 4 on Tue)* — The ABCs of not having a likelihood function: ABC and
  simulation-based inference (readings from Hilbe, de Souza & Ishida)
- **Nov 10, 12** — Machine learning: tree methods, supervised classification,
  outliers, imbalanced & missing data; unsupervised clustering, density
  estimation & dimensionality reduction (ICVG Ch. 6, 7, 9, VdP Ch. 5)
- **Nov 17, 19** *(traveling Tue only)* — Neural networks to foundation models: how modern
  astronomical surveys use deep learning, with case studies from time-domain
  astronomy
- **Nov 24, 26** — Fall break (Nov 21–29), no class. Nothing is due over
  break: the lab posted Nov 19 is due Wed Dec 2.
- **Dec 1, 3** — Large language models and AI agents: how they work, how they
  fail, and verification as a statistical problem, applying everything this
  course taught you to the machine itself (Tue and the first half of Thu).
  **First ten lightning talks Thu Dec 3; capstone notebooks & videos due Mon
  Dec 7 by Noon.**
- **Dec 8** — Remaining ten lightning talks; course wrap. **Final posted Dec 9.**
- **Dec 15** — Final take-home due by Noon; defenses Dec 15–17 (finals
  period; grades are due to the Registrar Dec 22).
