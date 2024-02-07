---
title: Hafta 1
date: 2023/2/7
description: Go'nun temellerinin tanıtılması.
tag: golang
author: Abdullah Bagyapan
---

# Hafta 1

**Amaç :** Go'nun temellerinin tanıtılması.

**Yazarlar :** [**Abdullah Bagyapan**](https://github.com/abdullahbagyapan)

## Döngüler

Go'da sadece `for` döngüsü vardır.

```go
slc_1 := []int{10, 20, 30, 40, 50, 60, 70, 80, 90}

for i, value := range slc_1 {
    fmt.Printf("index: %d, value: %d \n", i, value)
}
```

## Struct

Structlar yeni yapılar oluşturmak için kullanılır. Verileri gruplamada yardımcı olur.

Go'da struct tanımı, `type <Ad> struct {}` şeklinde yapılır.

```go
type User struct {

}
```

Structlar farklı değişkenler tutabilir.

```go
type User struct {
    Id int
    Name string
    Age int
}
```

### Nesne Oluşturma

Tanımlanan struct nesnesini oluşturmanın birden fazla yolu vardır.

```go
user_1 := User{
    Id:1,
    Name:"user_1"
    Age:18
}
```

```go
user_2 := New(User)

user_2.Id = 2
Name:"user_2"
Age:20
```

## Pointer

Pointerlar bir değişkenin hafızadaki adresini tutarlar.

Bir değişkenin pointer tipinde olmasını istiyorsak değişken türünün önüne `*` koymak yeterli olacaktır.

```go
var pstr *string
```

Pointerlar, bir değişkenin adresini tutabilmeleri için o değişkenin adresini bilmeleri gerekir, `&` işareti ile bir değişkenin hafızadaki adresi öğrenilir.

```go
var pstr *string

str := "Hello World"

pstr = &str
```

> Not: Eğer tutulan adresteki değer değişirse pointerin değeride değişmiş olur

```go
var pstr *string

str := "Hello World"
pstr = &str     // *pstr: "Hello World"

str = "Golang"  // *pstr: "Golang"
```

## Fonksiyonlar

Go'da 2 tür fonksiyon vardır.

1. Normal fonksiyonlar
2. Receiver fonksiyonlar

### Normal fonksiyonlar

```go
func AddTwoNumber(x , y int) int {
    return x + y
}
```

### Receiver fonksiyonlar

Structa özel olarak tanımlanmış fonksiyonlardır. Belirtilen struct türü dışında erişilemez.

```go
func (u User) GetName() string {
    return u.Name
}
```

## Errors

Go'da beklenmedik durumlar için `error` değerleri kullanılır.

```go
func Open(name string) (file *File, err error)
```

```go
error := errors.New("Error ...")
```

## Modüller

Modül, Go paketlerinin tutulduğu bir dosyadır.

Modül oluşturmak için go dosyalarının bulunduğu kök dizinde, terminale `go mod init <example>` şeklinde yazmak yeterli olacaktır.

## Bu Hafta Neler Yaptık ?

- Döngüleri öğrendik.
- Structların ne olduğunu ve neden kullanıldığından bahsettik.
- Pointerların varlığından ve çözdüğü sorunları öğrendik.
- Fonksiyon tanımlamalarını öğrendik.
- Error yapılarını öğrendik.
- Modülün ne olduğunu ve neden kullanıldığını öğrendik.

**Haftaya Görüşmek Üzere!** 