---
title: データ統合プロジェクトの作成
description: このトピックでは、データ統合プロジェクトの作成方法について説明します。
author: ShivamPandey-msft
ms.date: 02/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-24
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 50f435f9d461667a1908baa529d73766085c183a
ms.sourcegitcommit: 6526acd0300d9c5800d3d7675d54e23090d031df
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/10/2022
ms.locfileid: "8107290"
---
# <a name="create-a-data-integration-project"></a>データ統合プロジェクトの作成

[!include [banner](../includes/banner.md)]

このトピックでは、データ統合プロジェクトの作成方法について説明します。

1. Microsoft Dynamics 365 Finance にサインインします。
2. **ワークスペース \> データ管理** に移動し、**データ エンティティ** を選択します。 すべてのデータ エンティティが更新されるまで待機し、次のステップに進みます。
3. [Power Appsポータル](https://make.powerapps.com/)を開き、次 の手順を実行します。

    1. 適切な環境を選択します。
    2. 左側のナビゲーション ペインで、**Dataverse \>接続** を選択します。
    3. 次の項目の適切なインスタンスに接続します :

        - Dynamics 365
        - Dynamics 365 for Fin & Ops

4. [Power Apps 環境](https://admin.powerapps.com/environments)を開き、次の手順を実行します。

    1. **データ統合** を選択します。
    2. **接続設定** タブを選択します。
    3. **新規接続設定** を選択します。
    4. 接続の名前を入力します。
    5. 次の項目に対して適切な接続を選択します。

        - Dynamics 365
        - Dynamics 365 for Fin & Ops

    6. 適切な組織のマッピングを選択します。
    7. **作成** を選択します。

5. [Power Apps 環境](https://admin.powerapps.com/environments)を開き、次の手順を実行します。  

    1. 作成した接続セットを使用して、次のテンプレートのデータ統合プロジェクトを作成します。

        - 顧客支払分析情報の結果 (CDS から Finance and Operations 10.0.17 以上)
        - キャッシュ フロー時系列の結果 (CD から Fin と Ops)
        - 予算時系列の結果 (CD から Fin と Ops)

    2. プロジェクトごとに適切なスケジューリングを設定します。

> [!NOTE]
> Dataverse に必要なエンティティが表示されない場合は、**与信と回収** > **設定** > **Finance Insights** > **Finance Insights パラメーター** に移動し、機能 **顧客支払予測** を有効にしてから、**予測モデルの作成** を選択します。 AI モデルの配置が完了すると、統合の作成に必要な Dataverse エンティティが展開されます。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
