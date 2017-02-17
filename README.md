#Testing Guide for Developers

##Guiding principles
(1) use the [Testing Pyramid](https://www.mountaingoatsoftware.com/blog/the-forgotten-layer-of-the-test-automation-pyramid) - you should have many more unit tests than UI tests

![alt text](http://www.alwaysagileconsulting.com/blog/wp-content/uploads/2015/11/End-To-End-Testing-Considered-Harmful-Labelled-Test-Pyramid.png "Testing Pyramid")

Unit tests are good because:
* they are fast
* they are reliable
* they isolate failures

Acceptance tests may be UI tests, but end-to-end tests always are.
Minimise UI tests! They are expensive to write, time consuming to run, and sometimes non-deterministic (ie there are often false positives) and brittle (easily broken). They can be useful but we shouldn't have many of them. If they fail and expose a bug, unit test(s) should be written to address the failing scenario first.

Google reported how end-to-end testing had the following problems:
* difficult to find root cause of problems
* partner failures and lab failures ruined the test results 
* many smaller bugs were hidden behind bigger bugs. 

Ease of fixing bugs (mean time to repair) should be prioritised over having fewer test failures. 




## Interesting reading

[Google blog - just say no to more end to end tests](https://testing.googleblog.com/2015/04/just-say-no-to-more-end-to-end-tests.html)
[End to end testing considered harmful](http://www.alwaysagileconsulting.com/articles/end-to-end-testing-considered-harmful/)
[Yet another testing pyramid](https://watirmelon.blog/2011/06/10/yet-another-software-testing-pyramid/)
[Ice Cream Cone anti-pattern](https://watirmelon.blog/2012/01/31/introducing-the-software-testing-ice-cream-cone/)
