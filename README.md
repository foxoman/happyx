<div align="center">

![Happyx](https://user-images.githubusercontent.com/49402667/228402522-6dd72d4b-c21c-4acf-b1e2-8318b6e809da.png)
### Asynchronous web-framework written in Nim with ♥

![Nim language](https://img.shields.io/badge/>=1.4.0-1b1e2b?style=for-the-badge&logo=nim&logoColor=f1fa8c&label=Nim&labelColor=2b2e3b)

[![wakatime](https://wakatime.com/badge/user/eaf11f95-5e2a-4b60-ae6a-38cd01ed317b/project/bbd13748-36e6-4383-ac40-9c4e72c060d1.svg?style=for-the-badge)](https://wakatime.com/badge/user/eaf11f95-5e2a-4b60-ae6a-38cd01ed317b/project/bbd13748-36e6-4383-ac40-9c4e72c060d1)

[![Testing](https://github.com/HapticX/happyx/actions/workflows/tests.yml/badge.svg?style=for-the-badge)](https://github.com/HapticX/happyx/actions/workflows/tests.yml)

</div>


# Why HappyX? 💁‍♀️
Because it's simple to use 🙂

## Features ⚡
- Support `asynchttpserver` as default http server
- Support `httpx` via `-d:httpx`
- Logging with `-d:debug`

# Get Started 👨‍🔬

## Installing 📥
### Via Nimble
```bash
nimble install happyx
```
### Via GitHub
```bash
nimble install https://github.com/HapticX/happyx
```

## Usage ▶
```nim
import happyx

proc main =
  var server = newServer()

  server.routes:
    "/":
      req.answer("Hello, world!")
    
    "/user{id:int}"
      req.answer(fmt"Hello, user with ID {id}!")
  
  server.start()
  
main()
```
## Run 💻
### Default
```bash
nim c -r -d:ssl -d:debug main
```
### Httpx
```bash
nim c -r -d:ssl -d:debug -d:httpx main
```


# Contributing 🌀
You make us happy when sending PR or help us to find bugs and errors 🐛
