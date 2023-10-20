# Details on weekly releases

Releases for your projects were discussed Lecture 5. Here we give detailed information in one location.

## What is a release?

Releases are deployable software iterations you can package and make available for a wider audience to download and use. You can create a release to package software, along with release notes and links to binary files. Releases are based on Git tags (versions), which mark a specific point in your repository's history. Read more about releases in the official [Github Documentation](https://docs.github.com/en/repositories/releasing-projects-on-github/about-releases).

Making releases is common practice for packages: e.g. [numpy v1.21.3](https://github.com/numpy/numpy/releases/tag/v1.21.3)

## Release schedule

Every release apart from v8 should be released at *10am on Mondays* (before the lecture) according to the following schedule:

|	          	|	Date	    |	Topic	| Software version | Software releases |  Grading / Feedback |
| :---        |    :---  |    :--- | :--- | :--- | :--- |
|	0	|	18/09/2023	|	Public holiday	|
|	1	|	25/09/2023	|	Python introduction I	|
|	2	|	02/10/2023	|	Python introduction II	|
|	3	|	09/10/2023	|	VS Code |
|	4	|	16/10/2023	|	Git	and GitHub |
|	5	|	23/10/2023	|	Project introduction	| v1 | |
|	6	|	30/10/2023	|	Functionify	| v2 | v1 |  |
|	7	|	06/11/2023	|	Visualization and documentation	| v3 | v2 | code review (API) |
|	8	|	13/11/2023	|	Unit-tests, functional tests	| v4 | v3 | |
|	9	|	20/11/2023	|	Code refactoring	| v5 | v4 | graded (tests) |
|	10	|	27/11/2023	|	Profiling and code optimization	| v6 | v5 | code review  |
|	11	|	04/12/2023	|	Object oriented programming	| v7 | v6 | graded (speed)|
|	12	|	11/12/2023	|	Model analysis and project report | v8 | v7 | code review (OO) |
|	13	|	18/12/2023	|	Wrap up	|  | v8 | graded (project) |


## Project release rules

During project development, students are expected to regularly release new versions of their code according to the [class schedule listed above](#release-schedule). Selected releases will be subject to code review and grading as part of the course assessment as indicated in the table.

Use versioning for making your release. The only relevant rules for the class are:

- make major releases per week, e.g. `v1.0`
- if you find a bug/error after the release date, do not delete your release, but release a minor/patch release, e.g. `v1.1` with a description: `fixing xyz bug`. That way we know that you didn't miss the original deadline and later improved your code. We will always grade/review the latest available release.

However, if you're interested you can find more information about versioning in Python [here](https://py-pkgs.org/07-releasing-versioning.html).


## How to create and manage a release?

You can create new releases with release notes, @mentions of contributors, and links to binary files, as well as edit or delete existing releases.

To create a release follow the official [Github Documentation](https://docs.github.com/en/repositories/releasing-projects-on-github/managing-releases-in-a-repository).

With `git` one can easily [checkout specific tags](https://stackoverflow.com/questions/791959/download-a-specific-tag-with-git) in the following way:
- list the tags (```git tag -l```)
- `git checkout tags/<tag_name>`

## How should your project look?

We provide an example project for you to compare. Please check it out at [EPFL-BIO-210/demo-project](https://github.com/EPFL-BIO-210/demo-project).

Feel free to send us pull-requests if you want to suggest changes. You can check out the releases of this project [here](https://github.com/EPFL-BIO-210/demo-project/releases)!
