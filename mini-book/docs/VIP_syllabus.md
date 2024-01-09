Instructor: A. J. Medford

TA's: Lucas Timmerman, Logan Brabson, Neung-Kyung Yu

Email: [ajm@gatech.edu](mailto:ajm@gatech.edu)

[ltimmerman3@gatech.edu](mailto:ltimmerman3@gatech.edu)
       
[lbrabson3@gatech.edu](mailto:lbrabson3@gatech.edu)
       
[nyu49@gatech.edu](mailto:nyu49@gatech.edu)
       
Dr. Medford Office Hours: [By Appointment](https://app.acuityscheduling.com/schedule.php?owner=18040156&appointmentType=11047919)

TA Office Hours: Set up via email or slack correspondence

Class Hours: W 9:30-10:20am

Class Room: Zoom (see Canvas App)

Training Materials: [Jupyter Book](https://medford-group.github.io/training-materials/)

Course Description
==================

About VIP
---------

The Vertically-Integrated Projects (VIP) Program operates in a research
and development context. Undergraduate students that join VIP teams earn
academic credit for their participation in design/discovery efforts that
assist faculty and graduate students with research and development
issues in their areas of expertise.

The teams are:

-   Multidisciplinary - drawing students from all disciplines on campus;

-   Vertically-integrated - maintaining a mix of sophomores through PhD
    students each semester;

-   Long-term - each undergraduate student may participate in a project
    for up to three years and each graduate student may participate for
    the duration of their graduate career.

The continuity, technical depth, and disciplinary breadth of these teams
are intended to: Provide the time and context necessary for students to
learn and practice many different professional skills, make substantial
technical contributions to the project, and experience many different
roles on a large, multidisciplinary design/discovery team. Support
long-term interaction between the graduate and undergraduate students on
the team. The graduate students mentor the undergraduates as they work
on the design/discovery projects embedded in the graduate students’
research. Enable the completion of large-scale design/discovery projects
that are of significant benefit to faculty members’ research programs.

About Big Data and Quantum Mechanics
------------------------------------

This course explores projects at the intersection of computational
chemistry (quantum mechanics) and data science (big data) within the
application domain of surface science and catalysis. The team merges
expertise from computational and physical sciences, and students from
computer science, electrical engineering, industrial & systems
engineering, chemical engineering, chemistry, physics, and materials
science. The VIP course consists of sub-teams with research topics
developed by graduate students in the Medford group:

-   Training (led by Logan Brabson): All new students must complete a training program that
    involves the basics of high-performance computing, common quantum-mechanical techniques
    such as Density Function Theory (DFT), and the development and use of machine learning 
    techniques such as neural networks. DFT software packages are well-established, but 
    require the use of supercomputing resources and must be converged with respect to
    several numerical parameters. The training will cover approximately 10 weeks and is
    highly represnetative of training programs for new graduate students in this field.

-   Terminus Upgrade (led by Lucas Timmerman): This semester, my team will focus on upgrading the Medford Group computational infrastructure. The group's server, Terminus, is in desperate need of a revamp. The plan is to identify an ideal Linux based operating system to install for facilitating the group's research operations. Once finiished, the team will turn to focusing on installing and learning the Computational Catalysis Interface (CCI) developed by the Hibbits lab which will enable us to further diversify the group's computatinal resources. Finally, we will experiment with the new file storage system, CEDAR, for use in io operations across clusters. 

-   DFT Modeling of Surface Reactions (led by Neung-Kyung Yu):  This project involves using Density Functional Theory (DFT) to model and investigate surface reactions. DFT is a widely-used computational approach for simulating atomistic models. The project will employ the [SPARC code](https://www.sparc-x.com/), a recent DFT package developed by Prof. Suryanarayana at Georgia Tech, designed for massive parallel calculations. In this project, we will go beyond the scope of the DFT training materials and apply DFT to study fascinating surface reactions. Prior knowledge of the topics isn't required, but an interest in computational investigation of chemical reactions is needed as the project will involve greater complexity in both DFT and chemistry. Additionally, the project will involve testing new features in SPARC and enhancing its Python API.

-   Machine Learning for Electronic Structure (led by Jagriti Sahoo): This project focuses on crafting machine learning models to establish a framework to correct the DFT energies to that calculated at a higher level of theory (any wave-function method) using electron density fingerprints. We will leverage the [fingerprinting scheme](https://journals.aps.org/prmaterials/pdf/10.1103/PhysRevMaterials.3.063801) developed in previous research from our group that uses Maxwell-Cartesian Spherical Harmonics (MCSH) to project the electron density onto a basis for representation. This project involves improving the descriptor calculation scheme in SPARC, understanding and running DFT calculations to generate electronic structure data, and analyze them using supervised and unsupervised ML methods. The students will gain hands on experience in python and parallel programming in C, using supercomputing resources as well as emerging ML methods. I am looking for students who have prior experience in C programming and a curiousity in emerging ML methods in computational chemistry is strongly encouraged.

-   Machine Learning for Catalyst Discovery in Waste Sludge Chemistry (led by Kaylee Tian): This project delves into the intersection of computational cheminformatics and data analytics. The project focuses on utilizing ML tools to generate surface adsorption energy predictions and data analytics to provide insights for waste sludge chemistry. In this project, the students will utilize existing machine learning models published by [The Open Catalyst Project](https://opencatalystproject.org/) to predict adsorption energy of potential chemicals present in a waste sludge. The Open Catalyst Project aims to use machine learning for approximating quantum mechanical simulations (density functional theory) and discovering new catalysts. Then using data analytics and visualization techniques, the students will draw meaningful insights on material's reactivity relations. The students will gain hands on experience in python as well as experience in data analytics. Students with prior experience in python programming will be prefered. 


Returning VIP students who previously started work on a project may choose to continue 
building on their existing work isntead of joining one of the above subgroups.
If you are a returning student and are interested in an "independent study" project you should
contact Dr. Medford as soon as possible to initiate discussions on what is within scope for
the course and what is feasible given timelines and resources.

Course Logistics
================

The course will utilize the following resources for communication and
submission of assignments:

-   Github: All course materials will be posted to Github.

-   Canvas: The course Canvas site will be used for submission of
    assignments and peer grading.

-   Slack: The group Slack channel is the preferred method of
    communication with instructors and graduate students. You are
    responsible for anything that is announced in the `vip`
    Slack channel. You can join the Slack channel via [this link]( https://join.slack.com/t/slack-ymv5720/shared_invite/zt-21v1xmbap-5FQMR2rgE0B5krwMZPFyBQ ).

Course Objectives
=================

1.  Generate atomistic simulation and adsorption energy data using density functional theory (DFT)

2.  Converge numerical calculations with respect to input parameters

3.  Submit, manage, and analyze high-performance computing jobs

4.  Utilize machine-learning packages to model and predict the output of atomistic
    simulations

5.  Work with a team to solve real-world problems at the intersection of
    big data and quantum mechanical simulations

Course Structure
================

The grade will be assigned based on three categories:

-   Documentation: 33.3 %

-   Personal Accomplishments: 33.4 %

-   Teamwork and Interactions: 33.3 %

A grade of 0-5 will be assigned for each category based on the criteria
outlined below. A total grade will be computed based on the weighted
average of the 3 categories which will be converted to letter grades
using the following:

-   A: > 4

-   B: > 3

-   C: < 3

-   D: < 2

You will receive a grade at the midterm and after the end of the course.
**Both grades will averaged to determine your final letter grade.**

Documentation
-------------

The documentation grade will be assessed based on bi-weekly updates submitted via Canvas.
The weekly update should include the following components:

- Tasks completed in the prior week
- Discussion of any key challenges or results
- Tasks to be completed in future weeks
- Documentation needed to repeat analysis and access results
- A literature review of at least one paper that you read or used during the weeks (see [literature review lecture](lit-search))


Documentation for the bi-weekly updates should be provided as a text file or Word document.
Bi-weekly updates will be peer graded on a scale of 0-5 based on the following criteria (decimal scores are allowed):

-   5: Remarkable progress on tasks, clear description of process and findings, a well-defined plan for the next weeks, and relevant citations (A+)

-   4: Average progress on tasks, some documentation of results/challenges, a reasonable plan for the coming weeks, and relevant citation (A)
Goals are completely achieved (A)

-   3: Some progress on tasks, but documentation and/or plan is lacking detail. A citation is provided, but lacks relevance or appears to be re-used (B)

-   2: Very little progress on tasks, documentation and/or plan is omitted or incomplete. Citation lacks relevance or is omitted (C)

-   1: Clear lack of effort in completing tasks, documentation and plan are omitted or irrelevant. Citation not provided (D)

-   0: No submission

Bi-weekly updates should be compiled into a single document and submitted at the midterm and final. Instructors will review the average score from bi-weekly updates and compare this to the compiled updates to ensure that the peer grading is appropriate, and to ensure that citations are not recycled. Instructors reserve the right to revise the average score up or down if substantial inconsistencies between the score and the criteria above are observed.

Personal Accomplishments
------------------------

Personal accomplishments will be measured by self-defined goals and will be assessed
by each student's respective sub-team mentor. 
Within the **first three weeks** of the semester students will work with their 
sub-team mentor to define midterm and
semester goals for their specific tasks within their sub-team. 
Each goal should have a deliverable
that can be unambiguously evaluated as complete or incomplete (computer
code, report, figure, etc.), and each student should submit a
deliverable. Deliverables submitted by team members need not be unique,
but self-defined goals should be individualized, such that each
team member has different deliverables that support a larger team-based
goal.

-   5: Goals are completely achieved and additional progress has been
    made (A+)

-   4: Goals are completely achieved (A)

-   3: Goals are partially achieved (B)

-   2: Some progress has been made, but goals are not achieved (C)

-   1: No substantial progress is made towards goals (D)

The letter grade will be determined by the sub-team leader, and
is generally controlled by two factors: i) ability to plan research and
set realistic targets and ii) ability to achieve goals and deliver on a
plan. The best way to ensure success is constant dialogue and communication
with your sub-team leader about what you think you can achieve, and
any challenges you're facing.

Goals and deliverables for the training team will be provided
by instructors and are known to be achievable based on prior 
 experience.


#### Submission and review:
The deliverables will be submitted via
Canvas as a .zip file, and a copy of the project goals document should
be included with the submission to aid the reviewers. 
**All submissions should contain a file named "README"** that explains the
accomplishments in the context of the project goals and points the reviewer
to necessary information.
Any external deliverables (e.g. websites, Github, etc.) should be
clearly referenced. The README can also contain any comments, instructions, or
context that may be important for a grader. Only materials included in or referenced in the submission
should be used to assess the criteria (e.g. if a group presents
something in the VIP meeting but does not include it in the submission
then it does not count).

Teamwork and Interaction
------------------------

Teamwork and interaction will be graded based on peer evaluations
conducted through the VIP website and your participation in peer grading.
Note that this can be confusing. **Peer evaluations** occur twice per
semester through the VIP website, while **peer grading** occurs bi-weekly for
documentation.
The **response rate for peer grading and peer evaluations will account 
for 40% of the teamwork and interaction grade.**, while the scores you receive
from your teammates in the peer evaluation will account for the other 60% of
this grade. Note that you **only need to complete peer evals for your sub-team members**,
but **peer grading will be across different subteams** and will be explicitly
assigned.

Course Format
-------------

The course will by offered in a hybrid format. We have multiple online MS students who work in the course, so it is important to provide a mechanism for remote participation. 
The main lecture will take place virtually, but sub-teams can meet in person and/or use hybrid meetings. For the training, group, lectures will be given live during the course time and **will not be recorded.** If you miss a lecture you are responsible for following up with other students and the TA's to catch up on what you missed.
The project groups will use the course time to meet and discuss progress on projects.


Training Schedule *(all synchronous)*
========

Week 1 (1/10): Introduction to VIP and projects (Medford)

Week 2 (1/17): VIP Subteam pitches (Medford/Timmerman/Yu/Sahoo/Tian)

Week 3 (1/24): Literature searches (Medford) - Bi-weekly Update 1

Week 4 (1/31): Intro to Python and HPC (Brabson)

Week 5 (2/7): Intro to ASE (Brabson) - Bi-weekly Update 2 (Ex. 1.6.1-1.6.5)

Week 6 (2/14): Software check (Brabson)

Week 7 (2/21): Midterm Updates (pre-recorded presentations, virtual synchronous Q&A) - Bi-weekly Update 3 (Ex. 2.5.1 & 3.3.1-3.3.4)

Week 8 (2/28): Intro to Density Functional Theory (Medford/Brabson)

Week 9 (3/6): DFT calculations and applications (Brabson) - Bi-weekly Update 4

Week 10 (3/13): Machine Learning Basics (Brabson)

Week 11 (3/20): Spring Break

Week 12 (3/27): Projects (Timmerman/Yu/Sahoo/Tian) - Bi-weekly Update 5 (Ex. 5.4.1-5.4.3 & 6.4.1)

Week 13 (4/3): Projects (Timmerman/Yu/Sahoo/Tian)

Week 14 (4/10): Projects (Timmerman/Yu/Sahoo/Tian) - Bi-weekly Update 6 (Ex. 6.4.2 & 7.3.1-7.3.3)

Week 15 (4/17): Final Updates (pre-recorded presentations, virtual synchronous Q&A)

Changes to Syllabus
===================

The schedule and syllabus are subject to change. Given that this is a
research course, changes are to be expected; however, we will do our
best to notify you of any changes and implement them as fairly as
possible.
