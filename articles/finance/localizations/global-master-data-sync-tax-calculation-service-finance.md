---
title: 税計算サービスから Dynamics 365 Finance への税設定の同期
description: このトピックでは、税計算サービスから Microsoft Dynamics 365 Finance に税設定マスター データを同期する方法について説明します。
author: wangchen
ms.date: 01/05/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxIntegration, TaxServiceParameters
audience: Application user
ms.reviewer: kfend
ms.custom: intro-internal
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 3a9c11a6f5946d56b9e58a02c37f18adec155661
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/04/2022
ms.locfileid: "8687789"
---
# <a name="sync-the-tax-setup-from-the-tax-calculation-service-to-dynamics-365-finance"></a>税計算サービスから Dynamics 365 Finance への税設定の同期

[!include [banner](../includes/banner.md)]

このトピックでは、税計算サービスから Microsoft Dynamics 365 Finance に税設定マスター データを同期する方法について説明します。

[税の計算を始める](global-get-started-with-tax-calculation-service.md) で必要な設定手順を完了すると、以下の税設定データが税計算サービスから Finance に自動的に同期されます。

## <a name="sales-tax-code"></a>消費税コード

| 税計算サービス           | Finance                             |
| --------------------------------- | ----------------------------------- |
| 税コード                          | 消費税コード                      |
| Description                       | Name                                |
| ユーザー入力                        | 決済期間                   |
| ユーザー入力                        | 元帳転記グループ                |
| ユーザー入力                        | 消費税通貨                  |
| 負の税率が構成されている | マイナス消費税率の許可 |

## <a name="tax-value"></a>税額

| 税計算サービス | Finance                   |
| ----------------------- | ------------------------- |
| トランザクション開始日   | 自                 |
| トランザクション終了日     | 最終日                   |
| 最小額          | 最小値             |
| 最大時間数          | 上限             |
| 税率                | 値                     |
| 控除対象外のレート     | 控除対象外の割合 |

## <a name="tax-limits"></a>税の制限

| 税計算サービス | Finance           |
| ----------------------- | ----------------- |
| トランザクション開始日   | 自         |
| トランザクション終了日     | 最終日           |
| 最小税額      | 最小消費税 |
| 最大税額      | 最大消費税 |

## <a name="sales-tax-group"></a>売上税グループ

| 税計算サービス                         | Finance                                    |
| ----------------------------------------------- | ------------------------------------------ |
| 税グループ                                       | 売上税グループ                            |
| この税グループの税コード                  | この消費税グループの税コード |
| 税コードが **免税** としてマークされている         | 控除                                     |
| 税コードが **免税** としてマークされている         | 非課税コード                                |
| 税コードが、**リバースチャージである** としてマークされている | 受取人払い                             |
| 税コードが **税を使用する** としてマークされている        | 使用税                                    |

## <a name="item-sales-tax-group"></a>品目消費税グループ

| 税計算サービス             | Finance                                         |
| ----------------------------------- | ----------------------------------------------- |
| 品目別税グループ                      | 品目消費税グループ                            |
| この品目税グループの税コード | この品目売上税グループの税コード |

同期が完了した後も、転記やレポート作成のために残りのパラメータを Finance で管理します。

> [!NOTE]
> Finance から税計算サービスへの税設定の同期はサポートされていません。 既存の Finance 環境では、まずT税計算サービスで税の設定を作成します。 その後、設定データを Finance 環境に同期します。
