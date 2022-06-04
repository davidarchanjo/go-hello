![banner](./assets/banner.jpg)

# INSTALLATION
1. Download the current release from the official [download page](https://go.dev/dl/)
```shell
$ wget -c https://go.dev/dl/go1.18.3.linux-amd64.tar.gz -O - | tar -xz
```

2. Remove any previous Go installation
```shell
$ sudo rm -rf /usr/local/go
```

3. Move Go directory to default location
```shell
$ sudo mv go /usr/local
```

4. Set Go binary to be system-wide available
```shell
$ echo "export GOHOME=/usr/local/go" >> ~/.bashrc
$ echo "export PATH=$PATH:$GOHOME/bin" >> ~/.bashrc
$ source ~/.bashrc
```

5. Verify Go version
```shell
$ go version
go version go1.17 linux/amd64
```

7. Set GOPATH environment variable
```shell
$ cd ~ && mkdir go
$ echo "export GOPATH=$(pwd)/go" >> ~/.bashrc
$ echo "export PATH=$PATH:$GOPATH/bin" >> ~/.bashrc
```

# TEST INSTALLATION
1. Create a `hello.go` file
```shell
$ touch hello.go
```

2. Copy and paste the content
```go
package main

import "fmt"

func main() {
    fmt.Printf("hello, World!")
}
```

3. Run hello.go
```shell
$ go run hello.go
Hello, World!
```

4. Build hello.go to generate its native executable
```shell
$ go build hello.go
```

5. Run hello executable
```shell
$ ./hello
Hello, World!
```