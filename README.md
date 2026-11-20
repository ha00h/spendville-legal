# Spendville legal site (GitHub Pages)

정적 페이지:

| 경로 | 용도 |
|---|---|
| `/` | 인덱스 |
| `/privacy.html` | 개인정보처리방침 |
| `/account-deletion.html` | 계정 삭제 안내 (스토어 웹 URL) |

## 한 번에 배포 (권장)

Spendville와 분리된 **공개** 저장소를 씁니다.

```bash
# 1) GitHub 로그인 (토큰 만료 시)
gh auth login -h github.com

# 2) 이 폴더만 새 공개 레포로 푸시
cd legal-site
git init -b main
git add .
git commit -m "Add Spendville legal pages for store URLs."
gh repo create spendville-legal --public --source=. --remote=origin --push

# 3) Pages: Settings → Pages → Deploy from branch → main / root
#    또는 아래 Actions 워크플로를 레포 루트에 두고 GitHub Actions로 배포
```

배포 후 URL 예:

- `https://<github-username>.github.io/spendville-legal/`
- `https://<github-username>.github.io/spendville-legal/privacy.html`
- `https://<github-username>.github.io/spendville-legal/account-deletion.html`

## 연락처

`privacy.html` / `account-deletion.html`의 **(성명 기입)·(이메일 기입)** 을 채운 뒤 다시 푸시하세요.

## 커스텀 도메인 (선택)

Cloudflare/호스팅에서 `legal.hyeheaglab.com` → GitHub Pages로 CNAME 연결 후, 이 폴더에 `CNAME` 파일(`legal.hyeheaglab.com`)을 추가합니다.
