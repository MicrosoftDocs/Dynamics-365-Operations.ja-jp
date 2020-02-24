---
title: Dynamics 365 Talent の新機能または変更された機能 (2019 年 7 月 30 日)
description: このトピックでは、Microsoft Dynamics 365 Talent の新機能または変更された機能について説明します。
author: Darinkramer
manager: AnnBe
ms.date: 07/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 311042caf6a391a06c7e2d8c4c2c2f6e1f855437
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/03/2020
ms.locfileid: "3006290"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-july-30-2019"></a>Dynamics 365 Talent の新機能または変更された機能 (2019 年 7 月 30 日)

このトピックでは、Dynamics 365 Talent の新機能または変更された機能について説明します。

## <a name="changes-in-attract"></a>Attract の変更
今回のリリースには、Dynamics 365 Talent: Attract のマイナーなバグ修正が含まれています。

## <a name="changes-in-onboard"></a>Onboard の変更
今回のリリースには、Dynamics 365 Talent: Onboard のマイナーなバグ修正が含まれています。

## <a name="changes-in-core-hr"></a>Core HR の変更
このセクションに記載された変更は、ビルド番号 8.1.2409 に適用されます。


### <a name="region-support-for-canada-and-southeast-asia"></a>カナダおよび東南アジアの地域サポート

2019 年 8 月 1 日に、カナダおよび東南アジアの地域で Talent が使用可能になることをお知らせします。 この変更により、カナダおよびアジアの地域で環境を作成できるようになり、それらの場所だけですべての Talent データが管理されるようになります。 新しい環境ダイアログで場所を選択し、[Talent のプロビジョニング](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent) で説明されているように、その環境を LCS での Talent のプロビジョニングに使用することにより、新しい地域に環境を作成することができます。

他の地域からカナダおよびアジア地域への既存のプロジェクトのデータ移行はサポートされていません。 新しいプロジェクトのみ、これら新しくサポートされる地域にプロビジョニングできます。

### <a name="new-active-positions-list-page"></a>新しい有効な職位のリスト ページ

職位に基づくリストのオプションには、**すべての職位**、**有効な職位**、**空いている職位**、および**無効な職位**が含まれるようになりました。 新しい**有効な職位**のリスト ページには、現在の日付の時点で有効になっている職位 (オープンまたは入力済み) のみが表示されます。 

### <a name="allow-course-participants-to-be-added-to-open-courses"></a>コース参加者の空きのあるコースへの追加を許可する

今週の変更により、直属の部下のみを空きのあるコースに登録できるという問題が修正されます。

### <a name="fte-analysis-displaying-incorrect-fte-number"></a>FTE 分析で正しくない FTE 番号が表示される

**FTE 分析**は、**人事管理**の**分析**タブで修正されました。

### <a name="final-comments-label-translation"></a>最終コメント ラベルの翻訳

**最終コメント** ラベルが確認フォームで翻訳されるようになりました。

## <a name="in-preview"></a>プレビュー

### <a name="preview-features-are-enabled-only-in-sandbox-instances"></a>プレビュー機能は、サンドボックス インスタンスでのみ有効です。

Talent の新しいインスタンスをプロビジョニングする時に、インスタンス タイプを**実稼働**または**サンドボックス**のどちらかに指定することができます。 **サンドボックス** タイプのインスタンスにより、新機能を事前にテストできるようになります。 既存の Talent のインスタンスすべては、**実稼働**インスタンス タイプに更新されます。 既存のインスタンスのいずれかを**サンドボックス** インスタンス タイプに更新する場合は、変更要求を開始するよう [サポート](https://docs.microsoft.com/dynamics365/unified-operations/talent/talent-support) に連絡してください。

変更を公開する方法の詳細については、[Talent のプロビジョニング](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent) を参照してください。

### <a name="view-extended-information-for-performance-in-manager-self-service"></a>マネージャー セルフサービスの業績に関する追加情報の確認

新しいオプションにより、マネージャーは自分の直接レポートと拡張レポートの両方の業績を確認できるようになります。 現在、ライン マネージャーは業績目標の割り当てと更新、また新しい確認の発行をすることができます。 また、直属のマネージャーと従業員は業績仕訳の管理および更新を行うことにより、業績確認プロセスを確実に、スムーズに行うことができます。 この変更が実装されると、マネージャーは直接レポートに加えて、拡張レポートの業績関連情報の確認および管理ができるようになります。
