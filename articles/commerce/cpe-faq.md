---
title: Dynamics 365 Commerce の評価環境に関するよく寄せられる質問
description: このトピックでは、Microsoft Dynamics 365 Commerce の評価環境についてよく寄せられる質問に対する回答を示します。
author: v-chgri
manager: annbe
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: v-chgri
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 241853c12c5b6a7fdbd1cf7353b4274f4dd99cc1
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5213893"
---
# <a name="dynamics-365-commerce-evaluation-environment-faq"></a>Dynamics 365 Commerce 評価環境に関してよく寄せられる質問

[!include [banner](includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 Commerce の評価環境についてよく寄せられる質問に対する回答を示します。

**現在 Retail を実装する顧客に対して、コマースの評価環境を eコマース店舗として使用できますか ?**

No. コマースの評価環境は評価用にのみ使用されます。 Retail を実装する顧客に環境が必要な場合は、Microsoft にお問い合わせください。

**コマースの評価環境を使用して、Retail を実装する既存のアプリケーション/環境の上に eコマース機能をプロビジョニングできますか ?**

できません (多くの場合)。 コマースの評価コンポーネントは、前提条件とプロビジョニング ガイドで指定されている構成に一致する環境でのみ利用できます。 また、10.0.8 以前の初期リリース版でデプロイされた環境では、必要となる基本デモ データは利用できません。 

**Microsoft Dynamics Lifecycle Services (LCS) を介して Microsoft Azure で コマースの評価環境をデプロイするには、どのような費用がかかりますか ?**

従来の Dynamics 365 Finance / Dynamics 365 Supply Chain Management / Dynamics 365 Commerce 本部のデモ環境 (仮想マシン \[VM \]) は、Azure サブスクリプションでホストされます。 [Azure 価格計算ツール](https://azure.microsoft.com/pricing/calculator/) を使用してこのコストを見積もることができます。

Commerce Scale Unit、コマース サイト ビルダー、eコマース サイトなどのコンポーネントは、software as a service (SaaS) として提供され、Microsoft がホストしています。

**コマースの評価環境で現在サポートされている Azure 地域はどこですか ?**

コマースの評価環境は、北米地域でのみデプロイ可能です。

**完全な OneBox 仮想マシン (VM) オプションを含む、ダウンロード可能な仮想ハード ディスク (VHD) はありますか ?**

Dynamics 365 Commerce と Commerce Scale Unit は、完全に software as a service (SaaS) であり、クラウドでホストされている必要があります。

**コマースの評価環境は、どのくらいの期間使用できますか ?**

コマースの評価環境には、Commerce Scale Unit、コマース サイト ビルダーなどの SaaS コンポーネントが提供された日から30日間の期間制限が設定されています。

**コマースの評価環境の期限設定は延長できますか ?**

制限時間の延長は例外対応となり、状況に応じて考慮されます。 Microsoft パートナーの連絡先にお問い合わせください。

## <a name="additional-resources"></a>追加リソース

[Dynamics 365 Commerce 評価環境の概要](cpe-overview.md)

[Dynamics 365 Commerce 評価環境をプロビジョニングする](provisioning-guide.md)

[Dynamics 365 Commerce の評価環境を構成する](cpe-post-provisioning.md)

[Dynamics 365 Commerce 評価環境で BOPIS を構成する](cpe-bopis.md)

[Dynamics 365 Commerce 評価環境のオプション機能を構成する](cpe-optional-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]