---
title: 財務と運用アプリの暗号化
description: この記事では、環境の SQL Server データベースと Azure ストレージに格納されている、休眠している顧客データの保護に使用される暗号化技術について説明します。
author: nedb
ms.date: 06/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: tfehr
ms.custom: 21631
ms.search.region: Global
ms.author: nedb
ms.search.validFrom: 2020-01-01
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 13f1b4bd7db0a383580ac49d34f213ef2bd8b46d
ms.sourcegitcommit: 3289478a05040910f356baf1995ce0523d347368
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/01/2022
ms.locfileid: "9108832"
---
# <a name="encryption-in-finance-and-operations-apps"></a>財務と運用アプリの暗号化

[!include [banner](../includes/banner.md)]

## <a name="encryption-at-rest"></a>休眠データの暗号化

Microsoft は、環境の SQL Server データベースと Azure ストレージに格納されている、休眠している顧客データを保護する目的で暗号化技術を使用しています。

すべてのインスタンスは、[Microsoft SQL Server Transparent Data Encryption (TDE) ](/sql/relational-databases/security/encryption/transparent-data-encryption)と [Azure ストレージ暗号化](/azure/storage/common/storage-service-encryption) を使用して、ディスクに書き込まれる休眠データをリアルタイムで暗号化しています。 

財務と運用アプリでは、サービスマネージド キーを使用したサーバー側の暗号化を使用します。 キーの発行、ローテーション、バックアップなどのキーに関する管理は、Microsoft が処理します。

上記の既定の暗号化に加えて、**グローバル** X + + クラスで使用可能な暗号化APIを使用できます。 **グローバル ::editencryptedfield ()** メソッド と **global ::editencryptedfield ()** メソッドは、環境固有のデータ暗号化証明書を使用して、データの暗号化と復号化を行います。 これらの方法は、データ ストレージに使用される既定の暗号化技術を超える、追加の保護層として使用できます。

## <a name="encryption-in-transit"></a>転送時の暗号化

顧客と Microsoft データセンターの間で確立される接続は暗号化されており、業界標準のトランスポート層セキュリティ (TLS) 1.2 を使用して、すべてのパブリック エンドポイントが保護されます。 TLSは、セキュリティを強化したブラウザとサーバー間の接続を効果的に確立し、デスクトップとデータセンター間のデータの機密性と完全性を効果的に確保します。 

### <a name="supported-tls-versions"></a>対応している TLS のバージョン

財務と運用アプリは、TLS 1.2 のみをサポートします。 TLS の古いバージョンである 1.0 と 1.1 には対応していません。

### <a name="supported-cipher-suites"></a>対応している暗号スイート

財務と運用アプリでは、以下の暗号スイートのみサポートしています。

* TLS_ECDHE_ECDSA_WITH_AES_256_GCM_SHA384
* TLS_ECDHE_ECDSA_WITH_AES_128_GCM_SHA256
* TLS_ECDHE_RSA_WITH_AES_256_GCM_SHA384
* TLS_ECDHE_RSA_WITH_AES_128_GCM_SHA256
* TLS_ECDHE_ECDSA_WITH_AES_256_CBC_SHA384
* TLS_ECDHE_ECDSA_WITH_AES_128_CBC_SHA256
* TLS_ECDHE_RSA_WITH_AES_256_CBC_SHA384
* TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA256

## <a name="additional-resources"></a>追加リソース

* [Azure 休眠データの暗号化](/azure/security/fundamentals/encryption-atrest)
* [Microsoft SQL Server透過データの暗号化 (TDE)](/sql/relational-databases/security/encryption/transparent-data-encryption)
* [Azure ストレージの暗号化](/azure/storage/common/storage-service-encryption)
* [開発のための内部者向けヒント](https://community.dynamics.com/ax/b/newdynamicsax)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
