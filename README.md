# pkm-atelier-img-2

`pkm-atelier` 의 **둘째** 그림 저장소다. 코드는 [pkm-atelier](https://github.com/polos0117/pkm-atelier),
첫 그림 저장소는 [pkm-atelier-img](https://github.com/polos0117/pkm-atelier-img) 에 있다.

## 왜 하나 더 두나

GitHub Pages 사이트 한 개는 1 GB 까지다. 첫 저장소가 그 선을 넘어서(2026-10, 약 1.18 GB)
새 그림은 여기에 올린다. 첫 저장소의 그림은 지우지도 옮기지도 않는다 — 옛 주소가 그대로 산다.

어느 그림이 어느 저장소에 있는지는 등록기가 `pkm-atelier` 의 `data/img.json` 에
`"where": {"<파일>": 1}` 로 적고, 화면(`lib/img.js` 의 `BASES`)이 그 번호로 주소를 고른다.
첫 저장소(0 번)는 적지 않는다.

## 규칙

- **새 그림은 여기에만 올린다.** 첫 저장소는 닫혔다 — 그쪽에 새 이름이 올라오면 등록이 전부 멈춘다.
  이미 있는 이름을 고쳐 그리는 교체만 그 파일이 있는 저장소에 덮어쓴다.
- 같은 이름을 두 저장소에 두지 않는다(등록이 멈춘다).
- 새 그림은 WebP 품질 85(method 6)로 만든다. 1024×1536 기준 한 장 약 0.3~0.4 MB.
- 파일 이름 규칙·자리는 첫 저장소와 같다 — [IMAGE_RULES.md](https://github.com/polos0117/pkm-atelier/blob/main/IMAGE_RULES.md).

```
img/<파일>.webp        원본. 폼 초상은 1024×1536 (2:3)
img/thumb/<같은 이름>   목록용. 긴 변 512 — 워크플로가 만든다
```

## 올린 뒤에 할 일

없다 — 첫 저장소와 똑같이 `썸네일` 워크플로가 썸네일을 만들고 `pkm-atelier` 의 `그림 등록` 을 깨운다.
깨우려면 이 저장소의 Actions 비밀에 `CODE_REPO_TOKEN` 이 있어야 한다(첫 저장소와 같은 토큰을 써도 된다 —
그 토큰은 `pkm-atelier` 만 건드린다).

## 처음 한 번

1. 공개(Public) 저장소로 만든다 — Pages 무료 요금제는 공개 저장소만 낸다.
2. Settings → Pages → Source: Deploy from a branch, `main` / `(root)`.
3. Settings → Secrets and variables → Actions → `CODE_REPO_TOKEN`.

`.nojekyll` 은 Pages 가 파일을 있는 그대로 내보내게 한다. 워크플로의 "크기" 단계가 900 MB 를 넘으면
경고를 띄운다 — 그때 `pkm-atelier-img-3` 을 같은 방법으로 준비한다.
