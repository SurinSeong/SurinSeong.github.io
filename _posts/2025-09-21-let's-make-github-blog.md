---
layout: post
title: "[Mac] Github Blog 만들기"
subtitle: "Github Blog를 만들기 위해 준비해야 할 것은 무엇일까요? 함께 알아가봅시다!"
date: 2025-09-21 22:00:00 +0900
background: 
category: 블로그
---

# 1. 새로운 repository 생성하기

- github에 블로그용 새로운 repo를 생성한다.
- repo 이름: `깃허브계정이름.github.io`

# 2. 생성한 repo를 로컬에서 편집할 수 있도록 가져오기

- 블로그용 repo를 본인의 로컬 환경에서 편집할 수 있도록 clone 받아온다.
- 주의: **git**이 설치 되어 있어야 함.

# 3. Ruby 설치

- MacOS에는 사전 설치된 Ruby가 있음.
- Ruby 버전을 업그레이드 하고 싶을 경우, **Homebrew**를 통해서 업그레이드 할 수 있음.
  ```zsh
  brew update
  brew upgrade

  # Ruby 버전 업그레이드 하기 - rbenv 사용
  # brew를 통해 rbenv 설치
  brew install rbenv ruby-build

  rbenv init

  # 새로운 터미널 열고
  curl -fsSL https://github.com/rbenv/rbenv-installer/raw/main/bin/rbenv-doctor | bash

  mkdir -p /Users/ashleytharp/.rbenv/shims
  # 권한 설정으로 인한 접근 제한이 뜬다면 앞에 sudo를 붙여서 enter 친 후, password를 입력
  # password를 모른다면, 권한 설정 해준 뒤, 다시 시도

  vim ~/.bash_profile
  # 파일 작성
  eval "$(rbenv init - bash)"
  export PATH="/Users/내Mac사용자이름/.rbenv/shims:$PATH"

  source ~/.bash_profile

  # rbenv를 통한 업그레이드
  rbenv install 특정버전

  # 설치한 버전 글로벌 설정
  rbenv global 설치한버전

  # 새로운 터미널 열기
  ruby -v
  ```

# 4. Jekyll 과 bundler 설치

- Bundler : 루비 프로젝트에 필요한 gem들의 올바른 버전을 추적하고 설치해서 일관된 환경을 제공하는 도구

  ```
  gem install jekyll bundler
  ```

# 5. 원하는 블로그 테마 선택하기

- jekyll 테마를 내 블로그 레포의 로컬 폴더에 다운 받기

# 6. github 서버에 반영하기

  ```
  git add .
  git commit -m "커밋 메시지"
  git push origin master
  ```
