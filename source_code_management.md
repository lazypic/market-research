# Source code management

코드를 작성하기 시작했다면, 소스 관리툴을 같이 사용하는 것은 좋은 습관입니다.
회사에 프로그래머가 늘어나기 전에 회사 전체 코드에 대해 버전 관리를 시작하는 것이 좋습니다.
회사 스토리지에 있는 소스 코드가 날아가거나, 실수로 다른 개발자가 코드를 지우더라도 코드를 복원할 수 있어야 합니다.
매일 소스 코드 관리툴로 코드를 관리하게 되면 조직 이동이나 퇴사로 인한 업무 인수인계도 편하게 진행할 수 있습니다.

요즘 사용하는 코드 버전관리 시스템은 .md(마크다운)형식을 지원하기 때문에 코드뿐만 아니라 회사 기술문서, 정책 등의 정보도 버전 관리 하기가 편해졌습니다.

개인적으로 초반에는 Gogs, Gitea 형태의 무료 버전 관리시스템으로 시작하다가, 조직의 규모가 커지고 개발자 한명이 버전 관리 시스템을 온전히 관리할 수 있을 때 큰 어플리케이션으로 전환하는 것을 추천합니다. 초기에 설명한 오픈소스 툴로도 충분히 코드 버전관리, 이슈관리, PR + 코드리뷰 등의 업무가 가능합니다.
`.md` 형태의 개발 문서를 포함해서 코드를 Git 으로 잘 기록해 두었다면, Gogs 같은 가벼운 서비스에서 추후 Bitbucket + Jira 형태의 대규모 솔루션으로 마이그레이션 하는것은 어렵지 않습니다. 가장 피해야할 것은 수많은 솔루션을 도입해서 정책없이 이것 저것을 동시에 사용하는 것 입니다.

### Github
수많은 오픈소스 프로젝트가 Github를 사용합니다.
전 세계 개발자가 가장 많이 사용하는 플랫폼입니다.

- 홈페이지: https://github.com
- 사용하는 곳: [lazypic](https://github.com/lazypic), epic 등 전세계적으로 오픈소스 프로젝트에 많이 사용됩니다.
- 가격정책: https://github.com/pricing
    - Private 팀 리포지터리는 1인당 월 $9 소요.
    - Private 프로젝트가 될 정도로 가치가 있는 리포지터리 경우 1인당 월 $9 비용은 싸다고 생각합니다.

Lazypic이 Github를 솔루션을 사용하며 편리하다고 생각하는 점 중 하나는 Go 언어에서 패키지를 바로 불러서 사용할 수 있는 기능입니다.
큰 규모의 프로젝트 및 협업에 꽤 편리한 기능입니다.

```go
import "github.com/lazypic/package"

func main() {
    package.FunctionName()
}
```

### Gitlab
규모가 있는 버전 관리 시스템입니다. 인트라넷에 설치가 가능합니다.
관리자가 필요할 정도의 규모를 가진 툴입니다.

- 홈페이지: https://gitlab.com
- 라이센스: Creative Commons: CC BY-SA 4.0 license
- 작성언어: Go, Ruby, Vue.js
- 소스코드: https://gitlab.com/gitlab-org/gitlab-ce
- 가격정책: https://about.gitlab.com/pricing/
    - 제품별 기능제약: https://about.gitlab.com/features/
- 사용하는 곳: mofac, 4th

### Gogs
간단한 버전관리 툴입니다. 다운로드하고 실행하면 바로 사용할 수 있습니다. 관리가 거의 필요 없기 때문에 개발자가 적은 회사에 추천합니다.
회사 초기에는 적은수의 개발자가 여러가지 역할을 할 수 밖에 없기 때문에 Start-up 단계에서 추천합니다.

- 홈페이지: https://gogs.io
- 라이센스: MIT License
- 작성언어: Go
- 소스코드: https://github.com/gogs/gogs
- 사용하는 곳: Digitalidea, 2L

### Gitea
Gogs의 소스코드를 Fork 하여 개발된 소스코드 관리 시스템입니다.

- 홈페이지: https://gitea.io
- 라이센스: MIT License
- 작성언어: Go
- 소스코드: https://github.com/go-gitea/gitea

## ATLASSIAN Solution

### Bitbucket
기업이 온라인에서 비공개 리포지터리만 계속 만들어서 프로젝트를 진행하는 상황이라면 좋은 솔루션입니다.
서버 구축 없이 비용을 아낄수 있습니다.

- 홈페이지: https://bitbucket.org
- 가격정책: https://bitbucket.org/product/pricing
    - 내부서버: [50명 기준 1년 $3,300](https://www.atlassian.com/software/bitbucket/pricing?tab=self-managed)

### Jira ( and Confluence )
Jira는 소스코드 관리툴이라기 보다는 프로젝트 메니징 + 이슈관리 + 버그트레킹 관리 툴에 가깝습니다.
Jira 솔루션은 Bitbucket 코드 관리툴과 연동하여 강력하게 사용할 수 있기 때문에 이 항목에 함께 작성합니다.
회사 인원이 많아지고 대규모가 되면 도입을 검토해볼 필요가 있습니다.
초기에는 조직구조대비 복잡한 측면이 있습니다.

- 홈페이지: https://www.atlassian.com/software/jira
- 가격정책: https://www.atlassian.com/software/jira/pricing
    - 클라우드: 10명 이하 월 $10, 15명 이하 월 $75, 50명 이하 $300, 150명 월 $950
    - 내부서버: 250명 라이센스 일시불 $16,500 [self-managed](https://www.atlassian.com/software/jira/pricing?tab=self-managed) / 1인당 $66 모델
- 사용하는 곳: ILM, Weta, Pixar, Scanline, 4th, Samsung, NASA, Lockheed Martin, Raytheon, Boeing, Oracle, Novell, Harvard, Stanford ...

## Cloud Solution

### AWS: CodeCommit
- 홈페이지: https://aws.amazon.com/codecommit/
- 가격정책: 1인당 월 $1, 1기가당 $0.06, 1회 요청시 $0.001

lazypic은 비공개 되어야 하며, 라이센스 키젠 생성 툴처럼 협업이 필요없고 규모가 작은 코드에 이 서비스를 사용합니다.
AWS IAM 으로 권한을 확실히 할 수 있으며, lazypic은 AWS 기반으로 인프라가 되어있어 기존 구조와 잘 어울려서 셋팅할 수 있기 때문이기도 합니다.

### Google Cloud: Cloud Source Repositories
- 홈페이지: https://cloud.google.com/source-repositories/
- 가격정책: 5명 이상부터 1인당 월 $1, 1G당 $0.1, 1G 송신당 월$0.1

### Microsoft Azure: DevOps
- 홈페이지: https://azure.microsoft.com/en-in/services/devops/
- 가격정책: 5명까지 무료. 이후 명당 6,747원