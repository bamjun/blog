# 워드프레스 인증서 

[aws wordpress let's encrypt 가이드](https://docs.aws.amazon.com/ko_kr/lightsail/latest/userguide/amazon-lightsail-using-lets-encrypt-certificates-with-wordpress.html#request-a-lets-encrypt-certificate-wordpress)

인증서를 갱신 할때마다 고생이다.. aws 라이트세일에서 워드프레스 만들고, 가이드대로 인증서 발급했을때는 잘됐는데, 이게 메뉴얼 설정이라 자동갱신이 안돼는지 몰랐다.

서브도메인을 와일드 카드로 넣는 것때문에, 메뉴얼로 설정하는 방법을 알려준거 같다. 찾아보니, 서브도메일을 와일드 카드로 하려면, DNS 설정으로 해야하고, DNS 설정한 인증서를 자동갱신으로 하려면 DNS API를 이용해서, 자동화 해야한다.

DNS가 아닌 HTTP로 인증서를 발급해야, 자동갱신이 가능하다.

```bash
sudo certbot --apache -d example.com
```

이후 과정은 aws가이드에서 7단계 부터하면됨.

