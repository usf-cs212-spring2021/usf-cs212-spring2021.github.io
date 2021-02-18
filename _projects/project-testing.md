---
title: Project Testing
navbar: Guides
layout: guides
key: 1.2
bump: true

tags:
  - text: 'New'
    type: 'is-primary'
---

You must verify your project is passing the functionality tests to earn the project functionality grade as well as before every code review required to earn your design grade. This guide walks through that testing process.

This guide assumes you have already [setup your project](project-setup.html) in Eclipse.

## Walkthrough Video

The following video 33 minute video gives an overview of projects, how to test projects locally (starting at 13:53), testing projects remotely (starting at 24:33), and get your first functionality grade (starting at 29:38).

<https://usfca.zoom.us/rec/share/eDvBfWphlulSNRnkfA1SHbK3-PKVVJ7qfSrKgUVeF7LOFMYKUCDfu4eNymMxW94B.11aI6blR9502OY7Q?startTime=1613593866000>

## Testing Locally
{: .page-header }

It is important to work and test the projects iteratively, as well as attempt to pass the tests locally before considering running the tests remotely.

### Running Driver

When you first start, very little template code is provided. The tests provided only test the final output of your project, unlike the homework which has tests for individual methods. It will likely take some time before running the JUnit tests will be helpful.

Instead, you may want to start by running your `Driver` class directly using a Run Configuration and manually inspecting the output.

<details>
<p><summary>View Details</summary></p>

<div markdown=1>

  1. Go to the "Run" menu in the menubar at the top of Eclipse and select "Run Configurations..." from the dropdown.

  1. Click on the "Java Application" category in the left view pane and click the "New Configuration" button (looks like a blank file with a +).

  1. Enter any name you'd like in the "Name:" text box.

  1. Next to the "Project:" text box, click the "Browse" button and select the "SearchEngine" project.

  1. Next to the "Main class:" text box, click the "" button and select "Driver" from the list. At this point, your setup should look like this:

      ![Screenshot]({{ "/images/eclipse-project-driver-run-main.png" | relative_url }}){: style="width: 600px;"}

  1. Click on the "Arguments" tab. Enter the following into the "Program arguments" text area:

      ```
      -text input/text/simple/hello.txt -index actual/index-simple-hello.json
      ```

      ...or if you are on Windows:

      ```
      -text input\text\simple\hello.txt -index actual\index-simple-hello.json
      ```

      This will run `Driver` with the same arguments as the first project 1 test.

  1. **This next part is really important!** Remember, all of the test files are in a SEPARATE repository. Change the "Working directory:" setting to the "Other:" choice.

  1. Click the "Workspace..." button and select the "SearchEngineTests" project. At this point, your setup should look like this:

      ![Screenshot]({{ "/images/eclipse-project-driver-run-arguments.png" | relative_url }}){: style="width: 600px;"}

  1. Click the "Apply" and "Run" buttons.

</div>
</details>

<br/>
You can keep running this same "Run Configuration" while debugging. If you are failing a specific JUnit test, you can copy/paste the arguments used by the test (provided in the failure output) to debug your code.

### Running JUnit Tests

