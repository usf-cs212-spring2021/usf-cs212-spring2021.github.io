---
layout: guides
navbar: Guides
title: Homework Setup
key: 1
---

Before you begin, you need to make sure to go through the other setup guides first:

  - [General Guides](/guides/general/)
  - [Eclipse Guides](/guides/eclipse/)

For every homework assignment, you will need to repeat these steps:

  - **Setup your Github repository.** Click the Github Classroom invitation link on Canvas to automatically setup a private Github repository with the template and test code. Only you, the TAs, and the instructor will have access to this repository.

  - **Setup your Eclipse project.** Once your repository is setup, you must import the homework as a Java Maven Project in Eclipse. See the [Importing Eclipse Projects from Github](/guides/eclipse/importing-eclipse-projects-from-github.html) guide for detailed steps.

  - **Verify you can push changes to Github.** In Eclipse, make a minor change and [commit and push](http://wiki.eclipse.org/EGit/User_Guide#Committing_Changes) that change to Github. I recommend placing the [Git Staging View](http://wiki.eclipse.org/EGit/User_Guide#Git_Staging_View) somewhere on your Eclipse layout to make this process more convenient.

  - **Verify you can run the JUnit tests on Eclipse locally.** The tests will be in the `src` » `test` » `java` subfolder. Right-click the test file and select "Run As" » "JUnit Test" from the menu.

At this point, you should be able to start filling in the missing code, committing changes, and pushing those changes to Github.

Refer to the `TODO` comments in the template code for specifics on what code to fill in or modify for the assignment. When modifying this code, keep in mind the following:

  - **Do not modify any method or class declarations.** For example, you cannot add or remove keywords like `static` or add a `throws` keyword to a method if one was not already included.

  - **Do not modify methods that are already fully defined.** For example, if a method is provided and has no `TODO` comments within the method definition, you may not modify that method.

  - **Do not modify the test code.** This includes any input or output files utilized by the test code.

  - You MAY add additional members, methods, and classes as needed to the code.

  - You MAY add comments to clarify code for yourself. You can add comments to already defined methods if you want.

  - You MAY change a `return` statement in a method with a `TODO` comment as needed. (You may *not* change the return type in the method declaration, however.)

  - Remove the `TODO` comments when you are done. This removes them from the "Tasks" view in Eclipse. If you want to keep the comment around, you can change the text `TODO` to `DONE` instead.

To receive full credit on any homework assignment, you must:

  - **Pass all of the unit tests remotely.** See the [Homework Testing](/guides/homework/homework-testing.html) guide detailed steps. You will not receive full points if you are passing the tests locally but not remotely.

  - **Commit your work often.** Ideally, you should commit after you complete every `TODO` in the code. For example, if there are 5 `TODO` comments in the code, your repository should have at least 5 commits. <i class="fas fa-star has-text-warning"></i>

  - **Follow the `TODO` directions.** For example, if the `TODO` comment stated you must use a `HashSet` and your code does not, you could lose points even if you are passing all of the unit tests.

  - **Properly submit your homework on time.** Remember, there are [no late homework](/syllabus.html#late-policy) submissions unless you apply for a [policy exception](/syllabus.html#policy-exceptions).

Post on [CampusWire]({{ site.data.info.links.forums.link }}) if you have any questions regarding what must be done for a homework assignment or a question about your homework grade.
