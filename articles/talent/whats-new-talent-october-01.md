---
title: Dynamics 365 for Talent Core HR の新機能および変更された機能 (2018 年 10 月 1 日)
description: このトピックでは、Microsoft Dynamics 365 for Talent Core HR の新機能または変更された機能について説明します。
author: Darinkramer
manager: AnnBe
ms.date: 10/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-10-01
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 15b5fd7095a62aa9b7b79ebfcada667959b756aa
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/19/2019
ms.locfileid: "858747"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-october-1-2018"></a>Dynamics 365 for Talent Core HR の新機能および変更された機能 (2018 年 10 月 1 日)

[!include [banner](includes/banner.md)]

**ビルド 8.1.1035.0**

このトピックでは、Core HR の新機能または変更された機能について説明します。

## <a name="turn-off-electronic-payment-validation"></a>電子支払の検証を無効化する

**従業員セルフ サービス**ワークスペース (ESS) を通してまたは従業員フォームで直接に口座振込の出金を設定した場合、電子支払情報の検証が行われます。 このオプションを使用すると、金額と残余値の検証による確認が不要な場合に、その検証を柔軟に削除できます。 この機能は、要件が異なる外部給与システムと統合している場合に役に立ちます。

## <a name="manager-self-service---add-goals-for-team-members-through-the-team-performance-goals-tile"></a>マネージャー セルフ サービス - チーム業績目標タイルを通じてチーム メンバーの目標の追加

今回のリリースまでは、管理者は、各従業員に関連付けられている業績目標を通して、その従業員個人に目標を追加できます。 この更新により、管理者は**チーム業績目標**タイルにアクセスでき、直属の部下のいずれかを選択して新しい目標を作成できます。

## <a name="manager-self-service---add-reviews-for-team-members-through-the-team-performance-reviews-tile"></a>マネージャー セルフ サービス - チーム業績レビュー タイルを通じてチーム メンバーのレビューの追加

今回のリリースまでは、管理者は、各従業員に関連付けられているレビューを通じて、その従業員個人にレビューを追加できます。 この更新により、管理者は**チーム業績レビュー**タイルにアクセスでき、直属の部下のいずれかを選択して新しいレビューを作成できます。

## <a name="configure-proration-options-by-leave-plan"></a>休暇計画による比例配分オプションのコンフィギュレーション

組織は、従業員の入社日および退社日に基づいて、休暇を別々に付与します。 一部の組織によっては、従業員は開始日に全額配賦され、他の従業員は報奨を比例配分します。 このリリースでは、組織内の入退社者に対する比例配分および見越計上を選択する方法に関する新しいオプションが提供されています。 オプションには次のものがあります: 比例配分、完全な見越計上、および見越計上なし。

## <a name="other-changes"></a>その他の変更

-   更新された従業員エンティティ - **個人**タイトルは、Excel アドイン/データ管理を使用して更新できるようになりました。

-   支払情報の従業員セルフ サービスで、**削除**および**無効化**ボタンの削除を許可するセキュリティ変更。

## <a name="known-issue"></a>既知の問題

-   **問題:** 作業者に新しい添付ファイルを追加する場合、**新規**および**編集**ボタンは灰色表示です。**回避策:** 添付ファイル ページを開く前に、**作業者**ページの Factbox が閉じていることを確認します。 **作業者**ページが読み込まれるとき FactBoxes が閉じている場合、**添付ファイル**ボタンが有効になります。 (この問題は次のプラットフォーム更新プログラムで修正されます。)
