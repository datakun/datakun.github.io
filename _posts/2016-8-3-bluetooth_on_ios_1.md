---
layout: post
title: iOS에서 블루투스로 데이터를 보내고 싶었을 뿐인데..
---

[스택오버플로우의 답변](http://stackoverflow.com/a/24181946)

1. 나는 Qt를 이용해 SPP 프로파일만 지원하는 블루투스 기계(다른 통신방법은 RS232)와 아이폰 사이에 데이터를 교환하고싶었다.
그렇게 삽질은 시작됐다.


2. 일주일동안의 삽질을 통해 겨우 블루투스에 대해 겉핥기만 할 수 있었다.
블루투스 프로필 종류, 버전에 따른 소소한 차이점, 애플의 정책에 대해 알아가고 있을뿐이다.
위 스택오버플로우 답변을 정리하면,
블루투스 'Classic' 버전 모듈을 사용할 때 [iOS: 지원되는 Bluetooth 프로파일](https://support.apple.com/ko-kr/HT204387) 의 프로파일을 사용할 수 있다.
(단, 해당 모듈이 MFi 프로그램에 가입되어있어야한다.)
다른 방법으로 BLE(Bluetooth Low Energy) 모듈을 사용하는 방법이 있다.
이 방법은 해당 모듈이 MFi에 가입되어있지 않아도 된다.
즉, MFi 프로그램에 등록되어있지않은 블루투스 기계는 BLE 모듈을 중간자로 연결하여 아이폰과 통신이 가능하다.
문제는 국내에는 RS232<->BLE 모듈이 없다.
또다른 문제점이다..
