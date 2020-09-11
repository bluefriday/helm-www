---
title: "관련 프로젝트와 문서"
description: "커뮤니티에서 제공하는 서드파티 도구, 플러그인 및 문서"
weight: 3
aliases: ["/docs/related/"]
---

헬름 커뮤니티는 헬름에 대한 많은 추가 도구, 플러그인 및 문서를 만들었습니다. 우리는
이러한 프로젝트에 대해 듣고 싶습니다.

이 목록에 추가하고 싶은 것이 있으면 
[이슈](https://github.com/helm/helm-www/issues)나 [풀 
리퀘스트](https://github.com/helm/helm-www/pulls) 할 수 있습니다.

## 헬름 플러그인

- [Helm Diff](https://github.com/databus23/helm-diff) - 컬러 diff로 `helm upgrade` 
  미리보기
- [helm-gcs](https://github.com/nouney/helm-gcs) - Google Cloud Storage에서 
  저장소를 관리하는 플러그인
- [helm-monitor](https://github.com/ContainerSolutions/helm-monitor) - 프로메테우스/엘라스틱서치 쿼리를 기반으로 
  릴리즈 및 롤백을 모니터링하는 플러그인
- [helm-k8comp](https://github.com/cststack/k8comp) - k8comp 를 사용하여 hiera 에서 
  헬름 차트를 생성하는 플러그인
- [helm-unittest](https://github.com/lrills/helm-unittest) - YAML 을 사용한, 로컬 단위 테스트 
  차트를 위한 플러그인
- [hc-unit](https://github.com/xchapter7x/hcunit) - OPA(Open Policy Agent) 및 Rego 를 
  사용한, 로컬 단위 테스트 차트를 위한 플러그인
- [helm-s3](https://github.com/hypnoglow/helm-s3) - [비공개] 차트 레포지토리로 AWS S3를 
  사용할수 있도록 해주는 헬름 플러그인
- [helm-schema-gen](https://github.com/karuppiah7890/helm-schema-gen) - 헬름 
  3 차트에 대한 값 yaml 스키마를 생성하는 헬름 플러그인
- [helm-secrets](https://github.com/jkroepke/helm-secrets) - 중요 정보를 안전하게 관리하고
  저장하는 플러그인 ([sops](https://github.com/mozilla/sops) 기반)

또한 깃헙 작성자가 플러그인 저장소에서 
[헬름-플러그인](https://github.com/search?q=topic%3Ahelm-plugin&type=Repositories) 태그를 
사용하도록 권장한다.

## 추가적인 도구들

헬름 위에서 계층화된 도구들.

- [Chartify](https://github.com/appscode/chartify) - 기존 쿠버네티스 리소스에서 
  헬름 차트를 생성
- [VIM-Kubernetes](https://github.com/andrewstuart/vim-kubernetes) - 쿠버네티스 및 헬름 용 
  VIM 플러그인
- [Landscaper](https://github.com/Eneco/landscaper/) - "Landscaper 는 값(원하는 상태)이 있는 
  헬름 차트 참조 세트를 가져와서 쿠버네티스 
  클러스터에서 이를 구현"
- [Helmfile](https://github.com/roboll/helmfile) - 헬름파일은 헬름 차트 배포를 
  위한 선언적 사양
- [Helmsman](https://github.com/Praqma/helmsman) - Helmsman은 버전 제어가 필요한 
  (단순 TOML 형식으로 설명된)상태파일로부터 
  릴리즈를 설치/업그레이드/보호/이동/삭제 할수 있는 
  코드로써의-헬름-차트 도구
- [테라폼 헬름 
  공급자](https://github.com/hashicorp/terraform-provider-helm) - HashiCorp 
  테라폼 용 헬름 공급자를 사용하면, 선언적 코드형 인프라 구문을 사용하여 
  헬름 차트의 수명 주기를 관리 가능. 헬름 공급자는 모든 인프라 서비스에서 
  공통의 워크플로를 만들기 위해 쿠버네티스 공급자처럼, 다른 테라폼 공급자와 
  쌍을 이루는 경우가 많음.
- [Monocular](https://github.com/helm/monocular) - 헬름 차트 저장소를 
  위한 웹 UI
- [Armada](https://airshipit.readthedocs.io/projects/armada/en/latest/) - 다양한 
  쿠버네티스 네임스페이스에서 접두사가 붙은 릴리즈를 관리하고 
  복잡한 배포를 위해 완료된 작업을 제거
- [ChartMuseum](https://github.com/helm/chartmuseum) - Amazon S3 및 
  구글 클라우드 스토리지를 지원하는 헬름 차트 저장소
- [Codefresh](https://codefresh.io) - 헬름 차트 및 릴리즈를 관리하기 위한 
  UI 대쉬보드가 있는 쿠버네티스 기본 CI/CD 와 관리 플랫폼 
- [Captain](https://github.com/alauda/captain) - HelmRequest 및 
  릴리즈 CRD를 사용하는 Helm3 컨트롤러
- [chart-registry](https://github.com/hangyan/chart-registry) - OCI 저장소의 
  헬름 차트 호스트
- [avionix](https://github.com/zbrookle/avionix) - 헬름 차트 및 쿠버네티스 yaml 을 
  생성하기 위해 상속 및 코드 중복의 감소를 허용하는 파이썬 인터페이스.

## 헬름 포함 요소

헬름 지원을 포함하는 플랫폼, 배포판 및 서비스.

- [Kubernetic](https://kubernetic.com/) - 쿠버네티스 데스크탑 클라이언트
- [Jenkins X](https://jenkins-x.io/) - GitOps 를 경유하는 환경을 
  통해 어플리케이션을 
  [구동](https://jenkins-x.io/docs/getting-started/promotion/) 하기 위해, 
  헬름을 사용하는 쿠버네티스용 오픈소스로 자동화 된 CI/CD 

## 기타

차트 작성자와 헬름 사용자를 위한 유용한 정보는 다음과 같다.

- [대기](https://github.com/saltside/await) - 다른 조건들에 대해 "대기" 하는 
  도커 이미지--초기화 컨테이너에 특히 유용 [더 
  보기](https://blog.slashdeploy.com/2017/02/16/introducing-await/)