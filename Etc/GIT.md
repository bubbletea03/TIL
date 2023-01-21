# GIT 깨달은 것 기록

### `.gitignore`과 브랜치
`node_modules`가 있는 프로젝트에서 브랜치 이동을 할 때마다 난장판 나는 이유

- `node_modules`는 `.gitignore`에 의해 git의 관리 하에서 벗어나 있으므로, `checkout`을 해도 가만히 있기 때문이다.
- 이는 `.gitignore`이 적용되는 모든 프로젝트에서 주의가 필요하다.