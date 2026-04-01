# TerraformによるS3×CloudFront静的配信基盤構築

---

## ■ 概要

Terraformを用いてAWS上に静的Webサイト配信基盤を構築しました。  
サーバレス構成により、低コスト・高可用・高セキュリティなWeb配信を実現しています。

---

## ■ アーキテクチャ

![構成図](./images/diagram.png)

```plaintext
User → CloudFront → S3

---

## ■ 特徴

・S3を非公開化し、CloudFront経由のみアクセス可能
・CDNによる高速配信
・Terraformによるインフラコード化（IaC）

---
