# hello-go
* install Go:
```bash
brew install golang
```
* mkdir
```mkdir go-workspace```
* export GOPATH to /Users/f.yalcin/sandbox/go-workspace
```bash
# .zshrc
export GOPATH=$HOME/sandbox/go-workspace
export GOBIN=$GOPATH/bin
export GOROOT=/usr/local/opt/go/libexec
export PATH=$PATH:$GOPATH/bin
export PATH=$PATH:$GOROOT/bin
```
* check if set correctly:
```bash
go env GOPATH
/Users/f.yalcin/sandbox/go-workspace
```
* Create directory structure and the hello-go.go file inside:
```bash
mkdir go-workspace/src
mkdir go-workspace/bin
mkdir -p go-workspace/src/github.com/fy2/hello-go
touch go-workspace/src/github.com/fy2/hello-go/hello-go.go

go-workspace tree -Cf .
.
├── ./bin
└── ./src
    └── ./src/github.com
        └── ./src/github.com/fy2
            └── ./src/github.com/fy2/hello-go
                └── ./src/github.com/fy2/hello-go/hello-go.go

cd go-workspace/src/github.com/fy2/hello-go
git init .
# finish writing the Go program and then:
git add hello-go.go
git commit -m 'initial commit'
# create hello-go git remote repo and then
git remote add origin git@github.com:fy2/hello-go.
git push -u origin master
```
* Install the script:
```bash
cd go-workspace/src/github.com/fy2/hello-go

go install

cd /Users/f.yalcin/sandbox/go-workspace

tree -Cf bin
bin
└── bin/hello-go
```