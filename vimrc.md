~~~
" 구문 강조 사용
if has("syntax")
 syntax on
endif

" 화면 설정
set number " 줄번호
set laststatus=2 " 마지막 창에 statusline을 보여주는 설정 / 0:출력안함, 1:창이 2개 이상일 때 출력, 2:항상 출력
set showcmd " 사용자가 입력한 명령어 표시
set showmatch " 일치하는 괄호 하이라이팅
set ruler " 현재 커서 위치 표시
" set relativenumber " 커서를 기준으로 라인 넘버 표시, 커서 위치에 따라 바뀜
set cursorline " 커서가 있는 라인을 강조
set mouse=a " 마우스 스크롤 및 리사이즈 기능 [n: Normal mode, v: Visual mode, i: Insert mode, a: All modes]

" 검색 설정
set hlsearch " 검색어 하이라이팅
set ignorecase " 검색시 대소문자를 구분하지 않음
set incsearch " 검색어를 입력할 때마다 일치하는 문자열을 강조
set smartcase " ignore 옵션이 켜져있어도 검색어에 대문자가 있다면 정확히 일치하는 문자열을 찾음

" 들여쓰기 설정
set cindent " C언어 자동 들여쓰기
set autoindent " 자동 들여쓰기
set shiftwidth=4 " 자동 들여쓰기 너비 설정
set tabstop=4 " Tab으로 들여쓰기 시 사용할 스페이스 개수
set softtabstop=4 " 스페이스바 n개를 하나의 탭으로 처리
set smarttab " ts, sts, sw 값을 참조하여, 탭과 백스페이스의 동작을 보조
set smartindent " 자동 들여쓰기 시 #include와 같은 전처리 구문을 판단하여 들여쓰기를 하지 않음

" 입력 설정
set paste " 다른 곳에서 복사한 내용을 붙여넣을 때 자동 들여쓰기가 적용되는 것을 막음
set history=256 " 편집한 내용 저장 개수 (되돌리기 제한 설정)

" 파일 인코딩을 한국어로
if $LANG[0]=='k' && $LANG[1]=='o'
set fileencoding=korea
endif



set scrolloff=2
set wildmode=longest,list
set sw=1 " 스크롤바 너비
set autowrite " 다른 파일로 넘어갈 때 자동 저장
set autoread " 작업 중인 파일 외부에서 변경됬을 경우 자동으로 불러옴
set bs=eol,start,indent
set statusline=\ %<%l:%v\ [%P]%=%a\ %h%m%r\ %F\
" 마지막으로 수정된 곳에 커서를 위치함
au BufReadPost *
\ if line("'\"") > 0 && line("'\"") <= line("$") |
\ exe "norm g`\"" |
\ endif~~~
