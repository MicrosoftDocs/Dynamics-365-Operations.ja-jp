---
title: キャッシュ フロー予測の有効化 (プレビュー)
description: このトピックでは、財務インサイトでキャッシュ フロー予測機能を有効にする方法について説明します。
author: ShivamPandey-msft
ms.date: 07/24/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-24
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: f7c06eaeb79c1a2aa319cfa3d2ad8255bf716cd0
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5818731"
---
# <a name="enable-cash-flow-forecasting-preview"></a>キャッシュ フロー予測の有効化 (プレビュー)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

このトピックでは、財務インサイトでキャッシュ フロー予測機能を有効にする方法について説明します。

> [!NOTE]
> キャッシュ フローで支払予測を使用するには、[顧客支払予測の有効化](enable-cust-paymnt-prediction.md) で説明されているように、顧客支払予測機能を設定する必要があります。

1. Microsoft Dynamics Lifecycle Services (LCS) で環境ページの情報を使用して、その環境に対する Azure SQL のプライマリ インスタンスに接続します。 次の Transact-SQL (T-SQL) コマンドを実行して、サンドボックス環境のフライトを有効にします。 (Application Object Server \[AOS\] にリモートで接続する前に、LCS で IP アドレスに対してアクセスを有効にする必要がある場合があります。)

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('CashflowInsightsFeature', 1)`

    > [!NOTE]
    > Microsoft Dynamics 365 Finance の配置が Service Fabric 配置である場合は、この手順を省略できます。 財務インサイト チームは既にフライトを有効にしている必要があります。 **機能管理** ワークスペースに機能が表示されない場合や、有効にしようとしたときに問題が発生した場合は、<fiap@microsoft.com> に連絡してください。
  
2. **機能管理** ワークスペースを開き、次の手順に従います:

    1. **更新プログラムの確認** を選択します。
    2. 以下の機能を有効にします:

        - 新しいグリッド コントロール
        - グリッド内でのグループ化 (プレビュー) 
        - 顧客支払予測 (プレビュー)
        - キャッシュ フロー予測 (プレビュー)

3. **現金および銀行管理 \> キャッシュ フロー予測の設定** に移動し、予測に含める流動資産勘定を追加します。

    > [!NOTE]
    > 流動資産勘定が設定されていない場合は、キャッシュ フローを生成できません。

4. **現金および銀行管理 \> 設定 \> 財務インサイト (プレビュー) \> キャッシュ フロー予測** に移動し、次の手順を実行します:

    1. **キャッシュ フロー予測** タブで、**機能の有効化** を選択します。
    2. **予測モデルの作成** を選択します。

キャッシュ フロー予測機能の詳細については、[キャッシュ フロー予測](cash-flow-forecast-intro.md) を参照してください。

## <a name="privacy-notice"></a>プライバシー通知

プレビューは (1) Dynamics 365 Finance and Operations サービスを下回るプライバシーおよび少ないセキュリティ対策を使用している場合があり、(2) このサービスのためにサービス レベル アグリーメント (SLA) には含まれておらず、(3) 個人データや、その他の法律上またはコンプライアンス要件の対象となるデータの処理に使用されず、(4) サポートが制限されます。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]