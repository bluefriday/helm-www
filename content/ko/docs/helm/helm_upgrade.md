---
title: "Helm Upgrade"
---

## helm upgrade

릴리스를 업그레이드 한다.

### 개요

이 명령은 릴리스를 새 버전의 차트로 업그레이드 한다.

업그레이드 인수는 릴리스 및 차트여야한다.
차트 인수는 차트 참조('example/mariadb'), 차트 디렉터리 경로, 
패키지 차트 또는 정규화된 URL 중 하나일수 있다.
차트 참조의 경우 '--version' 플래그가 설정되지 않으면 최신 버전이 지정된다.

차트의 값을 재정의하려면 '--values' 플래그를 사용하고 파일을
전달하거나 '--set' 플래그를 사용하고 명령 줄에서 구성을 전달하고,
문자열 값을 강제하려면 '--set-string' 을 사용한다. 값이 커서
'--value' 도 '--set'도 사용하지 않으련느 경우
'--set-file'을 사용하여 파일에서 하나의 큰 값을 읽을 수도 있다.

'--values'/'-f' 플래그를 여러 번 지정할 수도 있다. 지정된 마지막(가장 오른쪽) 파일에 우선 순위가 부여된다. 
예를 들어 myvalues.yaml과 override.yaml에 'Test' 라는 키가 포함된 경우
override.yaml에 설정된 값을 우선한다.

    $ helm upgrade -f myvalues.yaml -f override.yaml redis ./redis

'--set' 플래그를 여러번 지정할 수도 있다. 지정된 마지막(가장 오른쪽) 파일에 
우선 순위가 부여된다. 예를 들어 'foo' 라는 키에 대해 'bar' 와 'newbar' 에서 
값이 모두 설정된 경우 'newbar'rk dntjsgksek. 

    $ helm upgrade --set foo=bar --set foo=newbar redis ./redis


```
helm upgrade [RELEASE] [CHART] [flags]
```

### 옵션

```
      --atomic                       설정된 경우, 업그레이드 실패 시 변경 사항을 롤백. --atomic 을 사용하면 --wait 플래그가 자동으로 설정
      --ca-file string               이 CA 번들을 사용하여 HTTPS 사용 서버의 인증서를 확인
      --cert-file string             이 SSL 인증서 파일을 사용하여 HTTPS 클라이언트를 식별
      --cleanup-on-fail              업그레이드 실패 시, 이 업그레이드에서 생성된 새 리소스 삭제를 허용
      --create-namespace             --install 이 설정된 경우 릴리스 네임스페이스가 없으면 생성
      --description string           사용자 정의 설명을 추가
      --devel                        개발 버전도 사용. 버전 '>0.0.0-0'에 해당하며 --version 이 설정되어 있으면 무시
      --disable-openapi-validation   설정된 경우, 업그레이드 프로세스는 쿠버네티스 OpenAPI 스키마에 대해 렌더링된 템플릿의 유효성 검사 미수행
      --dry-run                      업그레이드 시뮬레이션
      --force                        대체 전략을 통해 리소스 강제 업데이트
  -h, --help                         업그레이드 명령어에 대한 도움말
      --history-max int              릴리스 당 저장되는 최대 리비전 수를 제한. 0으로 지정할 경우 무제한(기본값 10)
      --insecure-skip-tls-verify     차트 다운로드를 위한 TLS 인증서 검사 건너뛰기
  -i, --install                      이 이름의 릴리스가 아직 없는 경우 설치 수행
      --key-file string              이 SSL 키 파일을 사용하여 HTTPS 클라이언트 식별
      --keyring string               확인에 사용되는 공개키의 위치 (기본값 "~/.gnupg/pubring.gpg")
      --no-hooks                     사전/사후 업그레이드 훅 비활성화
  -o, --output format                지정된 형식으로 출력을 인쇄. 허용되는 값:table, json, yaml (기본값 table)
      --password string              요청된 차트를 찾을 수 있는 차트 저장소 비밀번호
      --post-renderer postrenderer   포스트 렌더링에 사용될 실행 파일의 경로. $PATH 에 있으면 바이너리가 사용되며 그렇지 않은 경우, 주어진 경로에서 실행파일을 탐색(기본 exec)
      --render-subchart-notes        설정된 경우, 상위 차트와 함께 하위 차트 메모도 렌더링
      --repo string                  요청된 차트를 찾을 수 있는 차트 저장소 URL
      --reset-values                 업그레이드 할 때, 값을 차트에 내장된 값으로 재설정
      --reuse-values                 업그레이드 할 때, 마지막 릴리스의 값을 재사용하고 --set 및 -f 를 통해 명령 줄에서 재정의를 병합. '--reset-values' 가 지정될 경우 무시
      --set stringArray              명령줄에서 값 설정(쉼표로 여러 값 또는 개별 값을 지정 가능. key1=val1,key2=val2)
      --set-file stringArray         명령줄을 통해 지정된 각 파일에서 값 설정(쉼표로 여러 값 또는 개별 값을 지정 가능. key1=val1,key2=val2)
      --set-string stringArray       명령줄에서 STRING 값 설정(쉼표로 여러 값 또는 개별 값을 지정 가능. key1=val1,key2=val2)
      --skip-crds                    설정된 경우, 설치 플래그가 활성화 된 상태에서 업그레이드를 수행할 때 CRD 미설치. 기본적으로 설치 플래그가 활성화된 상태에서 업그레이드가 수행될때, 아직 없는 경우에는 CRD 설치
      --timeout duration             개별 쿠버네티스 (훜에 대한 작업과 같이)작업을 기다리는 시간 (기본값 5m0s)
      --username string              요청된 차트를 찾을 수 있는 차트 저장소 사용자 이름
  -f, --values strings               YAML 파일 또는 URL에 값 지정 (여러 개 지정 가능)
      --verify                       사용하기 전에 패키지 확인
      --version string               사용할 정확한 차트 버전 지정. 지정하지 않을 경우 최신 버전 사용
      --wait                         설정된 경우, 릴리스를 성공으로 표시하기 전에 모든 파드, PVC, 서비스, 및 스테이트풀셋 또는 레플리카셋의 최소 파드 수가 준비 상태가 될때까지 대기. --timeout 플래그로 설정된 시간까지 대기
```

