To make updates to the Jupyter book:

* Commit and push to the Github repo (permissions required)
* pip install jupyter-book
* pip install ghp-import
* jb build ./mini-book
* ghp-import -n -p -f mini-book/_build/html   # note: build lands under mini-book/

For VIP semesters, the Training Schedule in docs/VIP_syllabus.md is
generated from the course-admin repo (admin/courses/VIP/<term>/course-admin-VIP,
scripts/sync_schedule.py) — don't hand-edit the marked block. See that
repo's docs/BOOK.md for the full authoring/deploy workflow.
