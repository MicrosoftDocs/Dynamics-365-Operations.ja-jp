---
title: Dynamics 365 Commerce の評価環境に関するよく寄せられる質問
description: このトピックでは、Microsoft Dynamics 365 Commerce の評価環境についてよく寄せられる質問に対する回答を示します。
author: v-chgri
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: e8a3e760353b351d42aff82c0d372d2aca350cd2
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/13/2021
ms.locfileid: "7343561"
---
# <a name="dynamics-365-commerce-evaluation-environment-faq"></a>Dynamics 365 Commerce 評価環境に関してよく寄せられる質問

[!include [banner](includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 Commerce の評価環境についてよく寄せられる質問に対する回答を示します。

## <a name="can-we-use-the-commerce-evaluation-environment-as-an-e-commerce-storefront-for-customers-that-currently-implement-retail"></a>現在 Retail を実装する顧客に対して、コマースの評価環境を eコマース店舗として使用できますか ?

No. コマースの評価環境は評価用にのみ使用されます。 Retail を実装する顧客に環境が必要な場合は、Microsoft にお問い合わせください。

## <a name="can-the-commerce-evaluation-environment-be-used-to-provision-the-e-commerce-features-on-top-of-an-existing-applicationenvironment-that-implements-retail"></a>コマースの評価環境を使用して、Retail を実装する既存のアプリケーション/環境の上に eコマース機能をプロビジョニングできますか ?

できません (多くの場合)。 コマースの評価コンポーネントは、前提条件とプロビジョニング ガイドで指定されている構成に一致する環境でのみ利用できます。 また、10.0.8 以前の初期リリース版でデプロイされた環境では、必要となる基本デモ データは利用できません。 

## <a name="what-costs-are-involved-in-deploying-the-commerce-evaluation-environment-on-microsoft-azure-via-microsoft-dynamics-lifecycle-services-lcs"></a>Microsoft Dynamics Lifecycle Services (LCS) を介して、Microsoft Azure でコマースの評価環境を展開するには、どのような費用がかかりますか?

従来の Dynamics 365 Finance / Dynamics 365 Supply Chain Management / Dynamics 365 Commerce 本部のデモ環境 (仮想マシン \[VM \]) は、Azure サブスクリプションでホストされます。 [Azure 価格計算ツール](https://azure.microsoft.com/pricing/calculator/) を使用してこのコストを見積もることができます。

Commerce Scale Unit、コマース サイト ビルダー、eコマース サイトなどのコンポーネントは、software as a service (SaaS) として提供され、Microsoft がホストしています。

## <a name="which-azure-geographies-are-currently-supported-for-the-commerce-evaluation-environment"></a>コマースの評価環境で現在サポートされている Azure 地域はどこですか ?

コマースの評価環境は、北米地域でのみデプロイ可能です。

## <a name="is-there-a-downloadable-virtual-hard-disk-vhd-that-has-the-complete-onebox-virtual-machine-vm-option"></a>完全な OneBox 仮想マシン (VM) オプションを含む、ダウンロード可能な仮想ハード ディスク (VHD) はありますか ?

Dynamics 365 Commerce と Commerce Scale Unit は、完全に software as a service (SaaS) であり、クラウドでホストされている必要があります。

## <a name="how-long-can-the-commerce-evaluation-environment-be-used"></a>コマースの評価環境は、どのくらいの期間使用できますか ?

コマースの評価環境には、Commerce Scale Unit、コマース サイト ビルダーなどの SaaS コンポーネントが提供された日から30日間の期間制限が設定されています。

## <a name="can-i-extend-the-time-limit-for-my-commerce-evaluation-environment"></a>コマースの評価環境の期限設定は延長できますか ?

制限時間の延長は例外対応となり、状況に応じて考慮されます。 Microsoft パートナーの連絡先にお問い合わせください。

## <a name="additional-resources"></a>追加リソース

[Dynamics 365 Commerce 評価環境の概要](cpe-overview.md)

[Dynamics 365 Commerce 評価環境をプロビジョニングする](provisioning-guide.md)

[Dynamics 365 Commerce の評価環境を構成する](cpe-post-provisioning.md)

[Dynamics 365 Commerce 評価環境で BOPIS を構成する](cpe-bopis.md)

[Dynamics 365 Commerce 評価環境のオプション機能を構成する](cpe-optional-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
