---
title: "Helm Get All"
---

## helm get all

명명된 릴리스에 대한 모든 정보 다운로드

### 개요


이 명령어는 지정한 릴리스에서 노트, 훅, 제공된 값 및 생성된 
매니페스트 파일에 대한 정보를 사람이 읽을 수 있는 콜렉션으로 출력한다.


```
helm get all RELEASE_NAME [flags]
```

### 옵션

```
  -h, --help              all 에 대한 도움말
      --revision int      리비전으로 명명된 릴리스 가져오기
      --template string   출력 형식 지정을 위한 go 템플릿. 예: {{.Release.Name}}
```

### 부모 명령어에서 상속된 옵션들

```
      --add-dir-header                   이 값이 true이면, 헤더에 파일 디렉토리를 추가한다
      --alsologtostderr                  파일처럼 표준오류(stderr)로도 로그 출력
      --debug                            장황한(verbose) 출력 활성화
      --kube-apiserver string            쿠버네티스 API 서버의 주소 및 포트
      --kube-context string              사용할 kubeconfig 컨텍스트 이름
      --kube-token string                인증에 사용할 베어러(bearer) 토큰
      --kubeconfig string                kubeconfig 파일 경로
      --log-backtrace-at traceLocation   로깅 시 N 행에 걸친 스택 추적 내용을 표시 (기본값 :0)
      --log-dir string                   값을 지정하면, 지정한 디렉토리에 로그 파일 기록
      --log-file string                  값을 지정하면, 지정한 로그 파일 사용
      --log-file-max-size uint           로그파일이 증가할 수 있는 최대 크기 지정. 단위는 메가바이트이다. 값이 0이면, 최대 파일크기는 무제한. (기본값 1800)
      --logtostderr                      로그를 파일이 아닌 표준 출력으로 표시 (기본값 true)
  -n, --namespace string                 요청에 대한 네임스페이스 지정
      --registry-config string           레지스트리 구성 파일에 대한 경로 (기본값 "~/.config/helm/registry.json")
      --repository-cache string          캐시된 저장소 색인이 포함된 파일의 경로 (기본값 "~/snap/code/common/.cache/helm/repository")
      --repository-config string         저장소 이름 및 URL 을 포함하는 파일 경로 (기본값 "~/.config/helm/repositories.yaml")
      --skip-headers                     이 값이 true이면, 로그파일에서 헤더 접두어를 미사용
      --skip-log-headers                 이 값이 true이면, 로그파일을 열 때 헤더 제외
      --stderrthreshold severity         stderr로 로그가 변경될 수 있는 최저 임계점 (기본값 2)
  -v, --v Level                          로그 수준 상세표시 레벨
      --vmodule moduleSpec               파일로 필터링된 로깅을 위한 패턴=N 설정의 쉼표로 구분된 리스트
```

### 참조

* [helm get](helm_get.md)	 - 명명된 릴리스의 확장 정보 다운로드

###### Auto generated by spf13/cobra on 11-May-2020