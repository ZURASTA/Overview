Contributing
============

These are general purpose guidelines that our projects can follow, it is not required that all project's follow this approach. If contribution differs from this guideline for a particular project, make sure to include a `CONTRIBUTING.md` document to outline the process for that specific project.

Pre-existing Project
--------------------

The process for contributing is as follows:

1. Fork the project you wish to contribute to.
2. Make a new branch for your contribution. If it's a fix for a task listed on a waffle board, structure it as `#[issue]-[name]`, e.g. `#2-fix-stuff`. Or reference this [guide](https://help.waffle.io/automatic-work-tracking/auto-work-tracking-basics/recommended-workflow-using-pull-requests-automatic-work-tracking) for more information.
3. Once your branch is ready, submit a pull request. If it's a fix for a task listed on a waffle board, and it is the only fix needed, you may use a close command to close the related issue.
4. The pull request will be reviewed, and merged if it looks good. Otherwise it will be discussed and either required to be fixed up (in order to merge), or closed.

For giving feedback or input on a project, either comment on the specific issue or pull request in question, or create a new issue if it's a new point.


New Project
-----------

Contributing to a new project should be more flexible until it's deemed necessary to follow a process mentioned above. Ideally the branches on the remote (ZURASTA origin/upstream) should be kept clean, so it is easier to better utilise branches on that repo for other things. Though these branches can be retired at any time (in the github settings), so it's not a problem if that does happen.

New projects will likely want to have their labels setup, which can be achieved by running ([org-labels](https://github.com/repo-utils/org-labels)): `org-labels standardize ZURASTA/:repo ZURASTA/Overview`. Or alternatively creating a custom label spec.
