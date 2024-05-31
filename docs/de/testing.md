Software testing helps to achieve and maintain high quality software. Every
non-trivial software has bugs. Fixing bugs drives your code further away from
triviality, which again enforces new bugs. To minimise the bug-density of our
code, testing should be done for various reasons and at different levels.

Typically a test suite is implemented: a collection of small functions each
testing a specific functionality of the code. Developers and users may run the
test suite to check the integrity and correctness of the software.

- Unit tests help to find unintended behaviour while designing
  new functionality.
- Regression tests ensure that changes do not break things.
- Linter checks assist in creating clean code.
- Automatic integration tests protect against human error.
- Deployment tests help to find environment and dependency problems, and changes thereof after system upgrades.

Implement an adequate test suite for your project and explain what and how
tests should be run in the file named `CONTRIBUTING` in your project directory.

If your software needs data to run, provide test data. If your test data is
bigger than a few MB, you should not include it in the repository. Store it
somewhere else and make a reference to the data or provide a download script.
