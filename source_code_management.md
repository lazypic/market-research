# Source code management
회사에 프로그래머가 많아지기 전에 회사 전체 코드에 대해 버전관리를 시작해야 합니다.
회사 스토리지에 있는 소스코드가 날아가더라도 회사 전체 코드를 복원할 수 있어야합니다.
실수로 다른 개발자가 코드를 바꾸더라도 복원할 수 있어야 합니다.

요즘 만들어지는 버전관리 시스템은 .md(마크다운) 형식을 지원하기 때문에 회사 기술문서, 정책등도 코드처럼 관리할 수 있습니다.

### Github
전세계 개발자가 가장 많이 사용하는 플랫폼

- 홈페이지: https://github.com
- 사용하는 곳: [lazypic](https://github.com/lazypic), epic ... 전세계적으로 오픈소스 프로젝트에 많이 사용
- 가격정책: https://github.com/pricing
    - Private 팀 리포지터리는 1인당 $9 소요.

Lazypic이 github를 솔루션으로 사용하며 편리한점중 하나는 주로 사용하는 Go 언어에서 패키지를 바로 불러서 사용할 수 있다. 협업에 꽤 편리한 기능이다.

```go
import "github.com/lazypic/packagename"

func main() {
    packagename.funcname()
}
```

### Gitlab
- 홈페이지: https://gitlab.com
- 라이센스: Creative Commons: CC BY-SA 4.0 license
- 소스코드: https://gitlab.com/gitlab-org/gitlab-ce
- 가격정책: https://about.gitlab.com/pricing/
- 사용하는 곳: mofac, 4th

### Gogs
다운로드하고 실행하면 됩니다. 관리가 거의 필요없기 때문에 개발자가 적은회사에 추천합니다.

- 홈페이지: https://gogs.io
- 라이센스: MIT License
- 소스코드: https://github.com/gogs/gogs
- 사용하는 곳: Digitalidea, 2L

### Gitea
Gogs의 소스코드를 Fork 하여 개발됨.

- 홈페이지: https://gitea.io
- 라이센스: MIT License
- 소스코드: https://github.com/go-gitea/gitea

## ATLASSIAN solution

### Bitbucket
기업이 Private 리포지터만 계속 만들어서 프로젝트를 진행하는 상황이라면 좋은 솔루션이다.

- 홈페이지: https://bitbucket.org
- 가격정책: https://bitbucket.org/product/pricing

### Confluence and Jira
- 홈페이지: https://www.atlassian.com/software/jira
- 가격정책: https://www.atlassian.com/software/jira/pricing
- 사용하는 곳: ILM, Scanline, 4th