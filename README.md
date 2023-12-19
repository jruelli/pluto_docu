# PLUTO DOCS
![Build Status](https://gitlab.com/pluto_ipek/pluto_docu/badges/master/pipeline.svg)

The generated website can be visited here: https://pluto_ipek.gitlab.io/pluto_docu/

---

Pluto Robot [sphinx] documentation website using GitLab Pages.

Learn more about GitLab Pages at https://about.gitlab.com/product/pages/ and the official
documentation https://docs.gitlab.com/ee/user/project/pages/.

---

<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->
**Table of Contents**  *generated with [DocToc](https://github.com/thlorenz/doctoc)*

- [GitLab CI](#gitlab-ci)
- [Requirements](#requirements)
- [Building locally](#building-locally)
- [GitLab User or Group Pages](#gitlab-user-or-group-pages)
- [Troubleshooting](#troubleshooting)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

## GitLab CI

This project's static Pages are built by [GitLab CI][ci], following the steps
defined in [`.gitlab-ci.yml`](.gitlab-ci.yml):

## Requirements

- [Sphinx][]
- sphinx_rtd_theme

## Building locally

Please notice that there are various ways to get the required software running. 
We chose the one that looks the most straight-forward to us.  
Feel free to contact us in the case there are problems with the installation or if you find improvements.

Using windows: To work locally with this project, you'll have to follow the steps below:

1. Fork, clone or download this project
2. Install chocolatey (https://chocolatey.org/install)
3. Install make `choco install make`
4. [Install][sphinx] Sphinx `choco install sphinx`
5. Install sphinx_rtd_theme & sphinx-autobuild `pip install sphinx_rtd_theme sphinx-autobuild`
6. Generate the documentation (chose your desired option): `make`

The generated HTML will be located in the location specified by `conf.py`,
in this case `_build/html`.

## GitLab User or Group Pages

To use this project as your user/group website, you will need one additional
step: just rename your project to `namespace.gitlab.io`, where `namespace` is
your `username` or `groupname`. This can be done by navigating to your
project's **Settings**.

Read more about [user/group Pages][userpages] and [project Pages][projpages].

## Troubleshooting

No issues reported yet.

---

Forked from https://gitlab.com/pages/sphinx

Which is forked from:

Forked from https://gitlab.com/Eothred/sphinx

Learn more about GitLab Pages at https://about.gitlab.com/product/pages/ and the official
documentation https://docs.gitlab.com/ee/user/project/pages/.

[ci]: https://about.gitlab.com/product/continuous-integration/
[userpages]: https://docs.gitlab.com/ee/user/project/pages/getting_started_part_one.html#user-and-group-website-examples
[projpages]: https://docs.gitlab.com/ee/user/project/pages/getting_started_part_one.html#project-website-examples
[sphinx]: http://www.sphinx-doc.org/
