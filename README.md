# 박태경 자기소개 웹앱

강원대학교 컴퓨터공학과 박태경의 자기소개 웹페이지입니다.

## 배포 URL
https://d3j3asnedn954j.cloudfront.net

## 아키텍처
- **정적 호스팅**: Amazon S3 + CloudFront (OAC, Origin Access Control)
- **방명록 (예정)**: AWS AppSync + Amazon DynamoDB

```
사용자 → CloudFront (OAC) → S3 (index.html)
                └─(추후) AppSync → DynamoDB (방명록)
```

## 리소스
- S3 버킷: `taekyung-selfintro-574667602767-an2`

## 배포 방법
```bash
aws s3 cp index.html s3://taekyung-selfintro-574667602767-an2/index.html --content-type "text/html; charset=utf-8"
aws cloudfront create-invalidation --distribution-id E391OHOX2IT4AC --paths "/*"
```

## 연락처
may621@naver.com
