---
title: Dynamics 365 for Talent Core HR の新機能および変更された機能 (2018 年 10 月 16 日)
description: このトピックでは、Microsoft Dynamics 365 for Talent Core HR の新機能または変更された機能について説明します。
author: Darinkramer
manager: AnnBe
ms.date: 10/22/2018
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
ms.search.validFrom: 2018-10-22
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 7da597a682006cddb44ff9354813b07c15c1a449
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "305209"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-october-19-2018"></a>Dynamics 365 for Talent Core HR の新機能および変更された機能 (2018 年 10 月 19 日)

[!include[banner](includes/banner.md)]

**ビルド 8.1.1067**

このトピックでは、Core HR の新機能または変更された機能について説明します。

## <a name="allow-managers-to-update-time-off-requests"></a>管理者の休暇時間要求更新の許可

従業員の休暇時間要求は、ワークフローを通じて承認された後に更新する必要がある場合があります。 多くの場合、これらの更新は従業員の代理としてマネージャーにより行われます。 この新しい機能により、休暇時間の更新または休暇時間要求のキャンセルを従業員の代理としてマネージャーが行う機能が提供されます。 この能力は、**人材パラメーター**上で設定される**代わりに作業する**パラメーターにより制御されます。 
 
## <a name="allow-hr-to-update-time-off-requests"></a>HR の休暇時間要求更新の許可

上記の機能と同様に、従業員の休暇時間要求は、ワークフローを通じてすでに承認された後に更新する必要がある場合があります。 この機能により、HR ユーザーが休暇時間要求を更新する機能が提供されます。 **人員**ワークスペースおよび**作業者**ページにて、**休暇の表示**という新しいオプションを使用して、機能は有効になります。 それらのページ上で、マネージャーがアクションを実行するのと同様の方法で、HR ユーザーは要求の表示および休暇トランザクションの更新を行うことができます。

この機能へのアクセスを制御するセキュリティ職務権限は次のとおりです。
- 職務権限: 作業者固有の休暇プロセスの管理。
- 権限: すべての作業者の休暇申請の管理。

## <a name="other-changes"></a>その他の変更
このリリースでは次の更新が行われました。
- 作業者の採用アクションへの変更により、**ワークフロー完了**状態から移動できなくなることはありません。
- 雇用開始日がなくても採用レコードを作成できるようになりました。
- 従業員のセルフ サービスに表示されるコースに対する Dynamics 365 Talent の登録日について、タイム ゾーン オフセットを日付に適用できるようになりました。
- Excel ファイルは、**従業員エンティティ**を使用し、エラーを発生させずに複数回インポートすることができます。

## <a name="known-issue"></a>既知の問題

- **問題**: 作業者に新しい添付ファイルを追加する時、**新規**および**編集**ボタンが灰色表示になります。 
- **回避策:** 添付ファイル ページを開く前に、**作業者**ページの Factbox が閉じていることを確認します。 **作業者**ページが読み込まれる時、FactBoxes が閉じている場合には、添付ファイルボタンが有効になります。 (この問題は次のプラットフォーム更新プログラムで修正されます。)
