# AGENTS.md

이 저장소는 **Alfred 워크플로우**다. `info.plist`가 워크플로우 본체이고, Alfred는 이 폴더 자체를 워크플로우로 로드한다.

## Alfred와의 연결

이 저장소는 Alfred의 워크플로우 디렉토리에 **symlink (`ln -s`)** 로 연결되어 있다:

```
~/Library/Application Support/Alfred/Alfred.alfredpreferences/workflows/user.workflow.E1A0154E-1AC6-4DF8-9C3A-9E936D302048
  -> (이 저장소 경로)
```

따라서 이 저장소의 파일을 수정하면 Alfred에 즉시 반영된다. 별도 빌드/설치 단계는 없다.

링크 생성/검증은 `./install.sh` 로 한다 (idempotent, macOS 전용). 다른 머신에서 clone 후 한 번 실행하면 동일한 경로로 연결된다.
