---
title: Dynamics 365 Commerce プレビュー環境の概要
description: このトピックでは、Microsoft Dynamics 365 Commerce プレビュー環境の概要を示します。
author: v-chgri
manager: annbe
ms.date: 12/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: v-chgri
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 1ff96aeb5963df9ddee56783a089dad129bbb71c
ms.sourcegitcommit: 4ed1d8ad8a0206a4172dbb41cc43f7d95073059c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/04/2020
ms.locfileid: "3024686"
---
# <a name="dynamics-365-commerce-preview-environment-overview"></a>Dynamics 365 Commerce プレビュー環境の概要


[!include [banner](includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 Commerce プレビュー環境の概要を示します。

## <a name="overview"></a>概要

Commerce プレビュー環境は Dynamics 365 Commerce のオプションのエンドツーエンドのプレビュー環境であり、潜在顧客が一般公開前に Commerce 製品を試すことができます。

機能に影響しないいくつかの制限事項とは別に、Commerce プレビュー環境は完全なコマース経験を提供し、顧客および実装パートナーが製品の評価、フィードバックの提供、およびフィット/ギャップ分析を行うために使用できます。

## <a name="limitations-of-the-commerce-preview-environment"></a>Commerce プレビュー環境の制限事項

Commerce プレビュー環境では Commerce 機能の完全なセットが提供されますが、いくつかの制限事項があります。

- Commerce プレビュー環境自体には地理的な制限事項はありませんが、Retail Cloud Scale Unit (RCSU) および E コマース アプリケーションなどの環境のコンポーネントは米国でのみプロビジョニングできます。
- Commerce プレビュー環境の使用には、E コマースのプロビジョニング日から 30 日間という期限設定があります。
- Commerce プレビュー環境は、デモ トポロジを使用する環境でのみ正常に展開および初期化でき、環境のすべてのコンポーネントが単一の仮想マシン (VM) に展開されます。 この OneBox VMトポロジの主な制限事項は、プレビュー環境がサポートできる同時ユーザー数です。
- Commerce プレビュー環境は、Commerce 製品の一般提供 (GA) 前に評価できます。 新しいデモ環境は GA 後に使用できます。

## <a name="get-started"></a>はじめに

Commerce プレビュー環境をプロビジョニングする方法については、[Commerce プレビュー環境のプロビジョニング](provisioning-guide.md) を参照してください。

## <a name="additional-resources"></a>追加リソース

[Dynamics 365 Commerce プレビュー環境のプロビジョニング](provisioning-guide.md)

[Dynamics 365 Commerce レビュー環境のコンフィギュレーション](cpe-post-provisioning.md)

[Dynamics 365 Commerce プレビュー環境のオプション機能のコンフィギュレーション](cpe-optional-features.md)

[Dynamics 365 Commerce プレビュー環境に関するよく寄せられる質問](cpe-faq.md)
