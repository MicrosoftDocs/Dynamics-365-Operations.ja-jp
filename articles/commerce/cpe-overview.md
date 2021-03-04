---
title: Dynamics 365 Commerce 評価環境の概要
description: このトピックでは、Microsoft Dynamics 365 Commerce の環境環境の概要を説明します。
author: v-chgri
manager: annbe
ms.date: 07/16/2020
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
ms.openlocfilehash: 25c0574e8d4502bcb846fba0ddf913d81eded87b
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4413647"
---
# <a name="dynamics-365-commerce-evaluation-environment-overview"></a>Dynamics 365 Commerce 評価環境の概要

[!include [banner](includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 Commerce の環境環境の概要を説明します。

> [!NOTE]
> コマースの評価環境は一般的には提供されておらず、パートナーや顧客からのリクエストに応じて付与されます。 ライセンスの詳細については、Microsoft パートナーにお問い合わせください。

## <a name="overview"></a>概要

コマースの評価環境は、パートナーや見込み顧客にコマース製品を試用できる、 Dynamics 365 Commerce のオプションのエンドツーエンド環境です。

評価環境は、プロビジョニング後に必要となる手順を減らす目的でに、部分的に事前に構成されています。

機能や機能に影響を与えない軽微な制限事項とは別に、コマースの評価環境は完全なコマースの経験を提供し、顧客や実装パートナーが製品の評価、フィードバックの提供、フィット アンド ギャップ分析に使用することができます。

## <a name="limitations-of-the-commerce-evaluation-environment"></a>コマースの評価環境の制限事項

コマースの評価環境では、コマースの機能の完全なセットが提供されますが、いくつかの制限事項があります。

- コマースの評価環境自体には地理的な制限はありませんが、Retail Cloud Scale Unit (RCSU) や eコマース アプリケーションなどの環境の構成要素は、米国内のみでプロビジョニングできます。
- コマースの評価環境の使用には、eコマースのプロビジョニング日から 30 日間という期限の設定があります。
- コマースの評価環境は、環境のすべてのコンポーネントが単一のクラウド ホスト仮想マシン (VM) 上にデプロイされているデモ トポロジを使用する環境でのみ、正常にデプロイや初期化が可能です。 このトポロジの主な制限は、環境が対応できる同時使用ユーザー数です。

## <a name="get-started"></a>はじめに

コマースの評価環境をプロビジョニングする方法については、[コマースのプレビュー環境をプロビジョニングする](provisioning-guide.md) を参照してください。

## <a name="additional-resources"></a>追加リソース

[Dynamics 365 Commerce 評価環境をプロビジョニングする](provisioning-guide.md)

[Dynamics 365 Commerce の評価環境を構成する](cpe-post-provisioning.md)

[Dynamics 365 Commerce 評価環境で BOPIS を構成する](cpe-bopis.md)

[Dynamics 365 Commerce 評価環境のオプション機能を構成する](cpe-optional-features.md)

[Dynamics 365 Commerce 評価環境に関するよく寄せられる質問](cpe-faq.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]