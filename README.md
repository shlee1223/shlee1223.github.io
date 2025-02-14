OmniOne OpenDID GitHub Pages
==

Welcome to the OmniOneID GitHub Pages repository. <br>
This repository contains the source code, documentation, and related resources for OmniOneID GitHub Pages.

## Folder Structure
Overview of the major folders and documents in the project directory:

```
OmniOneID.github.io
├── CLA.md
├── CODE_OF_CONDUCT.md
├── CONTRIBUTING.md
├── LICENSE
├── MAINTAINERS.md
├── README.md
├── dependencies-license.md
├── index.html
└── assets
    └── css
    └── favicon
    └── images
    └── vendor
```

<br/>

Below is a description of each folder and file in the directory:

| Name                             | Description                                     |
| -------------------------------- | ---------------------------------------- |
| CLA.md                           | License agreement for open-source contributions              |
| CODE_OF_CONDUCT.md               | Code of conduct for contributors                |
| CONTRIBUTING.md                  | Contribution guidelines and procedures          |
| LICENSE                          | License                                         |
| MAINTAINERS.md                   | Guidelines for project maintainers              |
| README.md    | Overview and instructions for the source code                   |
| dependencies-license.md          | Licenses for the project’s dependency libraries |
| index.html          | Main HTML source for GitHub Pages |
| assets                             | Assets folder                                   |
| ┖ css                            | CSS resources folder                         |
| ┖ favicon                      | Favicon resources folder           |
| ┖ images                   | Image resources folder                        |
| ┖ vendor                             | JS and other resource folder          |

## Libraries
This project refers to the following third-party libraries:
- **Third-party libraries**: These are open-source dependencies. A detailed list of third-party libraries and their licenses can be found in the [dependencies-license.md](dependencies-license.md) file.

## GitHub Pages Technical Guide
This project provides a website service based on GitHub Pages technology, which offers hosting services for static pages. <br>
For a technical guide on GitHub Pages, please refer to [GitHub Pages](https://docs.github.com/en/pages). <br>

## docsify.js Technical Guide
This project is developed based on the open-source docsify.js. It provides HTML rendering services for Markdown document files. <br>
For a technical guide on docsify.js, please refer to [docsify.js](https://docsify.js.org/). <br>

## Website Management Technical Guide
- The sidebar displayed on the left of the website is managed based on the sidebar.md file. <br>
- The sidebar is managed per language and version in the [sidebar branch](https://github.com/OmniOneID/did-doc-architecture/tree/sidebar/). <br>
- When a version is upgraded, maintainers review the new version's document structure and create a new sidebar.md for that version. <br>
- The corresponding version folder is then created in the sidebar branch, with separate sidebar.md files for each language. <br>
- To make it easier to create sidebar.md, you can use  [docsify-cli](https://github.com/docsifyjs/docsify-cli). <br>
- The top-right navigation bar is also managed based on the navbar.md file, which is located in the sidebar branch. <br>
- When a new version of the sidebar is added, an alias setting needs to be added to index.html. Please add it to the following section of the code:
 
```java
alias: { // custom setting
  '/V1.0.0/(.*)': getRawGithubUserContentURL() + '/refs/heads/V1.0.0/$1',
  '/V1.1.0/(.*)': getRawGithubUserContentURL() + '/refs/heads/V1.1.0/$1'
},
```

- Additional details for website management will be continuously updated in this document.

## Contributing
Please read [CONTRIBUTING.md](CONTRIBUTING.md) and [CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md) for details on our code of conduct, and the process for submitting pull requests to us.

## License
[Apache 2.0](LICENSE)
