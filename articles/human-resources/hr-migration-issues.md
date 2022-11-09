---
title: Dynamics 365 Human Resources インフラストラクチャ統合の既存の問題
description: この記事は、 Microsoft Dynamics 365 Human Resources インフラストラクチャ統合の際に発生する可能性がある問題を一覧表示します。
author: twheeloc
ms.date: 10/27/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 28c2c10a9293d00e26dfcc80ab08b89a122a6135
ms.sourcegitcommit: 088a7b5eb9a3b68710dfe012abf4c24776978750
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/01/2022
ms.locfileid: "9733476"
---
# <a name="dynamics-365-human-resources-infrastructure-merge-known-issues"></a>Dynamics 365 Human Resources インフラストラクチャ統合の既存の問題

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]
[!include [preview banner](../includes/preview-banner.md)]

## <a name="shared-dataverse-environments"></a>共有された Dataverse 環境

デュアル書き込みフレームワークは、2 つの財務と運用アプリ環境を同じ Dataverse 環境にリンクさせることはできません。 以下の両方の項目と共有している Dataverse 環境がある場合、Dataverse 環境を複製するか、分割する必要があります。

- 財務と運用アプリ
- 現在の人事環境

## <a name="environment-type-requirements"></a>環境タイプの要件

移行を行うには、以下の環境タイプが必要です:

- サンドボックスのスタンドアロン環境がない場合、移行を検証するために作成する必要があります。
- 複数の運用スタンドアロン環境がある場合、そのうちの 1 つを移行することができます。 他の環境をサンドボックスとしてマークするよう、Microsoft サポートに連絡してください。

## <a name="teams-integration"></a>Teams 統合

現在、Teams の既存の人事アプリは、Microsoft Power Platform ソリューションに移行しています。 詳細については、[Teams の Human Resources アプリ](hr-admin-teams-leave-app.md) を参照してください。

## <a name="licensing"></a>ライセンス

次の領域では Dynamics 365 Human Resources のライセンスに変更はありません: 

- **ライセンス購買の最小数**
- **運用環境とサンドボックス環境のライセンス** - 運用環境とサンドボックス環境を 1 つずつ付与する既存のスタンドアロン人事ライセンスをお持ちの場合、同じ数のライセンスを追加コストなしで財務と運用インフラストラクチャで利用できます。
- **追加のサンドボックス ライセンス** - スタンドアロンの人事アプリケーションのサンドボックス ライセンスを追加購入した場合、財務と運用インフラストラクチャ上のサンドボックス環境にも同じ数のライセンスが利用できます。 
