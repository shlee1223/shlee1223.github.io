OmniOne OpenDID GitHub Pages
==

OmniOneID GitHub Pages Repository에 오신 것을 환영합니다. <br>
이 Repository는 OmniOneID GitHub Pages의 소스 코드, 문서, 관련 리소스를 포함하고 있습니다.

## 폴더 구조
프로젝트 디렉터리 내 주요 폴더와 문서에 대한 개요:

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

각 폴더와 파일에 대한 설명은 다음과 같습니다:

| 이름                             | 설명                                     |
| -------------------------------- | ---------------------------------------- |
| CLA.md                           | 오픈소스 기여를 위한 라이선스 관련 동의 정보              |
| CODE_OF_CONDUCT.md               | 기여자 행동 강령                         |
| CONTRIBUTING.md                  | 기여 지침과 절차                         |
| LICENSE                          | 라이선스                                 |
| MAINTAINERS.md                   | 프로젝트 유지 관리자 지침                |
| README.md    | 소스 코드 개요 및 지침                   |
| dependencies-license.md          | 프로젝트 의존 라이브러리의 라이선스 정보 |
| index.html          | GitHub Pages를 위한 메인 HTML 소스 |
| assets                             | 자산 폴더                                   |
| ┖ css                            | CSS 리소스 폴더                         |
| ┖ favicon                      | 파비콘 리소스 폴더           |
| ┖ images                   | 이미지 리소스 폴더                        |
| ┖ vendor                             | JS 등 리소스 폴더          |

## 라이브러리
이 프로젝트에서 사용되는 라이브러리는 아래와 같은 서드 파티 라이브러리를 참조합니다.
- **서드 파티 라이브러리**: 이 라이브러리들은 오픈 소스 종속성으로, 서드 파티 라이브러리와 해당 라이선스의 자세한 목록은 [dependencies-license.md](dependencies-license.md) 파일을 참고하십시오.

## GitHub Pages 기술 가이드
이 프로젝트는 GitHub Pages 기술을 기반으로 홈페이지 서비스를 제공합니다. 해당 기술을 통해 정적 페이지에 대한 호스팅 서비스를 제공합니다. <br>
GitHub Pages에 대한 기술 가이드는 [GitHub Pages](https://docs.github.com/en/pages)를 참조하십시요. <br>

## docsify.js 기술 가이드
본 프로젝트는 docsify.js 오픈소스를 기반으로 개발되었습니다. 해당 오픈소스를 통해 Markdown 문서 파일에 대한 HTML 렌더링 서비스를 제공합니다. <br>
docsify.js에 대한 기술 가이드는 [docsify.js](https://docsify.js.org/)를 참조하십시요. <br>

## 홈페이지 관리 기술 가이드
- 홈페이지 내부에서 출력되는 좌측의 사이드바는 sidebar.md 파일을 기준으로 관리됩니다. <br>
- 사이드바는 언어별 그리고 버전별로 관리되며, [sidebar branch](https://github.com/OmniOneID/did-doc-architecture/tree/sidebar/)에서 관리됩니다. <br>
- 버전이 업그레이드 될때마다 메인테이너는 신규 버전에 맞는 문서 목차를 검토한 후, 해당 버전에 맞는 sidebar.md를 생성합니다. <br>
- 이후 sidebar branch에 해당 버전의 폴더를 생성하고 언어별로 별도의 sidebar.md를 각각 생성합니다. <br>
- sidebar.md를 보다 쉽게 생성하기 위해서는 [docsify-cli](https://github.com/docsifyjs/docsify-cli)를 활용할 수 있습니다. <br>
- 우측 상단의 네비게이션바 또한 navbar.md 기준으로 관리되며 sidebar branch에 위치합니다. <br>
- 새로운 버전의 사이드바가 추가되는 경우 index.html 내부에 alias 설정 추가가 필요합니다. 아래 소스 코드 부분에 추가해주세요.
 
```java
alias: { // custom setting
  '/V1.0.0/(.*)': getRawGithubUserContentURL() + '/refs/heads/V1.0.0/$1',
  '/V1.1.0/(.*)': getRawGithubUserContentURL() + '/refs/heads/V1.1.0/$1'
},
```

- 이외 홈페이지 관리를 위한 추가적인 특이사항은 본 문서에 지속적으로 업데이트할 예정입니다.

## 기여
기여 절차와 행동 강령에 대한 자세한 내용은 [CONTRIBUTING.md](CONTRIBUTING.md)와 [CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md)를 참조해 주십시오.

## 라이선스
[Apache 2.0](LICENSE)
