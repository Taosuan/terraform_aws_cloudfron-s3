# ■ TerraformによるS3×CloudFront静的配信基盤構築

---

## ■ プロジェクト概要

本プロジェクトでは、Terraformを用いてAWS上に静的Webサイト配信基盤を構築しました。  
サーバレス構成を採用し、低コストかつ高可用なWeb配信を実現しています。

---

## ■ アーキテクチャ

```plaintext
User → CloudFront → S3
