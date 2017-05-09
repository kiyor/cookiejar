## Usage

- before

```
cookieJar, _ := cookiejar.New(nil)
client := &http.Client{
  Jar: cookieJar,
}
```

- after

```
cookieJar, _ := cookiejar.New(nil,"./cookiejar")
client := &http.Client{
  Jar: cookieJar,
}
```

- default store location is $home/.gocookiejar
- only save after client called `SetCookies`