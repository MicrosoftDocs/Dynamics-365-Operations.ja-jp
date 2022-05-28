---
title: Human Resources の機能を管理する
description: このトピックでは、機能管理の機能および使用方法について説明します。
author: twheeloc
ms.date: 08/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FeatureManagementWorkspace
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 914752e71871ce05255fbb52ad6a0ee8f0226a4c
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/04/2022
ms.locfileid: "8687306"
---
# <a name="manage-features-in-human-resources"></a>Human Resources の機能を管理する


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Microsoft Dynamics 365 Human Resources の新機能の継続的なロールアウトの一環として、お客様にできるだけ早く新しい機能を体験していただきたいと思います。 一般公開される準備がほぼ整っており、広範なテストを経たプレビュー機能を提供します。 一般提供にリリースする前に、顧客フィードバックおよび検証の最終ラウンドを探しています。

Human Resources の新機能に関する詳細は、[Human Resources の新機能](hr-admin-whats-new.md) および [Dynamics 365 と Power Platform リリース プラン](/dynamics365/release-plans/?panel=products1#pivot=products) を参照してください。

**機能管理** ワークスペースでは、各リリースで可能になる機能の一覧を表示できます。 既定では、新機能が無効になっています。 ワークスペースを使用してそれらを有効にし、それらのドキュメントを参照できます。 機能管理の詳細については [機能管理の概要](../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) を参照してください。

すべての新機能は少なくとも 30 日間、通常は 30-60 日間、プレビューのままになります。 主な機能は、通常、プレビュー期間に従って毎年 10 月と 4 月に使用可能です。 **機能管理** ワークスペースに新しい機能が表示されたら、すぐにそれらをオンにすることができます。 一部の機能は既定でオンになっている場合があります。

機能が一般に使用可能になったら、運用環境でオンまたはオフにすることができます。 **機能管理** ワークスペースは、プレビュー機能が必須になるタイミングを示します。 この日付は、通常、半年のリリース計画に沿って 10 月 1 日または 4 月 1 日になっています。 必須機能を無効にすることはできません。 必須になるまでは、すべての環境で機能を有効または無効にすることができます。

## <a name="enable-or-disable-preview-features"></a>プレビュー機能の有効化または無効化

プレビュー機能にアクセスするには、まず、環境でプレビュー機能を有効にする必要があります。 プレビュー機能の有効化または無効化は、環境に特有のものです。

> [!IMPORTANT]
> プレビュー機能は **サンドボックス** 環境でのみ有効になります。 プレビュー機能をオンにすると、その環境内の組織にいるすべてのユーザーに対してその機能が有効になります。 プレビュー機能をオフにすると、プレビュー機能が無効になり、ユーザーがアクセスできないようになります。 プレビュー機能は、Human Resources でサポートが制限されます。 プライバシーとセキュリティ対策の使用は少なく、Human Resources サービス レベル アグリーメント (SLA) には含まれません。 個人のデータ (つまり、ユーザーを識別する任意の情報)、または法律上または規制順守要件の対象となるその他のデータを処理するプレビュー機能を使用しないでください。

1. 人事管理では、**システム管理** を選択します。

2. **機能管理** タイルを選択します。

3. プレビュー機能を有効にするには、一覧から選択して **有効化** を選択します。 プレビュー機能を無効にするには、一覧から選択して **無効化** を選択します。

## <a name="enable-or-disable-benefits-management"></a>福利厚生の管理の有効化または無効化

福利厚生の管理を有効にするには、[プレビュー機能の有効化または無効化](hr-admin-manage-features.md?enable-or-disable-preview-features) と同じ手順を使用します。

> [!IMPORTANT]
> 有効にした後は、**実稼働** 環境で福利厚生の管理を無効にすることはできません。 ただし、**サンドボックス** 環境では、福利厚生の管理を無効にすることができます。

給付金管理の構成と使用の詳細については、[給付金管理の概要](hr-benefits-management-overview.md) を参照してください。

給付金管理では、**給付金** ワークスペースの機能が置き換えられます。 給付金管理のプレビュー機能を有効にすると、**給付金** ワークスペースの次のフォームにアクセスできなくなります。

- **福利厚生**
- **給付金の要素**
- **貢献度計算レート**
- **給付金登録の結果**
- **給付金の期限切れと延長の結果**
- **給付金の適格性ポリシー ルール タイプ**
- **給付金の適格性ポリシー**
- **適格性イベント**

これらのページの情報は、読み取り専用モードで表示できます。 情報を編集する場合は、まず福利厚生の管理を無効にする必要があります (**サンドボックス** 環境にのみ適用)。

## <a name="enable-or-disable-leave-and-absence"></a>休暇および欠勤の有効化または無効化

休暇および欠勤を有効にするには、[プレビュー機能の有効化または無効化](hr-admin-manage-features.md?enable-or-disable-preview-features) と同じ手順を使用します。

> [!IMPORTANT]
> 有効にした後に 休暇および欠勤の **複数の休暇タイプ** 機能を無効にすることはできません。 これは、**サンドボックス** 環境と **実稼働** 環境の両方に適用されます。

休暇および欠勤のプレビュー機能の詳細については、[休暇および欠勤のプレビュー機能](hr-leave-and-absence-overview.md?leave-and-absence-preview-features) を参照してください。

## <a name="send-us-feedback"></a>フィードバックをお送りください

これらのプレビュー機能の使用経験に関するご意見をお聞かせください。 その他の機能を使用する際に、以下のサイトにて、フィードバックを定期的に転記することをお勧めします。

- [コミュニティ](https://community.dynamics.com/enterprise/f/759?pi53869=0&category=Talent) – このサイトは、ユーザーが使用ケースを説明したり、質問したり、およびコミュニティ ヘルプを得られる優れたリソースです。
- 製品に必要な機能、または既存の機能に対して行われるべき変更についてお知らせください。 [Human Resources のアイデア](https://powerusers.microsoft.com/t5/Ideas-for-Human-Resources/idb-p/HumanResources) で製品アイデアを提案します。
    
フィードバックまたは製品のレビューの送信には個人データ (ユーザーを識別できる任意の情報) を含めないでください。 収集した情報はさらに分析されることがありますが、該当するプライバシーに関する法律の下で要求に回答するためには使用されません。 これらのプログラムで個別に収集された個人データは、[Microsoft のプライバシーに関する声明](https://privacy.microsoft.com/privacystatement) の対象となります。

## <a name="see-also"></a>参照

- [Human Resources の新機能](hr-admin-whats-new.md)
- [Dynamics 365 および Power Platform リリース プラン](/dynamics365/release-plans/?panel=products1#pivot=products)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
