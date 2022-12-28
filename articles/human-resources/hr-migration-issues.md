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
ms.openlocfilehash: 3fe21df8be010ace3070ad08ed95f3d3efc7b01d
ms.sourcegitcommit: bdee5e642d417a13abdb778c14ec5f2dbbf8dee7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/09/2022
ms.locfileid: "9838558"
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

## <a name="dual-write-integration"></a>二重書き込みの統合

二重書き込み は、Customer Engagement アプリと財務と運用アプリの間の、ほぼリアルタイムの対話を提供する既成のインフラストラクチャです。 統合に二重書き込みを使用している場合、見つかったいくつかの問題が発生する可能性があります。 Dataverse テーブルおよび問題の詳細については、[Dataverse テーブル](hr-developer-entities.md) を参照してください。