### 부모 명령어에서 상속된 옵션들

```
      --add-dir-header                   이 값이 참이면, 헤더에 파일 디렉토리를 추가
      --alsologtostderr                  표준 오류를 로그 및 파일로 표시
      --debug                            장황한(verbose) 출력 활성화
      --kube-apiserver string            쿠버네티스 API 서버의 주소 및 포트
      --kube-context string              사용할 kubeconfig 컨텍스트 이름
      --kube-token string                인증에 사용될 베어러(bearer) 토큰
      --kubeconfig string                kubeconfig 파일 경로
      --log-backtrace-at traceLocation   로깅 시 N 행에 걸친 스택 추적 내용을 표시 (기본값 :0)
      --log-dir string                   값을 지정하면, 지정한 디렉토리에 로그 파일 기록
      --log-file string                  값을 지정하면, 지정한 로그 파일 사용
      --log-file-max-size uint           로그파일이 증가할 수 있는 최대 크기 지정. 단위는 메가바이트이다. 값이 0이면, 최대 파일크기는 무제한. (기본값 1800)
      --logtostderr                      로그를 파일이 아닌 표준 출력으로 표시 (기본값 true)
  -n, --namespace string                 요청에 대한 네임스페이스 지정
      --registry-config string           레지스트리 구성 파일에 대한 경로 (기본값 "~/.config/helm/registry.json")
      --repository-cache string          캐시된 저장소 색인이 포함된 파일의 경로 (기본값 "~/.cache/helm/repository")
      --repository-config string         저장소 이름 및 URL 을 포함하는 파일 경로 (기본값 "~/.config/helm/repositories.yaml")
      --skip-headers                     이 값이 true이면, 로그파일에서 헤더 접두어를 미사용
      --skip-log-headers                 이 값이 true이면, 로그파일을 열 때 헤더 제외
      --stderrthreshold severity         stderr로 로그가 변경될 수 있는 최저 임계점 (기본값 2)
  -v, --v Level                          로그 수준 상세표시 레벨
      --vmodule moduleSpec               파일로 필터링된 로깅을 위한 패턴=N 설정의 쉼표로 구분된 리스트
```

### 참조

* [helm](helm.md)	 - 쿠버네티스에 대한 헬름 패키지 매니저.

###### Auto generated by spf13/cobra on 14-Sep-2020