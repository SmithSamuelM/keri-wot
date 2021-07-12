# KERI IETF Draft Specification



## Licenses

The legal structure of this repository with respect to the licening of its
associated contributions follow GitHub's Open Source Guide reccomendations for
open source standards and code. These may be found [here](https://opensource.guide/legal/)

All software and documentation in this repository is *Copyright 2021 KERI Contributors* and is
 *Licensed under the Apache License, Version 2.0 (the "License")* [here](LICENSE);
 you may not use the software or documentation in this repository except in compliance with the License.
You may obtain a copy of the License at [Apache2](http://www.apache.org/licenses/LICENSE-2.0).
Unless required by applicable law or agreed to in writing, software distributed
under the License is distributed on an "AS IS" BASIS.

Contributers of contributions to this repository as defined in the
[Apache2](http://www.apache.org/licenses/LICENSE-2.0) license are bound by the
Developer Ceritificate of Origin v1.1 (DCO 1.1) which may be found
[here](https://developercertificate.org)

As a GitHub repository, all contributions to this repository are also bound by
the GitHub inbound=outbound policy. This may be found under Section 6
[here](https://docs.github.com/en/github/site-policy/github-terms-of-service#6-contributions-under-repository-license)


##  Documentation and Specification Template
This repo is a [GitHub Repo Template][1] for creating GitHub repositories.
Newly generated repos will contain all the necessary code for using MkDocs.


## Purpose



## Usage


### Prime and clone a new repository
1. Generate a new repository from this template repository (see [GitHub docs][7]).
2. Clone the new repository (see [GitHub docs][8]).

### Pick a theme style
This repo supports the use of a *Specification* styled theme. In all other cases,
a *General Documentation* styled theme is provided.

1. Open the repository using your favorite IDE .
2. Apply your style selection

| Style | Configuration Action | View Demo |
| --- | --- | --- |
| _General Documentation_ | Move the `mkdocs.spec.yml` file, which is located
at the root of the repo, to the `archive` folder.
| _Specification_ | Move the `mkdocs.yml` file to the `archive` folder, and
rename `mkdocs.spec.yml` to `mkdocs.yml`.

### Configure MkDocs

[MkDocs][3] uses a [YAML file][13] to configure the operational properties for
the document generator.

1. Open the repository using your favorite IDE .
2. Edit the `mkdocs.yml` file and find the sections depicted below:

    ```
    # Project information
    site_name: Trust over IP – General Template
    site_url: https://trustoverip.github.io/mkdocs-material/
    site_author: Jane Doe
    site_description: >-
      Trust over IP Foundation template for general documentation
      and technical specification using Material for MkDocs

    # Repository information
    repo_name: trustoverip/mkdocs-material
    repo_url: https://github.com/trustoverip/mkdocs-material

    # Content Generator Settings
    docs_dir: 'content'
    site_dir: 'html'
    ```

3. Update the following settings:

    1. `site_name`: Set to ToIP Deliverables name using the naming convention `<TypeIndicator><4digitID>: <DeliverableName>`. For example,  _BP000: Utility Selection Criteria_.

    2. `site_url`: Set to the GitHub Pages URL that will serve up this new repo site.

    3. `site_author`: Set to the sponsoring ToIP WG. For example, _ToIP Governance Stack WG_.

    4. `site_description`: Set to a short description of the ToIP Deliverable being documented by this repo.

    5. `repo_name`: Set using name of the new GitHub repo.

    6. `repo_url`: Set using the URL of the new GitHub repo.

    7. `docs_dir`: Enter the preferred directory name for where the content for this document/spec will reside.

    8. `site_dir`: Enter the preferred directory name for where the static HTML pages will be generated from Markdown files.

    9. `extra.title`: Set to ToIP Deliverables name using the naming convention `<TypeIndicator><4digitID>: <DeliverableName>`. For example,  _BP000: Utility Selection Criteria_.

### Configure Makefile

1. Open the repository using your favorite IDE (i.e. [Visual Studio Code][10], [Atom][11]).
2. Edit the `Makefile` file and find the variables depicted below:

    ```
    REPO_NAME ?= mkdocs-material
    UPSTREAM_REPO ?= https://github.com/trustoverip/mkdocs-material.git
    DEV_IMAGE ?= trustoverip/mkdocs-material-devenv
    PANDOCS_IMAGE ?= trustoverip/pandocs-devenv
    DEV_SITE_PORT ?= 7500
    DEV_HOST_DIR ?= host_mkdocs
    PUB_HOST_DIR ?= host_pandocs
    PUBLISH_DIR ?= publish
    ```

3. Update the following settings:

    1. `REPO_NAME`: Provide the GitHub repository name.
    2. `UPSTREAM_REPO`: Set using the GitHub Repo Clone URL.
    3. `DEV_SITE_PORT`: Pick a port that will be used for the local test server: _https://localhost:8080_

### Update Readme
1. Open the repository using your favorite IDE (i.e. [Visual Studio Code][10], [Atom][11]).
2. Based on the type of deliverable that will be associated with this new repo, copy the appropriate `template` from the [templates folder within the trustoverip/deliverables repo][15] to `./archive/SUGGESTED_OUTLINE.md`.
3. Move `README.md` to the `archive` folder. Rename it to `ORIGINAL_INSTRUCTIONS.md`.
4. Rename `DOC_README.md` to `README.md`
5. Update `README.md` accordingly.

    1. At the top of your file modify the _title_ so it is in the form:

        ```
        <TypeIndicator><4digitID>: Friendly Version of Your Title.
        ```

    2. Refer to the _Contribution Options_ of the [ToIP Deliverables Portal][14].


