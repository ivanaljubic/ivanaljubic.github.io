## Hi

This repo contains the source for Prof. Ivana's website hosted [here](https://rishikeshavan.github.io/prof-ivana-site/).

The different sections `Publications`, `Talks`, `Teaching`, `Projects` and `CV` are displayed on the top of the page. The `Publications`, `Talks` and `Projects` lists out the various titles and clicking on each of them will take you to its own page with additional details about it.

## Updating Content

Please follow the below steps to update/add new content:

#### 1. About

The homepage can be updated by editing the content in [about.md](_pages/about.md).

#### 2. Publications

To add a new publication:

- Add a `.md` file to the [\_publications](_publications) folder.
- The name of the file must be in the format of `yyyy-mm-dd-title-of-the-publication.md`. This is important for the order of displaying the publications
- The file needs to have the following values in at the beginning and these determine the `properties` of the file

```
---
title: "Title of the publication"
collection: publications
type: refereedconf/journal/reportorsubmittedpaper/editedbook/bookchapter/phdthesis
author: "Authors of the publication"
permalink: /publication/yyyy-mm-dd-title-of-the-publication
date: yyyy-mm-dd
venue: "Journal of publication, Vol, Pages"
---
```

- `type` should be one of the values mentioned and accordingly the publication will be displayed under the specific section in the `Publications` Page
- `permalink` should always start with `/publication/` followed by the name of the file without the `.md` externsion
- After this section, any content related to the publication can be added and they will be displayed in the repective page of the publication
- New `.pdf` files for the publications must be added to [docs/publications](docs/publications/) and referenced accordingly in the respective publication's `.md` file

To edit an existing publication:

- Identify the assosciated `.md` file in the [\_publications](_publications) folder.
- As much as possible, avoid editing the first section of the file where its properties are mentioned unless you are sure of the changes being made
- Any addition/deletion of content can be made after the properties of the file.

#### 3. Talks

To add a new talk:

- Add a `.md` file to the [\_talks](_talks) folder.
- The name of the file must be in the format of `yyyy-mm-dd-title-of-the-talk.md`. This is important for the order of displaying the talk
- The file needs to have the following values in at the beginning and these determine the `properties` of the file

```
---
title: "Title of the talk"
collection: talks
category: "Presentation"
type: intlpresentation/plenarykeynote/othertalk
permalink: /talks/yyyy-mm-dd-title-of-the-talk
venue: "Conference name of the talk"
date: yyy-mm-dd
location: "Geo Location of the talk"
---
```

- `type` should be one of the values mentioned and accordingly the talk will be displayed under the specific section in the `Talks` Page
- `permalink` should always start with `/talks/` followed by the name of the file without the `.md` externsion
- After this section, any content related to the Talk can be added and they will be displayed in the repective page of the talk
- New `.pdf` files for the talks must be added to [docs/publications](docs/publications/) and referenced accordingly in the respective talk's `.md` file

To edit an existing talk:

- Identify the assosciated `.md` file in the [\_talks](_talks) folder.
- As much as possible, avoid editing the first section of the file where its properties are mentioned unless you are sure of the changes being made
- Any addition/deletion of content can be made after the properties of the file.

#### 4. Teaching

Editing the `Teaching` page is straight-forward and can be done in the [teaching.md](_pages/teaching.md) file. Whatever content is present in this file will be directly reflected in the `Teaching` page.

#### 5. Projects

To add a new project for which you will be providing the content:

- Add a `.md` file to the [\_portfolio](_portfolio) folder.
- The name of the file must be in the format of `title-of-the-project.md`.
- The file needs to have the following values in at the beginning and these determine the `properties` of the file

```
---
title: "Title of the project"
excerpt: "Short description about the project"
collection: portfolio
---
```

- New files for the project, `.pdf` or code files, must be added to [docs/publications](docs/publications/) under a seprate folder and referenced accordingly in the respective project's `.md` file

- After this section, any content related to the Project can be added and they will be displayed in the repective page of the Project

To add a new project that should be redirected an external page:

- Add a `.md` file to the [\_portfolio](_portfolio) folder.
- The name of the file must be in the format of `title-of-the-project.md`.
- The file needs to have the following values in at the beginning and these determine the `properties` of the file

```
---
title: "Title of the project"
excerpt: "Short description about the project"
link: 'https://external-link.com'
collection: portfolio
---
```

- Clicking on this project in the `Projects` page will redirect to the external link

To edit an existing project:

- Identify the assosciated `.md` file in the [\_portfolio](_portfolio) folder.
- As much as possible, avoid editing the first section of the file where its properties are mentioned unless you are sure of the changes being made
- Any addition/deletion of content can be made after the properties of the file.

#### 6. CV

Editing the `CV` page is straight-forward and can be done in the [cv.md](_pages/cv.md) file. Whatever content is present in this file will be directly reflected in the `CV` page.

#### 7. Misc changes

Other changes like Email, Google Scholar link and updating the picture can be done in the [\_config.yml](_config.yml) file. Please note that, this is the master file that also contains other properties that control how the project is built and changes to them might affect the site.

All pictures are present in [images](images) folder.

The original `README.md` file is located [here](docs/og-README.md).

This [link](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax) provides a good base to understand editing `.md` files
