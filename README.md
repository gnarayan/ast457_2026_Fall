ASTR457: Foundations of Data Science in Astronomy at UIUC, Fall 2026

Gautham Narayan, UIUC

TR, 1230-1350, Astronomy 134

This course has been redesigned for the agentic AI era: AI tools are allowed
and documented on all labs, every student gets their own datasets with truth
held by the instructor, and grades come from verification, calibration, and
your ability to defend your own work. Read the syllabus PDF, especially
"Working with AI: The Ground Rules", before doing anything else.

Instructions

    Clone this repo

    The topics of each week's lectures are described in the syllabus - read
    457_FDS_Syllabus.md (screen-reader-friendly) or 457_FDS_Syllabus.pdf,
    they have identical content

    Lecture slides are in directories named lecture/XY/ where XY is the number of the week

    Various help cheat sheets are included in help/. If you are new to
    astronomy conventions (magnitudes, filters, light curves), read
    help/astro_conventions.md before Lab 01.

    Labs are in the labs/ directory - your dataset is labs/XY/data/<your netid>.csv.
    Only your own dataset will be graded against your truth values, so make sure
    you use yours.

    Every lab and take-home submission includes the AI-use appendix described in
    the syllabus.

    Solutions to labs will be posted over the weekend after the Wednesday they
    were due

    You should also review slides and lab solutions to make sure you understand
    what is happening

Adding to Repo
	git add <file>
	git commit -m "Comment"
	git push

Pulling from <main, origin, upstream>
	git fetch <main, origin, upstream>
	git merge upstream/main -m "Comment"

Submitting your work

    Fork this repo, create a folder named for your NetID inside `submissions/`,
    commit your work there, and
    open a pull request before Noon on the due date (Wednesdays for labs).
