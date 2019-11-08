---
title: Dynamics 365 Talent - Core HR の新機能および変更された機能 (2018 年 8 月)
description: このトピックでは、Microsoft Dynamics 365 Talent - Core HR の新機能または変更された機能について説明します。
author: Darinkramer
manager: AnnBe
ms.date: 08/27/2018
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
ms.search.validFrom: 2018-08-27
ms.dyn365.ops.version: Talent August 2018 update
ms.openlocfilehash: 14dc4d2a1b69f58d6d9c2466b2bcaf4f9185931e
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/03/2019
ms.locfileid: "2550277"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent---core-hr-august-2018"></a>Dynamics 365 Talent - Core HR の新機能および変更された機能 (2018 年 8 月)

[!include [banner](includes/banner.md)]

**ビルド 8.1.104**

このトピックでは、Dynamics 365 Talent: Core HR の新機能または変更された機能について説明します。

## <a name="view-expiring-records-in-manager-self-service"></a>マネージャー セルフ サービスで期限が切れるレコードの表示

マネージャー セルフ サービスで期限が切れるレコードを表示できるようになります。 新しいオプションでは、管理者が表示用に使用する情報を構成できるようにします。 コピーされるフィールドは次のとおりです。

-   証明書

-   ID 番号

-   猶予期間

-   審査

-   テスト

この機能は、期限切れになるレコードを検索する日数の範囲も指定できるようにします。

## <a name="configurable-transfer-actions"></a>構成可能な移動アクション

転送要求の入力中に利用可能なオプションをロール別に構成できます。 この機能は、組織内のロール間でさらに柔軟性を提供します。

たとえば、従業員の転送を要求するマネージャには、報酬金額を提案または入力する、または転送要求に関連付けられるタスク リストを選択するためのアクセス権がない可能性があります。 この場合、マネージャは転送要求を作成または送信できますが、報酬またはタスク リストの割り当てを入力することはできません。 この同じ構成で、HR は新しい報酬値を割り当てると共に、転送完了の結果として完了するための任意の追加のチェックリストを割り当てることができます。

既定では、新しい構成オプションはこの更新の前に処理能力を変更しないよう設定されています。

## <a name="leave-and-absence"></a>休暇

追加の日付フィールドが休暇で使用できるようになりました。

この機能により、特定の従業員の日付を使用する計画レベルで見越計上期間の基準を設定できます。 これにより、休暇の見越計上処理中に使用される計画の開始日以外の日付を使用できます。 従業員の特定の日付のオプションには、次の値が含まれます。

-   カスタム (この更新前に使用可能)

-   記念日

-   元の採用日付

-   勤続日数

-   作業者の調整済開始日

-   作業者の開始日

従業員の特定の日付のいずれかを使用するように構成する場合は、登録プロセスでは指定された日付を使用して見越計上期間を計算します。 見越計上期間の基準は、見越計上処理中に何が使用されるかを理解するための従業員の計画登録にも表示されます。

## <a name="microsoft-word-integration"></a>Microsoft Word 統合

ドキュメント テンプレートは Core HR 全体で有効になります。 この機能により、作成した Word テンプレートに基づく文字およびレポートを作成できます。

この機能に関する追加情報は、[Office 統合のチュートリアル](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/office-integration/office-integration-tutorial?toc=/dynamics365/unified-operations/talent/toc.json) で参照できます。


## <a name="other-fixes"></a>その他の修正

今回のリリースには、複数のバグ修正、新しいエンティティの追加、既存のエンティティの修正、およびローカライズされたラベルの変更が含まれます。
