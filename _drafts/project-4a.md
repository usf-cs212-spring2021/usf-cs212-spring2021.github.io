---
title: Project 4 Web Crawler
navbar: Guides
layout: guides
key: 2.5

tags:
  - text: 'New'
    type: 'is-primary'

assignments:
  - text: 'Project 4 Web Crawler'
    link: 'https://usfca.instructure.com/courses/1594619/assignments/6987891'

---

For this project, you will extend your [previous project](project-3.html) to create a multithreaded web crawler using a work queue that builds the inverted index from a seed URL.

**This writeup is for the web crawler functionality only.** See the general [Project 4 Writeup](project-4.html) for more details.

## Functionality

The core functionality of your project must satisfy the following requirements:

  - Maintain the functionality of the [previous project](project-3.html).

  - Process additional command-line parameters to support the functionality of this project. See the [Input](#input) section for specifics.

  - Support the same output capability as before. See the [Output](#output) section for specifics.

  - Add support to build the inverted index from a seed URL instead of a directory using a web crawler. The web crawler must be multithreaded using a work queue such that each URL that must be crawled is handled by a single worker thread.

  - To avoid a infinite crawl, the web crawler should parse up to a fixed limit of unique URLs as specified by a command-line argument. If the argument is missing, the crawler should parse only the provided link by default.

  - The web crawler must download webpages over HTTP or HTTPS when crawling as follows:

    - Use sockets, NOT use the URL class to download the HTML. However, your code may use the URL class to parse and clean URLs (see the Relative URLs and Unique URLs sections below).

    - If the HTTP response status was a redirect, follow the redirect up to a limit of 3 redirects (to avoid an infinite redirect loop).

      The content at the end of this process will be assigned to the original URL. For example, the URL [~cs212/redirect/one](https://www.cs.usfca.edu/~cs212/redirect/one) eventually redirects to [~cs212/simple/hello.html](https://www.cs.usfca.edu/~cs212/simple/hello.html). However, the web crawler will associate the content of [~cs212/simple/hello.html](https://www.cs.usfca.edu/~cs212/simple/hello.html) with the original link [~cs212/redirect/one](https://www.cs.usfca.edu/~cs212/redirect/one) instead.

    - Do *not* add HTML from web pages unless the HTTP response status code was `200 OK` and the content type is HTML.

    It is acceptable to read the entire web page into memory at once.

  - Convert all processed URLs to a consistent absolute form (remove fragments, convert relative URLs to absolute URLs, etc.) and do not process the same URL more than once. For example, if you already processed <https://www.cs.usfca.edu/~cs212/guten/1400-h/1400-h.htm> and encounter <https://www.cs.usfca.edu/~cs212/guten/1400-h/1400-h.htm#link2HCH0020>, you should not re-process this URL and it should not count towards the total.

  - Use a breadth-first approach to crawling URLs. For example, suppose the seed URL has 49 or more URLs on the page. The first 49 URLs on the seed page (plus the seed URL itself) should be a part of the crawl. *If you use the work queue correctly, then crawling will automatically be breadth-first.*

  - For each normalized unique URL that must be crawled (up until the limit):

    - Each worker thread should be responsible for parsing a single link.

    - Remove any HTML block elements that should not be considered for parsing links, including the `head`, `style`, `script`, `noscript`, and `svg` elements.

    - Parse all of the URLs remaining on the page and add to the queue of URLs to process as appropriate. (You must do this before you remove the other HTML tags.)

    - Remove all of the remaining HTML tags and entities.

    - Clean, parse, and stem the resulting text to populate the inverted index in the same way plain text files were handled in previous projects.

  - Your code may *NOT* use any of the classes in the `java.util.concurrent` package.

The functionality of your project will be evaluated with various JUnit tests. Please see the [Testing](#testing) section for specifics.

## Input

Your main method must be placed in a class named `Driver`. The `Driver` class should accept the following **additional** command-line arguments:

  - `-url seed` where `-url` indicates the next argument `seed` is the seed URL your web crawler should initially crawl to build the inverted index.

      If the `-url` flag is provided, your code should **enable multithreading** with the default number of worker threads even if the `-threads` flag is not provided.

  - `-max total` where `-max` is an *optional* flag that indicates the next argument `total` is the total number of URLs to crawl (including the seed URL) when building the index. Use `1` as the default limit if this flag is not provided or is not provided with a valid value.

The command-line flag/value pairs may be provided in any order, and the order provided is not the same as the order you should perform the operations (i.e. always build the index before performing search, even if the flags are provided in the other order).

Your code should support all of the command-line arguments from the [previous project](project-3.html) as well.

## Output

The output of your inverted index and search results should be the same from the [previous project](project-3.html). As before, you should **only generate output files if the necessary flags are provided**.

## Testing

You must pass 100% of the tests in the `Project4Test.java` group of JUnit tests. This test group does NOT include the long-running runtime tests that benchmark your single- versus multi-threading code for the [previous project](project-3.html). However, it does make sure your new web crawler code runs faster with 3 threads versus 1 thread.

<article class="message is-info">
  <div class="message-body">
    <i class="fas fa-info-circle"></i>&nbsp;These tests are only for the web crawler functionality. The search engine functionality will be verified during the final code review appointment, not via automated system tests.
  </div>
</article>

## Hints

It is important to develop the project iteratively. One possible breakdown of tasks are:

  - Get `log4j2` working and start adding debug messages in your code. Once you are certain a class is working, disable debug messages for that class in your `log4j2.xml` file.

  - Several homework assignments are directly useful for this project, but you will need to make them work together. Specifically, use your [`HtmlFetcher`](https://github.com/usf-cs212-fall2020/homework-HtmlFetcher-template) to download HTML, parts of your [`HtmlCleaner`](https://github.com/usf-cs212-fall2020/homework-HtmlCleaner-template) to remove block elements from that HTML, your [`LinkParser`](https://github.com/usf-cs212-fall2020/homework-LinkParser-template) to parse out all of the remaining links, and finally the [`HtmlCleaner`](https://github.com/usf-cs212-fall2020/homework-HtmlCleaner-template) again to strip out the remaining HTML. From there, your [`TextFileStemmer`](https://github.com/usf-cs212-fall2020/homework-TextFileStemmer-template) homework might have method you could use for stemming the remaining text into words and adding to your inverted index.

  - Outside of the relevant homework and lecture classes, there is likely only one new class (a web crawler class) required for this project. However, you must be careful to properly multithread and synchronize in this class!

The important part will be to test your code as you go. The JUnit tests provided only test the entire project as a whole, not the individual parts. You are responsible for testing the individual parts themselves.
