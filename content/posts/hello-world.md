+++
date = "2017-04-03T19:13:42-04:00"
title = "hello world"
draft = false
tags = [ "golang", "docker" ]
categories = [ "getting-started" ]
+++

# Introduction
Hello, world!

One of the simpler introductory hello world implementations is with Docker.
```bash
docker run hello-world
```
See more at https://docs.docker.com/engine/getstarted/step_one/#step-3-verify-your-installation.

Then with Go, the introductory code looks like the following.
```
package main

import "fmt"

func main() {
  fmt.Println("Hello, world!")
}
```
Assuming that code exists in a file `main.go`, you would then just need to do:
```bash
go run main.go
```
Or, just go to https://play.golang.org to test it out in the browser.