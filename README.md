# 한낮의 해바라기

아버지의 시를 모은 사이트입니다. 시는 Supabase DB에 저장되고, 관리자만 사이트에서 직접 올릴 수 있습니다.

## 처음 한 번만 하는 설정

1. **SQL Editor** → New query → `supabase/setup.sql` 내용을 붙여넣고, `YOUR_EMAIL`을 관리자 이메일로 모두 바꾼 뒤 **Run**
2. **Authentication → Users → Add user → Create new user** → 같은 이메일 + 비밀번호, **Auto Confirm User** 체크
3. **Authentication → Sign In / Providers** → **Allow new users to sign up** 끄기
4. **Project Settings → API Keys** 에서 `anon public` 키 복사
5. `index.html` 위쪽 두 줄에 붙여넣기
   ```js
   const SUPABASE_URL = 'https://프로젝트주소.supabase.co';
   const SUPABASE_ANON_KEY = 'anon public 키';
   ```
6. GitHub에 `index.html` 올리기

## 시 올리기

1. 사이트 맨 아래 **관리** → 로그인
2. **새 시 올리기**: 제목, 쓴 날짜, 시, 사진(선택) → **올리기**
3. 쓴 날짜에 따라 차례의 "2026년 11월" 같은 묶음에 자동으로 들어갑니다.
4. 시 화면의 **이 시 고치기**에서 수정·삭제할 수 있습니다.

`service_role` 키는 절대 넣지 마세요. `anon public` 키는 공개돼도 괜찮습니다.
