---
title: Course Syllabus
hidecrumbs: true
navbar: Syllabus
layout: guides
---

# CS 212 Software Development
{: .title }

#### Spring 2021 &bull; CS 212-01, CS 212-02 &bull; 4 Credits
{: .subtitle .has-text-weight-light }

{{ site.data.info.blurb }}

[USF Catalog](https://catalog.usfca.edu/preview_course_nopop.php?catoid=22&coid=186456)
{: .button .is-primary }


## Summary

This syllabus is similar to a contract between students and the instructor, and as such it is quite long (with many sections required by the university). A few key points from this syllabus are highlighted here:

  - We will primarily use [CampusWire]({{ site.data.info.links.forums.link }}) for all asynchronous communication for this class, not email. See: [Communication Policy](#communication-policy)

  - You should be stuck for an hour on a problem before seeking help, but you should definitely seek help if you have been stuck for an hour. See: [Getting Help](#asynchronous-communication)

  - Do not cheat. This includes working too closely with your classmates or the CS tutors. See: [Cheating Policy](#cheating-policy)

  - You must pass at least one exam to earn a C or higher letter grade in this class. See: [Pass Requirements](#pass-requirements)

  - You must make enough progress on projects to earn a C or higher letter grade in this class. See: [Pass Requirements](#pass-requirements)

  - You are required to either attend 1 synchronous lecture per week or watch the lecture recording. See: [Attendance](#attendance)

  - You are required to participate in 1 synchronous or asynchronous interaction per week outside of class. See: [Attendance](#attendance)

  - There are automatic exceptions granted for certain situations. See: [Policy Exceptions](#policy-exceptions)

  - Treat this class like a part-time job and plan to spend 10 to 20 hours coding per week outside of class. See: [Credit Hour Policy](#credit-hour-policy)

You are still required to read through the entire syllabus below.

## Course Details
{: .page-header }

This section covers basic information about the course, instructor, and teacher assistants.

### Lecture Sections

This syllabus covers the following lecture sections:

<div class="columns">
  <div class="column is-narrow">
    <strong>CS 212-01 (CRN 20428)</strong><br/>
    <i class="fa-fw fas fa-calendar-alt"></i>
    <del>Tuesdays</del>, Thursdays<br/>
    <i class="fa-fw fas fa-clock"></i>
    12:45pm &ndash; 2:30pm<br/>
    <i class="fa-fw fas fa-signal-stream"></i>
    Zoom: <a href="{{ site.data.info.streams.lecture1.link }}">{{ site.data.info.streams.lecture1.room }}</a>
  </div>

  <div class="column is-narrow">
    <strong>CS 212-02 (CRN 21979)</strong><br/>
    <i class="fa-fw fas fa-calendar-alt"></i>
    <del>Tuesdays</del>, Thursdays<br/>
    <i class="fa-fw fas fa-clock"></i>
    4:35pm &ndash; 6:20pm<br/>
    <i class="fa-fw fas fa-signal-stream"></i>
    Zoom: <a href="{{ site.data.info.streams.lecture2.link }}">{{ site.data.info.streams.lecture2.room }}</a>
  </div>  
</div>

Generally, Tuesday lectures will be replaced by pre-recorded asynchronous content. Thursday lectures will be held synchronously via Zoom and recorded. See the [course schedule]({{ "/schedule.html" | relative_url }}) for details.

<i class="fas fa-info-circle"></i>
See the [Attendance Policy](#attendance-policy) for whether you can attend a section you are not enrolled.
{: class="notification" markdown="1" }

### Lab Sections

This syllabus covers the following lab sections:

<div class="columns">
  <div class="column is-narrow">
    <strong>CS 212L-01 (CRN 20454)</strong><br/>
    <i class="fa-fw fas fa-calendar-alt"></i>
    Fridays<br/>
    <i class="fa-fw fas fa-clock"></i>
    2:15pm &ndash; 3:20pm<br/>
    <i class="fa-fw fas fa-signal-stream"></i>
    Zoom: <a href="{{ site.data.info.streams.lab1.link }}">{{ site.data.info.streams.lab1.room }}</a>
  </div>

  <div class="column is-narrow">
    <strong>CS 212L-02 (CRN 22014)</strong><br/>
    <i class="fa-fw fas fa-calendar-alt"></i>
    Fridays<br/>
    <i class="fa-fw fas fa-clock"></i>
    3:30pm &ndash; 4:35pm<br/>
    <i class="fa-fw fas fa-signal-stream"></i>
    Zoom: <a href="{{ site.data.info.streams.lab2.link }}">{{ site.data.info.streams.lab2.room }}</a>
  </div>
</div>

The first several lab sessions will be lead by the instructor and held synchronously. These will not be recorded, as much of the time is spent in breakout rooms.

Later in the semester, the lab sessions will convert to TA office hours and one-on-one code reviews with the instructor.

<i class="fas fa-info-circle"></i>
See the [Attendance Policy](#attendance-policy) for whether you can attend a section you are not enrolled.
{: class="notification" markdown="1" }

### Instructor and Assistants

The instructor and instructor office hours for this course will be:

<div class="columns">
  <div class="column is-narrow">
    <div class="box">
      <!-- nested columns for profile photo -->
      <div class="columns is-mobile is-variable is-1">
        <div class="column is-narrow">
          <div class="image is-64x64">
            <img class="is-rounded" src="/images/engle.png">
          </div>
        </div>

        <div class="column">
          <strong>Sophie Engle</strong><br/>
          <i class="fa-fw fas fa-calendar-alt "></i>
          <span>Mondays, Thursdays</span>
          <br/>

          <i class="fa-fw fas fa-clock "></i>
          <span>2:45 &ndash; 4:15pm</span>
          <br/>

          <i class="fa-fw fas fa-signal-stream "></i>
          Zoom: <a href="{{ site.data.info.streams.instructor.link }}">{{ site.data.info.streams.instructor.room }}</a>
          <br/>

          <i class="fa-fw fas fa-globe "></i>
          <a href="//sjengle.cs.usfca.edu">sjengle.cs.usfca.edu</a>
        </div>
      </div>
      <!-- end nested columns -->
    </div>
  </div>
</div>

The teacher assistant and teacher assistant office hours for this course will be:

<div class="columns">
  <div class="column is-narrow">
    <div class="box">
      <!-- nested columns for profile photo -->
      <div class="columns is-mobile is-variable is-1">
        <div class="column is-narrow">
          <div class="image is-64x64">
            <img class="is-rounded" src="/images/corella.jpg">
          </div>
        </div>

        <div class="column">
          <strong>José Corella</strong><br/>
          <i class="fa-fw fas fa-calendar-alt "></i>
          <span>Mon/Wed 10:00 – 10:45am</span>
          <br/>

          <i class="fa-fw fas fa-calendar-alt "></i>
          <span>Mon/Wed 5:00 – 5:45pm</span>
          <br/>

          <i class="fa-fw fas fa-signal-stream "></i>
          Zoom: <a href="{{ site.data.info.streams.tajose.link }}">{{ site.data.info.streams.tajose.room }}</a>
          <br/>

          <i class="fa-fw fas fa-tasks bump"></i>
          Projects, Lab 1
        </div>
      </div>
      <!-- end nested columns -->
    </div>
  </div>

  <div class="column is-narrow">
    <div class="box">
      <!-- nested columns for profile photo -->
      <div class="columns is-mobile is-variable is-1">
        <div class="column is-narrow">
          <div class="image is-64x64">
            <img class="is-rounded" src="/images/weinstein.jpg">
          </div>
        </div>

        <div class="column">
          <strong>Lev</strong>in <strong>Weinstein</strong><br/>
          <i class="fa-fw fas fa-calendar-alt "></i>
          <span>Tue 2:45 – 4:15pm</span>
          <br/>

          <i class="fa-fw fas fa-calendar-alt "></i>
          <span>Wed 1:15 – 2:45pm</span>
          <br/>

          <i class="fa-fw fas fa-signal-stream "></i>
          Zoom: <a href="{{ site.data.info.streams.talev.link }}">{{ site.data.info.streams.talev.room }}</a>
          <br/>

          <i class="fa-fw fas fa-tasks bump"></i>
          Homework, Attendance, Labs
        </div>
      </div>
      <!-- end nested columns -->
    </div>
  </div>

  <div class="column is-narrow">
    <div class="box">
      <!-- nested columns for profile photo -->
      <div class="columns is-mobile is-variable is-1">
        <div class="column is-narrow">
          <div class="image is-64x64">
            <img class="is-rounded" src="/images/cabezudo.jpeg">
          </div>
        </div>

        <div class="column">
          <strong>Andrew Cabezudo</strong><br/>
          <i class="fa-fw fas fa-calendar-alt "></i>
          <span>Pending</span>
          <br/>

          <i class="fa-fw fas fa-signal-stream "></i>
          Zoom: <a href="{{ site.data.info.streams.tadrew.link }}">{{ site.data.info.streams.tadrew.room }}</a>
          <br/>

          <i class="fa-fw fas fa-tasks bump"></i>
          Participation, Lab 1
        </div>
      </div>
      <!-- end nested columns -->
    </div>
  </div>
</div>

All instructors and teacher assistants will hold office hours and assist with questions on CampusWire in addition to the tasks listed above.

<i class="fas fa-envelope-open-text"></i>
See the [Communication Policy](#communication-policy) for how to contact the instructor and TAs.
{: class="notification" markdown="1" }

### Prerequisites

The prerequisite for this class is [CS 245 Data Structures and Algorithms](https://catalog.usfca.edu/preview_course_nopop.php?catoid=22&coid=186459) with a letter grade of C or higher. You may not take the prerequisite at the same time as this class.

There is a lab corequisite of [CS 212L](https://catalog.usfca.edu/preview_course_nopop.php?catoid=22&coid=189646) that you must take at the same time as this class.

This course is currently restricted to Computer Science majors and minors.

### Required Materials

This course utilizes resources and software that are freely available for enrolled students. There are no required books.

### Important Dates

Below are important dates relevant to this class:

| 🚩 | Date  | Description |
|---:|:-----:|:------------|
|    | 01/25 | Spring 2021 classes begin. |
|    | 01/29 | Last day to add classes online. |
|    | 02/12 | Census date; last day to drop without a "W" appearing on transcript. |
| 🚩 | 03/09 | Exam 1; retake opportunity on Thursday. |
|    | 03/16 | Beginning of a week-long spring break. |
|    | 03/23 | Classes resume following spring break. |
| 🚩 | 04/09 | Project Cutoff; deadline to meet the [project pass requirement](#pass-requirements). |
|    | 04/01 | Easter holiday begins at 4pm. |
|    | 04/12 | Last day to withdraw from a class and receive a "W" on transcript. |
| 🚩 | 05/04 | Exam 2; retake opportunity on Thursday. |
|    | 05/13 | Spring 2021 classes end. |
|    | 05/15 | Finals begin; start of final code reviews. |
{: class="table dates is-hoverable" style="width: auto;" }

See the [official academic calendar](https://myusf.usfca.edu/registration/academic-calendar) for other important dates.

<i class="fas fa-info-circle"></i>
There will be an individually-scheduled final code review instead of a final exam during finals week.
{: class="notification" markdown="1" }

## Learning Outcomes
{: .page-header }

This section covers the learning outcomes related to this course.

### Course Learning Outcomes

At the end of this course, you should be able to:

  1. Independently design programs
  2. Implement large programs with 1,000 to 2,000 source lines of code (SLOC)
  3. Design and execute tests to identity and repair software bugs
  4. Redesign and refactor code to improve quality

See the [Assessment](#assessment) section for how these learning outcomes will be assessed.

### Program Learning Outcomes

The relevant Program Learning Outcomes (PLOs) for this course with respect to the [Computer Science Major](https://catalog.usfca.edu/preview_program.php?catoid=22&poid=13114&returnto=3095) (including [4 + 1 Dual Degree](https://catalog.usfca.edu/preview_program.php?catoid=22&poid=13333&returnto=3095) program) are:

  > **Application:** Apply problem-solving skills to implement medium and large scale programs in a variety of programming languages

  > **Project:** Demonstrate effective communication and organization as part of a team of software developers or researchers collaborating on a large computer program

This course satisfies the "Application" outcome and prepares students for the "Project" outcome.

This relevant PLO for this course with respect to the [Computer Science Minor](https://catalog.usfca.edu/preview_program.php?catoid=22&poid=13115&returnto=3095) is:

> Implement an intermediate-size program in one programming language

This course satisfies the above outcome.

See the [Computer Science](https://catalog.usfca.edu/preview_entity.php?catoid=22&ent_oid=1639&returnto=3095) entry of the USF catalog for details on the department-wide objectives.

## Assessment
{: .page-header }

Assessment of the learning outcomes will be done by a combination of pass requirements and assignments. Specifically, students will earn a letter grade based on their performance on exams, homework, projects, and other assignments. Students not meeting one or more of the pass requirements will have that capped to a C- maximum letter grade.

### Pass Requirements

To ensure you are meeting the [learning outcomes](#learning-outcomes) for this course, you must meet the following minimum requirements to receive a C or higher grade in this course:

  - **Exam Pass Requirement:** Students must receive an average C letter grade or higher on at least one exam and its retake(s).

  - **Project Pass Requirement:** Students must pass project 1 functionality, project 1 design, and project 2 functionality BEFORE the withdraw deadline. The cutoff for this requirement is **April 9, 2021** and the withdraw deadline is **April 12, 2021** for the Spring 2021 semester.

**Failure to meet 1 or more of the following requirements will cap your letter grade for this course to C– maximum, regardless of whether you have a higher letter grade in Canvas.**
{: .has-text-danger }

The exam pass requirement assesses that students understand the underlying concepts required to meet the learning outcomes. The project pass requirement assesses that students are able to utilize those concepts in practice to meet the learning outcomes. All other assignment categories are in support of these two primary means of assessment.

If you are concerned about not meeting one or more of these requirements by the withdraw deadline, you are encouraged to consult with the instructor. Your best option may be to withdraw from the class. Note, however, that a W (withdraw) counts as an attempt and CS majors and minors have restrictions on how many times they may attempt CS courses.

<i class="fas fa-exclamation-triangle"></i>
Meeting the pass requirements does not guarantee a passing grade. See the [Grade Breakdown](#grade-breakdown) section below for how the final grade will be calculated.
{: class="notification" markdown="1" }

### Grading Breakdown

If you are meeting the [pass requirements](#pass-requirements), then your final letter grade for this class will be calculated as follows:

| Percent | Category        |
|--------:|:----------------|
|      5% | Attendance      |
|      5% | Participation   |
|      5% | Quizzes         |
|     10% | Exams           |
|     15% | Homework        |
|     60% | Projects        |
{: class="table is-hoverable" style="width: auto;"}

The assignments within each category are not necessarily equally weighted. For example, some participation assignments are worth more points than others.

Each of these categories are described more below, including any relevant policies and how the category relates to learning outcomes.

#### Attendance

There are two weekly attendance requirements, each with synchronous and asynchronous options:

<style>
table.attendance-table {
  width: 100%;
}

table.attendance-table th:first-child {
  white-space: nowrap;
  width: auto;
}

table.attendance-table th:not(:first-child) {
  width: 50%;
}

</style>

| Weekly Requirement | Synchronous Options | Asynchronous Options |
|:------------|:--------------------|:---------------------|
| In Class | Attend at least 1 hour of lecture session. | Watch the entire recording of the lecture session within 48 hours. |
| Outside Class | Attend a lab session, instructor or teacher assistant office hours, (synchronous) code review, CS Tutoring Center appointment, or other CS or university-sponsored student group activity. | Post or respond publicly (to other students) on the [CampusWire]({{ site.data.info.links.forums.link }}) class forum. The post or response may be anonymous. |
{: .attendance-table .is-hoverable .table }

Students are strongly encouraged to select the synchronous option when possible. These requirements are waived for weeks when exams will be administered or opportunities are limited due to holiday breaks.

#### Participation

This category includes pass/fail assignments for completing surveys and discussions, participating in exercises during lecture or lab, and participating in CS-sponsored events.

#### Quizzes

Short quizzes are assigned throughout the week, sometimes at the start of class. Students are given unlimited opportunities to retake quizzes until the deadline. Correct quiz answers are released to the class after the deadline. Quizzes will be conducted on [Canvas]({{ site.data.info.links.canvas.link }}).

#### Exams

There will be two exams. The exams are *not* comprehensive. Instead of a final exam, students will have a final project graded during finals week.

Each exam will have a one or more retake opportunities. The exam score will be the average of the original and retake attempts. See [Important Dates](#important-dates) for the exact exam and exam retake dates.

Students must take the exam and initial retake during their scheduled class time. However, students residing outside of the Pacific time zone (based on the address on file with the university) may request an exam time more appropriate for their time zone. This should be done with caution; the instructor may not be available to answer questions depending on the requested time.

#### Homework

Homework programming assignments are assigned on a semi-weekly basis, and usually due the following week. Students may work on these assignments during their lab session, allowing them to get immediate help from the instructor and teacher assistants.

#### Projects

Programming projects place an emphasis on code quality&mdash;it is not enough to achieve correct results. Each project must pass several functionality tests and then undergo multiple rigorous code reviews checking for specific criteria, such as proper encapsulation and generalization, efficiency, and maintainability.

We use a **mastery learning** approach with projects: students must perfect the current project before moving on to the next project. The final project grade will depend on when and how many projects are completed.

Each project grade is split into two components: functionality (evaluated with automated software tests) and design (evaluated with one-on-one code reviews). The project functionality must be passed before the code review may be passed, students must pass code review for each project sequentially, and may only have at most one synchronous code review appointment per week.

The functionality grade depends on when the project passes the tests. Projects that pass the functionality tests by the deadline will receive a 100%. Otherwise, there will be a --10% late penalty for each week the project is late past the deadline.

The design grade depends on when the project undergoes its first code review. Projects that have at least one code review by the deadline will receive a 100%. Otherwise, there will be a --10% late penalty for each week the **first** code review is late past the deadline. Abuse of the code review process may also result in deductions. For example, failing to fix all of the issues from a previous code review may result in a --5% to --10% deduction.

You must pass project 1 functionality, project 1 design, and project 2 functionality BEFORE the withdraw deadline. See the [Pass Requirements](#{{ "Pass Requirements" | slugify }}) for details.

### Grading Scale

The following is the grading scale mapping percentage to letter grade and GPA for this course:

<style>
table.gpa tbody tr:nth-child(n+9) {
  color: #CD542C;
  font-weight: 500;
}
</style>

|          | Letter |        | GPA |
|---------:|:-------|:-------|:---:|
| 97% &le; | A+     | < 100% | 4.0 |
| 94% &le; | A      | < 97%  | 4.0 |
| 90% &le; | A--    | < 94%  | 3.7 |
| 87% &le; | B+     | < 90%  | 3.3 |
| 84% &le; | B      | < 87%  | 3.0 |
| 80% &le; | B--    | < 84%  | 2.7 |
| 77% &le; | C+     | < 70%  | 2.3 |
| 74% &le; | C      | < 77%  | 2.0 |
| 70% &le; | C--    | < 74%  | 1.7 |
| 67% &le; | D+     | < 70%  | 1.3 |
| 64% &le; | D      | < 67%  | 1.0 |
| 60% &le; | D--    | < 64%  | 0.7 |
|  0% &le; | F      | < 60%  | 0.0 |
{: class="table gpa" style="width: auto;"}

Non-passing grades for undergraduate CS majors and minors are highlighted in <strong class="has-text-danger">red</strong> text. See the [Undergraduate Student Regulations](https://catalog.usfca.edu/content.php?catoid=22&navoid=3097) for more about letter grades and GPA for undergraduate students.

### Student Awards

At the end of the semester, various awards may be given to students. While these awards are informal and do not impact the final grade, they do provide a way for students to differentiate themselves on resumes.

## Course Policies
{: .page-header }

This section includes miscellaneous policies specific to this course, including communication, attendance, credit hours, cheating, and more. These policies are in addition to the standard USF policies included later.

### Communication Policy

Email will NOT be used for communication in this course.

Instead, please see how best to communicate depending on whether you wish to communicate synchronously (live, simultaneously, in real time) or asynchronously (on your own time, without immediate responses or feedback).

##### Synchronous Communication

The synchronous communication that would have occurred in-class will be conducted during the live lectures as follows:

  - [Comment Box](https://PollEv.com/discourses/wTsFNpgkUScBoCcIbyQfI/respond): At the start of class and during breaks, the instructor will enable a poll that allows you to enter questions and comments anonymously.

  - [Raise Hand](https://support.zoom.us/hc/en-us/articles/115001286183): Use the "Raise Hand" feature in Zoom to get the instructor's attention. The instructor will pause and give you an opportunity to ask a question verbally or via the chat.

  - [Meeting Chat](https://support.zoom.us/hc/en-us/articles/203650445-In-Meeting-Chat): Use the in-meeting "Chat" feature in Zoom to ask questions or make comments. These should be posted in the "Everyone" channel (not privately). If you do not want your name to appear in the main chat, you can privately chat the TA to post the question on your behalf instead.

Office hours will also be held via Zoom. Requests will be taken on a first-come first-serve basis (i.e. no appointments). You may join individually or in groups. The instructor will create private breakout rooms to respond to questions as needed.

##### Asynchronous Communication

Most asynchronous course-related communication will be handled using [CampusWire]({{ site.data.info.links.forums.link }})—a forum and chat platform that supports public, anonymous, and private posts. When making posts on CampusWire, please keep the following in mind:

  - **Search other posts first.** It is possible your question has already been asked and answered in another post.

  - **Make most posts public.** You can **post anonymously** if you prefer. Your classmates will not be able to see your identity for anonymous posts, but instructors will still be able to see your name.

  - **Avoid posting code.** If you have a question regarding your specific code, please commit and push your code to your GitHub repository and post a link. That ensures only those with access to your repository (instructor and teacher assistants) will see your code.

  - **Make posts specific to solutions or grades private** to the instructor and teacher assistants. This replaces directly emailing the instructor regarding the course.

  - **Follow the 1 hour rule.** You should be stuck on a problem between 30 minutes to 1 hour before asking for help, but should immediately ask for help if stuck over 1 hour. Worst case, you figure out the answer before we are able to help. Best case, we can help you get unstuck!

  - **Post exact details when possible.** You will get a solution faster if you include as many details as possible when asking for help. This might include exact error messages, stack traces, which tests are failing and passing, console or log output, and more. If you forget, we will have to ask you for this detail which can extend how long it takes to get help.

In addition to [CampusWire]({{ site.data.info.links.forums.link }}), the instructor will also use [Canvas]({{ site.data.info.links.canvas.link }}) to notify students of missing assignments or warn about low grades.

This course also has an [anonymous suggestion box]({{ site.data.info.links.suggestions.link }}) where you can raise non-urgent concerns or suggestions.

<i class="fas fa-exclamation-triangle"></i>
**Under no circumstances should you reach out to the teacher assistants via any unapproved communication channel.** Instructors and teacher assistants must provide all students equal opportunity for course-related help. Using unapproved communication channels creates an unfair advantage over other students and will be treated as a violation of the [Student Conduct Code](https://myusf.usfca.edu/fogcutter).
{: .notification }

### Student Conduct

Students are required to adhere to the University's [Student Code of Conduct](https://myusf.usfca.edu/fogcutter/student-conduct). In short, students are expected to treat each other with respect at all times.

In addition, remote learning often involves a **netiquette policy**. Simply stated, "netiquette" is network etiquette—that is, the etiquette of cyberspace. And "etiquette" means "the forms required by good breeding or prescribed by authority to be required in social or official life." In other words, Netiquette is a set of rules for behaving properly online [[1](http://www.albion.com/netiquette/introduction.html)].

##### Synchronous Netiquette

Activities that are **synchronous** are those that occur live (in real-time) with everyone participating at the same time. This includes livestreamed lectures and labs on Zoom. When communicating and participating in synchronous portions of the course:

  - Arrive on time and attend for the entire session.
  - Listen and dialog with each other respectfully.
  - Participate in live polls and surveys in a timely manner.
  - Need a break? Wait until the scheduled breaks if possible. There will be a 10 to 15 minute break each lecture.

It will always be OPTIONAL whether you wish to enable your audio and/or video. When enabling your audio and/or video, keep in mind the following:

  - The main livestream is recorded for students unable to attend synchronously. If you enable your audio and/or video, it is possible it will be part of the password- protected recording.
  - Consider enabling your audio and video during small group breakout rooms or when asking a question live.
  - Keep your microphone muted unless speaking.
  - If you choose to enable your video, please make sure to present yourself appropriately (dressed as you would be in the classroom) and double-check your background environment (for example, clean up laundry, trash).
  - Be careful what you do while your video is enabled. Everyone can see you in "Gallery View" if you enable video, even if you are not currently speaking.

##### Asynchronous Netiquette

Activities that are **asynchronous** are those that occur outside of class time, usually individually on your own. This includes watching a pre-recorded lecture or participating in an online discussion board. When communicating and participating in asynchronous portions of the course:

  - Be respectful of other participants and keep your comments constructive.
  - Avoid using all caps (may be read as SHOUTING).
  - Keep subject lines clear.
  - Spelling and grammar do count; proofread your writing.
  - Be coherent and succinct.
  - Check the most recent comment/email before replying to an earlier one.
  - Do not falsify information or impersonate others online.  
  - ~~Limit use of acronyms (eg YOLO), icons and emojis.~~ If you want to use an acronym, icon, or emoji (or even a GIF) in this class to express yourself, please feel free to do so :) Just keep it appropriate!

### Attendance Policy

See the [Attendance](#attendance) requirement for this course.

Please attend the section of lecture and lab for which you are registered when possible. Keeping the class sizes balanced is important for interactive exercises.

Attendance is mandatory for exams and all one-on-one synchronous code review appointments. You must be on-time to these appointments. If you arrive more than 5 minutes late, the appointment may be canceled. You risk a grade penalty for repeated canceled or missed appointments.

### Late Policy

Except for projects, late submissions are not normally accepted.

<i class="far fa-tired"></i>
Don't worry---you may request an exception to this late policy in certain cases. See the [Policy Exceptions](#policy-exceptions) section for details.
{: .notification }

### Cheating Policy

All students are expected to know and adhere to the University's [Honor Code](https://myusf.usfca.edu/academic-integrity/). In short, students must never represent another person's work as their own. Examples of honor code violations include (but are not limited to):

  - Copying and pasting code (especially without attribution) from the web
  - Having anyone other than yourself complete your work (including teacher assistants, tutors, and former students)
  - Working too closely with others such that your code no longer represents an individual contribution
  - Sharing your solutions with others (either directly or indirectly)

Keep in mind that unauthorized collaboration or discussion that results in the same or very similar work indicates that you have not placed enough independent thought into your submission and is a violation of the honor code, regardless of whether you directly copied!

**Flagrant or repeat violations of the honor code will result in an F in the course and a report to the Academic Integrity Committee (AIC).**{: .has-text-danger }
At the discretion of the instructor, a less severe penalty may be imposed for minor or first offenses. This is at the sole discretion of the instructor and any violation may result in an F in the course.

<i class="fas fa-code-branch"></i>
Keep in mind that there is a history of your code development on Github. Commit and push changes often to record your incremental code development.
{: .notification }

### Credit Hour Policy

All courses must comply with the [Credit Hour Policy](https://myusf.usfca.edu/sites/default/files/usf_credit_hour_policy_0.pdf), which states:

  > "One unit of credit in lecture, seminar, and discussion work should approximate one hour of direct faculty instruction and a minimum of two hours of out-of-class student work per week through one 15-week semester."

As this is a 4 credit course, students must spend a **minimum** of 8 hours of out-of-class work per week to earn a non-failing (D&ndash; or higher) letter grade. To earn a passing C or higher letter grade (as required for the CS major and minor), students should expect to spend closer to **10 to 15 hours per week** on projects and assignments.

<i class="fas fa-hourglass-half"></i>
Think of this class like a part-time job. If you do not put in the time, you will not make it to the final project. Many students do not pass due to poor time management!
{: .notification }

## Policy Exceptions
{: .page-header }

Life sometimes (often?) interferes with learning, especially in these unprecedented times. Several exceptions to course policies will be granted **automatically** upon request.

These policy exceptions are requested by making a **private post** on [CampusWire]({{ site.data.info.links.forums.link }}) **within one week** of the original deadline. There are several types of exceptions you can request:

| Assignment    | Extensions? | Excused? | Extra Credit? |
|:--------------|:------------|:---------|:--------------|
| Attendance    | No          | Yes (x2) | Yes (x2) |
| Participation | Yes (x1)    | No       | Yes (x1) |
| Quizzes       | No          | Yes (x2) | No       |
| Exams         | No          | No       | No       |
| Homework      | Yes (x2)    | No       | Yes (x1) |
| Projects      | No          | No       | Yes (x3) |
{: .table .is-hoverable style="width: auto;" }

There are no automatic policy exceptions granted for exams. Instead, exams have automatic retake opportunities.

See the following sections for additional details.

### Deadline Extension

These are requests to extend the original deadline of the assignment. You have two options: request a deadline extension of up to 48 hours without a late penalty, or a deadline extension of up to 1 week with a 10% late penalty.

You may have up to 1 participation assignment and 2 homework assignments extended automatically.

### Assignment Excused

These are requests to have the assignment grade excused, such that the grade is not used in your final grade calculation.

You may have up to 2 attendance assignments and 2 quizzes excused automatically.

### Extra Credit

These are requests to make up **missing points** via extra work. Unless otherwise stated, extra credit may not be used to earn over a 100% grade within any category.

You may request extra credit for up to 2 attendance assignments, 1 participation assignment, 1 homework assignment, and 3 projects. The extra credit is handled  differently depending on each category:

  - **Attendance**: You may earn extra credit by attending at least 50% of a synchronous lab session during the exam weeks. There are two opportunities (one for exam 1, one for exam 2).

  - **Participation:** You may earn extra credit by making a public informative post on CampusWire on a topic related to class. For example, making a post (complete with links and screenshots) about a program that makes managing `git` repositories easier.

  - **Homework:** You may earn extra credit by completing the extra credit homework assignment given at the end of the semester.

  - **Projects:** You may earn extra credit by implementing additional functionality in your project. See the [Project Guides](/guides/projects) for details.

Some extra credit opportunities are only available at specific times in the semester. Make sure to keep up to date on course announcements!

### Regret Clause

Did you cross the line and violate the [Academic Honesty](https://myusf.usfca.edu/academic-integrity/) policy? You can invoke the regret clause [[2](https://www.harvardmagazine.com/2020/03/cs50-regret-clause)] to avoid the full consequences outlined in the [Cheating Policy](#cheating-policy) section. Instead, you will be able to resubmit the offending assignment with up to a 40% point deduction depending on the severity of the violation. The incident will still be submitted to the Academic Integrity Committee (AIC) for reporting purposes only.

You must *voluntarily* invoke the regret clause within one week of submitting the offending assignment and attend a one-on-one appointment with the instructor to discuss the specifics of your cheating case to qualify. You cannot retroactively invoke the regret clause. If the instructor confronts you regarding cheating after the grace period, expect full consequences for that action.

You can only invoke the regret clause once. Repeat cheating cases will immediately result in an F for the course and report to the Academic Integrity Committee.

### Other Exceptions

Additional exceptions may be requested for *any* reason, but are more likely to be approved for verifiable exceptional circumstances.

The class is structured such that past certain cutoffs, it becomes infeasible to earn a passing grade by the end of the semester. In those cases, rather than a policy exception, it may be necessary to consider withdrawing or an incomplete.

## University Policies
{: .page-header }

This section includes [standard statements](https://myusf.usfca.edu/arts-sciences/faculty-resources/curriculum/syllabi/policies-legal-declarations) on University policies and resources.

### Students with Disabilities

The University of San Francisco is committed to providing equal access to students with disabilities. If you are a student with a disability, or if you think you may have a disability, please contact [USF Student Disability Services (SDS)](https://myusf.usfca.edu/sds) at [sds@usfca.edu](mailto:sds@usfca.edu) or call (415) 422-2613 to speak with a disability specialist. All communication with SDS is private and confidential. If you are eligible for accommodations, please request that your accommodation letter be sent to me as soon as possible, as accommodations are not retroactive. Once I have been notified by SDS of your accommodations we can discuss your accommodations and ensure your access to this class or clinical setting.

### Behavioral Expectations

All students are expected to behave in accordance with the [Student Conduct Code](https://myusf.usfca.edu/fogcutter) and other University policies.

### Academic Integrity

USF upholds the standards of honesty and integrity from all members of the academic community. All students are expected to know and adhere to the University's [Honor Code](https://myusf.usfca.edu/academic-integrity/).

### Communication

~~All course communications, like all other USF communications, will be sent to your USF official email address. You are therefore strongly encouraged to monitor that email account.~~

<i class="fas fa-info-circle"></i>
See the [Communication Policy](#communication-policy) for this course.
{: class="notification" markdown="1"}

### Counseling and Psychological Services (CAPS)

CAPS provides confidential, free [counseling](https://myusf.usfca.edu/student-health-safety/caps) to student members of our community; an online workshop series open to all students; consultations and referrals; extensive [website resources](https://myusf.usfca.edu/caps); an all hours “warmline” (call 855-531-0761); peer-led Crisis Textline (text HOME to 741741); remote individual and group teletherapy to students residing within California (call 415-422-6352. The Dean of Students Office also offers [Case Management](https://myusf.usfca.edu/dean-of-students/ocrs) support for those seeking off campus mental health services.

### Confidentiality, Mandatory Reporting, and Sexual Assault

For information and resources regarding sexual misconduct or assault visit the [Title IX](https://myusf.usfca.edu/TITLE-IX) coordinator or [USF's Callisto website](http://usfca.callistocampus.org/).
