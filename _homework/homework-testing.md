---
layout: guides
navbar: Guides
title: Homework Testing
key: 2
---

Every homework comes with a `src` » `test` » `java` directory with JUnit 5 test code. You must pass all of these tests remotely to earn full credit.

## Local Testing

**You should try passing the tests locally before you try passing them remotely.** Before you can do that, you need to follow the [homework setup](/guides/homework/homework-setup.html) guide to setup the your repository using Github classroom and then import that repository as a Java Project in Eclipse.

To run the JUnit tests provided with the homework template, follow these steps:

  1. Open up the `src` » `test` » `java` subfolder in the Eclipse project.

  2. Open up the class containing the same name as the homework assignment plus the suffix `Test` at the end. For example, for the `ArgumentParser` homework assignment, `ArgumentParserTest` is the associated test class.

  3. From the "Run" menu, select "Run As" &raquo; "JUnit Test" from the menu. If prompted which tests to run, select the one with the same name as the class. For example, for the `ArgumentParser` homework assignment, `ArgumentParserTest` is the associated test class.

      <i class="fas fa-info-circle"></i>
      You can run just the nested tests or one test at a time if you want. This can help you focus on a small number of tests at a time as you develop the code. To do this, right-click the test method or nested test class, and select "Run As" &raquo; "JUnit Test" from the popup menu.
      {: .notification }

  4. Running the tests should open the "JUnit" view. You can use that view to see which tests you are passing and which you are not. See the [Eclipse User Guide](https://help.eclipse.org/2020-12/topic/org.eclipse.jdt.doc.user/reference/views/ref-view-junit.htm) for what each of the buttons mean in this view.

  5. After making changes to your code, you can re-run the tests by following the same steps or clicking the <img alt="Rerun Test" src="https://help.eclipse.org/2020-12/topic/org.eclipse.jdt.doc.user/images/org.eclipse.jdt.junit/elcl16/relaunch.svg"> Rerun Test button.

It is important you only try to pass one test at a time, because the changes you make may affect other tests. You should `git commit` your changes every time you start passing a new test. Please only `git push` your changes at the end of every coding session.

## Remote Testing

Once you are passing all of the tests locally, it is time to test your homework remotely.

PENDING

<i class="fas fa-info-circle"></i>
Commit often, but please do not push until the end of your coding session. Each push triggers the Github Action to run, regardless of whether your code is passing any tests. Under our education plan, we receive a fixed number of free minutes each month.
{: .notification }