You must use the [JUnit 5](https://junit.org/junit5/) tests provided with the [project-tests]({{ site.data.info.links.github.link }}/project-tests) repository to determine if your project is meeting the required functionality. The suite of tests for each project are given by the `Project#Test.java` files in the [src]({{ site.data.info.links.github.link }}/project-tests/tree/main/src/test/java) subdirectory. For example, the tests for [Project 1](project-1.html) are provided by the [Project1Test.java]({{ site.data.info.links.github.link }}/project-tests/blob/main/src/test/java/Project1Test.java) file.

While you are initially working on the project, **focus on individual tests** or individual groups of tests. There is no need to run all of the tests every time; in fact this can make debugging harder! See the [Homework Testing](/guides/homework/homework-testing.html#running-individual-tests) guide for different ways you can run individual JUnit tests. Here is an example run configuration:

![Screenshot]({{ "/images/project-eclipse-junit-run-configuration.png" | relative_url }}){: style="width: 600px;"}

**Pay attention to the test output.** The output tells you where to find the actual and expected output files and what caused the test to fail. It also tells you the arguments that were passed to your `Driver` class, which is helpful for debugging. The full output, which can be copied to the console for easy copying/pasting using the <img src="{{ "eclipse-copy-junit-output-to-console.png" | prepend: "/images/" | relative_url }}" style="height: 16px; vertical-align: middle;"> button, includes the following text:

```
Actual File:
    actual/index-simple-hello.json
Expected File:
    expected/index/index-simple/index-simple-hello.json
Arguments:
    -text input/text/simple/hello.txt -index actual/index-simple-hello.json
Message:
    Difference detected on line: 2.
```

This gives the actual arguments passed to `Driver` by the test, the actual and expected files being compared, and where the first difference was detected. You can use the [Compare Editor](http://help.eclipse.org/2020-06/topic/org.eclipse.platform.doc.user/reference/ref-25.htm?cp=0_4_4_1_2) in Eclipse to compare the files side-by-side for debugging, or use the [Run Configurations](#run-configurations) in Eclipse to enter the same arguments manually.

<i class="fas fa-exclamation-triangle"></i>
To save space, the tests automatically delete your output files if they match the expected output. Only output files for failing tests will be kept.
{: .notification }

### Running Maven

Most of the time, if you are passing the tests locally you will also pass them remotely. However, there are slight differences between how the tests are run by Eclipse and how they are run by Github Actions.

If you want to test out the same approach used by Github Actions, you have to use Maven to run the tests instead of the JUnit interface in Eclipse.

<details>
<p><summary>View Details</summary></p>

<div markdown=1>

Here is a screenshot of the run configuration you must create:

![Screenshot]({{ "/images/eclipse-maven-project-configuration.png" | relative_url }})

Follow these steps to create this run configuration:

1. Go to the "Run" menu in the menubar at the top of Eclipse and select "Run Configurations..." from the dropdown.

1. Click on the "Maven Build" category in the left view pane and click the "New Configuration" button (looks like a blank file with a +).

1. Enter any name you'd like in the "Name:" text box.

1. Under the "Base directory:" text box, click the "Workspace" button and select the "SearchEngine" project.

1. Enter the following into the "Goals:" text box:

    ```
    clean compile test-compile test
    ```

    The `clean` goal removes all previously-compiled class files. The `compile` goal compiles all of the main source code in the `main` directory and the `test-compile` goal compiles all of the test source code in the `test` directory of the `project-tests` repository. Finally, the `test` goal runs the JUnit tests found in the `test` directory.

1. Next to the "Parameter Name" list, click the "Add..." button to add a parameter. Enter `test` for the "Name:" text box and `Project#Test*` for the "Value:" textbox, where `#` is the project number. For example, enter `Project1Test*` for Project 1. Click the "OK" button when done.

1. [OPTIONAL] Click the "Add..." button to add another parameter. Enter `excludedGroups` and `none() | !verify` for the name and value. This tells Maven to run all tests except those without tags, or those that don't have the `verify` tag. Or, in other words, it only runs the tests tagged with `verify`, which finishes much faster than running all of the tests. *This can be skipped if you want to run all of the tests regardless.*

1. Ignore the red `SLF4J:` output at the beginning. Look for output similar to:

    ```
    [INFO] Running Project1Test$A_OutputTest

    Running: actual/index-text.json...
    Elapsed: 3.085000 seconds
    [INFO] Tests run: 1, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 3.336 s - in Project1Test$A_OutputTest
    ```

    Make sure you always see `Failures: 0`. Otherwise, scroll up in the console output to see which tests failed.

</div>
</details>

<br/>
These steps are really only required for fine-grained debugging and can be skipped most of the time.

## Testing Remotely
{: .page-header }

You must test your code remotely before you can earn credit for the functionality of your project and before you can sign up for a code review appointment.

This process begins by creating a release on Github. This will trigger the Github Action that verifies your project functionality.

### Creating Releases

Creating releases will familiarize you with [**versioning**](https://en.wikipedia.org/wiki/Software_versioning) your code.

  1. After passing all of the tests locally and pushing your latest commits to Github, follow the [Creating Releases](https://help.github.com/articles/creating-releases/) steps to draft a new release of your project code on Github.

  2. You must choose a "tag" or the version number you are going to assign to your code at this stage. Out in the "real world" you will likely use [semantic versioning](https://semver.org/), which we will roughly mimic in class.

      Specifically, you must name your release `v#.#.#` where the first `#` is the project number (1, 2, 3, or 4), the second `#` is the number of code reviews you've had for that project, and the last `#` is the number of patches/fixes you released since the last code review for that project.

      For example, your first release should be `v1.0.0` because it is for project 1, you have not had any code reviews yet, and you have not had any other releases yet. If your code does not pass the tests remotely, then you have to fix your code and re-release your project as `v1.0.1` since you now have 1 prior release. After your first code review, the next release will be `v1.1.0` (notice how the last number reset to 0).

      The release `v2.3.4` means this release is for project 2, you have had 3 code reviews for project 2 so far, and this is the 4th release since your last code review of project 2. (It also means there must be a prior `v2.3.3` release made before this one.)

  4. Click the "Publish release" button. You can leave the title and description blank.

You can see a [sample release]({{ site.data.info.links.github.link }}/project-template/releases) on the template repository.

**Generally, you should not delete releases even if they are not passing tests.**

### Verification Action

Pending

### Debugging Failures

Pending

{% comment %}

### Verification Script

Once you have created a release, the verification script on Github Actions will automatically trigger.

You can find the results in the "Actions" tab on Github. Click on the release title to go to that run and view details. The first "Verify Project" link will summarize the results, the second will show details on each step in the run.

The action performs these steps:

  1. It will check if you have the latest version of the verification action. If this fails, you will see an error similar to:

      "Update your "/verify.yml" file from the attached artifact."  
      "Your Github Action verify.yml is out of date."
      {: .has-text-danger }

      To fix, see the [Outdated Verification Script](#outdated-verification-script) section below.

  1. It will attempt to parse the version number. If the version number is not in the right format (`v#.#.#`), then it will fail with an error message similar to:

      "The release tag is in an unexpected format."
      {: .has-text-danger }

      That includes having a *lowercase* `v` at the start! If this happens, you will have to edit the release version or create a new release to continue.

  1. It will attempt to setup the environment for testing. This includes downloading your code, setting up Java, and setting up fresh test files. If this part fails, please post on Piazza with a link to the action run.

  1. It will compile the project and test code. If this step fails, look at the log. Depending on your Eclipse configuration, the `javac` compiler might be using more strict compile settings when it comes to warnings and Javadoc than your system.

  1. It will run the tests associated with the release version. This might take awhile. You can watch as it progresses if you want.

  1. It will generate a test report regardless of whether the tests passed or failed. These report files are available in the "Artifacts" section. See the [Generated Reports](#generated-reports) section below for details.

  1. It will output the result of the tests. If the tests succeed, you will see a message like:

      ![Screenshot]({{ "/images/verify-project-passed.png" | relative_url }}){: style="width: 500px;"}

      If the tests failed, you will need to look at the logs and the reports to debug what happened. We can help as well if you post a link directly to the action run on Piazza!


If everything passes and you want credit for passing the functionality, follow the [project grading](project-grading.html) steps to notify the teacher assistant.

###### Generated Reports

As long as the verification action was able to compile the code, it will generate reports from running the tests (regardless if the tests pass or fail). These can be helpful for debugging. There is an HTML version:

![Screenshot]({{ "/images/sample-report.png" | relative_url }}){: style="width: 500px;"}

There are also raw text reports that have additional information, such as:

```
-------------------------------------------------------------------------------
Test set: Project1Test$A_IndexOutput
-------------------------------------------------------------------------------
Tests run: 26, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 10.001 s - in Project1Test$A_IndexOutput
```

However, the raw logs will have the most information. You can download those logs from the action run details (click on the second "Verify Project" link).

###### Outdated Verification Script

If the verification action fails with the message, "Your Github Action `verify.yml` is out of date," then you need to push the latest version to your repository before you can continue.

![Screenshot]({{ "/images/verify-action-outdated.png" | relative_url }}){: style="width: 500px;"}

The latest version will be included under the "Artifacts" section (see above). Download that file and place it in the `.github/workflows` folder of your repository. You might need to show hidden files on your system to see the `.github` folder.

Push the changes to your repository. Once that is done, click the "Re-run jobs" button near the top right corner (see above). If this fails again, try creating a new release. This should trigger the Github Action to run again with the latest version.
{% endcomment %}
