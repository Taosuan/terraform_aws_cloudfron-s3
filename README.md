# TerraformによるS3×CloudFront静的配信基盤構築

---

## ・ 概要

Terraformを用いてAWS上に静的Webサイト配信基盤を構築しました。  
サーバレス構成により、低コスト・高可用・高セキュリティなWeb配信を実現しています。

---

## ・ 構成図

![構成図](./images/diagram.png)


---

## ・ 特徴

・S3を非公開化し、CloudFront経由のみアクセス可能  
・CDNによる高速配信  
・Terraformによるインフラコード化（IaC）

---

## ・ 設計ポイント

### - セキュリティ

　S3バケットのパブリックアクセスを完全に遮断し、CloudFrontのOrigin Access Control（OAC）を利用してアクセス制御を実装しています。

### - パフォーマンス

　CloudFrontのエッジロケーションを活用し、ユーザーへのレスポンス速度を向上させています。

### - コスト最適化

　EC2などのサーバを使用せず、マネージドサービスのみで構成することで運用コストを削減しています。

### - 可用性

　S3およびCloudFrontのマネージドサービスにより、高い可用性を確保しています。

---

```plaintext
#実行方法(コードで定義した構成を構築)
terraform init
terraform apply

#削除方法（構築した構成を削除）
terraform destroy
