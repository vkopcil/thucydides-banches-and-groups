thucydides-banches-and-groups
=============================

This project is here to demostrate usage of surefire plugin test categories with thucydides runner

Project is based on thucydides-simple-archetype v 0.9.262.
Instead of failsafe plugin I have to use surefire, which means tests are executed in test phase.
To eliminate any known and solved bugs in surefire plugin itself, I've updated it's version.
You can use 
<code>mvn test thucydides:aggregate</code>
to run tests and generate report.
I've created three test classes from original one, to demonstrate batch selection.

In master branch 
you can see test method selection works using categories. All test are run by same executor.

In BATCHES branch
there is setting which should run only single test class, using batches, depending on current value of thucydides.batch.number.
Without test categories it works as expected. But with categories, all tests run in last batch.


