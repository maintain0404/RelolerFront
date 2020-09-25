## 파일 watcher inotify 제한 해제
오류 : ENOSPC: System limit for number of file watchers reached
cmd : echo fs.inotify.max_user_watches=524288

## 다른 페이지 서브하기
다른 js 파일을 npm run serve 뒤에 붙여주면 됨