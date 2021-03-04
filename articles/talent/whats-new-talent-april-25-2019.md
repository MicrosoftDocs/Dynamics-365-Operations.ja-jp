---
title: Dynamics 365 Talent (2019 年 4 月 23 日) の新機能および変更された機能
description: このトピックでは、Microsoft Dynamics 365 Talent の新機能または変更された機能について説明します。
author: Darinkramer
manager: AnnBe
ms.date: 04/23/2019
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
ms.search.validFrom: 2019-04-23
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 53faf972759c8f770017fcd3a87920410988e626
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/17/2020
ms.locfileid: "4527189"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-april-23-2019"></a>Dynamics 365 Talent (2019 年 4 月 23 日) の新機能および変更された機能

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

このトピックでは、Dynamics 365 Talent の新機能または変更された機能について説明します。

## <a name="changes-in-attract"></a>Attract の変更
今回のリリースには、Dynamics 365 Talent: Attract のマイナーなバグ修正が含まれています。

## <a name="changes-in-onboard"></a>Onboard の変更
今回のリリースには、Dynamics 365 Talent: Onboard のマイナーなバグ修正が含まれています。

## <a name="changes-in-core-hr"></a>Core HR の変更
このセクションに記載された変更は、ビルド番号 8.1.2253 に適用されます。 かっこ内の数字は、Lifecycle Services (LCS) のサポート番号を参照しています。

### <a name="common-data-service-entity-support-for-custom-fields"></a>カスタム フィールドに対する Common Data Service エンティティのサポート
今週のリリースでは、次のエンティティがカスタム フィールドをサポートするようになりました。報酬レベル、福利厚生オプション、スキルのタイプ、および報酬地域です。

### <a name="additional-odata-entities-302992"></a>追加の OData エンティティ (302992)
現在、次のエンティティで OData がサポートされています。作業者の職務経験および作業者の教育です。
   
### <a name="performance-journal-attachments-for-managers-and-employees-308248"></a>管理者および従業員の業績仕訳帳の添付ファイル (308248)
今回のリリースでは、業績仕訳帳エントリの作成および更新時に、マネージャと従業員の両方に対して添付ファイルが使用可能になりました。

### <a name="employee-rehire-flag-always-available-310047"></a>従業員再雇用フラグは常に使用可能 (310047)
従業員の再雇用オプションが、退職プロセス以外の更新で使用可能になりました。 

### <a name="cannot-change-the-name-of-my-payment-method-308815"></a>**自分の支払方法** の名前を変更することはできません (308815)
従業員セルフ サービスにおいて **自分の支払方法** のラベルを変更できるように、個人用設定が有効になっています。

### <a name="financial-dimensions-against-a-position-cant-be-deleted-293908"></a>職位に対する財務分析コードは削除できません (293908)
既存の職位および会社間の財務分析コードに対する変更の要求時に財務分析コードを削除することができるようになりました。 

### <a name="customer-is-unable-to-publish-back-data-into-talent-when-opening-the-data-from-excel-302955"></a>Excel からのデータを開く時に、顧客は Talent にデータを戻して公開することができない (302955)
この変更により、関連するテーブルを使用した場合の公開の問題が修正されます。

## <a name="in-preview"></a>プレビュー

### <a name="allow-reason-codes-to-be-specified-on-leave-types"></a>理由コードを休暇タイプに指定できるようにする
組織は、休暇申請に関する追加情報が必要な場合があります。 休暇タイプに理由コードを指定し、従業員が休暇申請で理由コードを選択できるようになりました。

### <a name="require-reason-codes-for-certain-leave-types-on-time-off-requests"></a>休暇申請で特定の休暇タイプに理由コードが必要
従業員が休暇を送信するときに、組織は特定の休暇タイプに理由コードを要求することがあります。 これは、会社の方針または規制要件が原因である可能性があります。 どの休暇タイプに理由コードが必要かを指定できるようになりました。また、従業員に休暇申請で休暇タイプに理由コードを指定するように要求できます。

### <a name="provide-leave-and-absence-transaction-list-for-hr"></a>HR の休暇および欠勤トランザクション リストを提供します。
従業員の休暇を追跡し、どのように計算するかを理解することにより、HR が従業員の質問に答えるのに役立つだけでなく、従業員に正確な休暇の付与ができるようになります。 HR は、残高の背後にある理由を確認するための、トランザクション (交付、見越、調整、および要求) の表示が新しくなりました。

## <a name="coming-soon"></a>間もなく公開

### <a name="improvements-to-the-user-interface-for-duplicate-employee-check"></a>重複する従業員チェックのためのユーザー インターフェイスの改良
この変更により、名前のフィールドを入力すると重複が検出され、見つかった重複の数がステータスに表示されるようになります。 提供されたリンクを選択して新しいページを開き、検出された一致を使用するかどうかを評価できます。 データ入力の中断を回避するために、重複フォームは自動的に開きません。
## <a name="known-issues"></a>既知の問題

### <a name="email-support-for-alerts"></a>アラートの電子メールサポート
Finance and Operations の Platform update 26 を使用すると、あるイベントによってトリガーされたときに、自動的に連絡先に電子メール通知を送信する警告ルールを作成できます。


[!INCLUDE[footer-include](../includes/footer-banner.md)]