---
title: Dynamics 365 Talent (2020 年 1 月 21 日) の新機能および変更された機能
description: この記事では、Microsoft Dynamics 365 Talent の新機能または変更された機能について説明します。
author: Darinkramer
manager: AnnBe
ms.date: 01/21/2020
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
ms.search.validFrom: 2020-01-21
ms.dyn365.ops.version: Talent
ms.openlocfilehash: e9dee64e94c904cfe07c6a7766f6a60b1d60a2db
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/17/2020
ms.locfileid: "4528125"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-january-21-2020"></a>Dynamics 365 Talent (2020 年 1 月 21 日) の新機能および変更された機能

[!include [banner](includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

この記事では、Dynamics 365 Talent の新機能および変更された機能について説明します。

## <a name="changes-in-attract"></a>Attract の変更

今回のリリースには、Dynamics 365 Talent: Attract のマイナーなバグ修正が含まれています。 最新の発表 [Dynamics 365 Human Resources でより成功する要員を構築する](https://cloudblogs.microsoft.com/dynamics365/bdm/2019/12/06/building-a-more-successful-workforce-with-dynamics-365-human-resources/) をサポートするための Attract への機能が追加されました。

### <a name="download-environment-data"></a>環境データのダウンロード

管理者は、環境のデータをダウンロードできます。 ZIP ファイルにエクスポートされたすべてのジョブ、候補者、およびコンフィギュレーションを使用して、データは標準の JSON 形式でエクスポートされます。 詳細については、[Attract および Onboard からのデータのエクスポート](https://docs.microsoft.com/dynamics365/talent/attract-onboard-export-data) を参照してください。

### <a name="restricting-access-to-environments-for-non-admin-users"></a>管理者以外のユーザーによる環境へのアクセスを制限する

管理者は、管理者以外のユーザーによる環境へのアクセスを制限できるようになりました。 このアクションを元に戻すことはできません。 詳細については、[Attract へのアクセスの制限](https://docs.microsoft.com/dynamics365/talent/attract-onboard-export-data#restrict-access-to-attract) を参照してください。

## <a name="changes-in-onboard"></a>Onboard の変更

今回のリリースには、Dynamics 365 Talent: Onboard のマイナーなバグ修正が含まれています。

### <a name="exporting-onboarding-guides"></a>研修用ガイドのエクスポート

ユーザーは、すべての研修用ガイドと研修用テンプレートを Word 文書形式でエクスポートできるようになりました。 詳細については、[Attract および Onboard からのデータのエクスポート](https://docs.microsoft.com/dynamics365/talent/attract-onboard-export-data) を参照してください。

## <a name="changes-in-core-hr"></a>Core HR の変更

このセクションに記載された変更は、ビルド番号 8.1.2726 に適用されます。 ヘッダーにあるかっこ内の数字は、Microsoft Dynamics Lifecycle Services (LCS) のサポート番号を参照していることがあります。

### <a name="most-recent-annual-compensation-field-in-verify-employment-form-isnt-consistent-392092"></a>雇用検証フォームの最新の年次報酬フィールドに一貫性がない (392092)

このリリースには、**雇用検証** フォームで会社のセレクターに基づく最新の通貨を常に表示する変更が含まれています。

### <a name="known-as-field-added-to-the-feedback-recipient-lookup-407789"></a>フィードバック受信者のルックアップに追加された呼称フィールド (407789)

パフォーマンス フィードバックを提供する際、作業者のルックアップでは、フィードバックが正しい人に送られるかどうかを判断するための十分な情報が提供されませんでした。 従業員の一意の名前を識別するのに役立つ、**呼称** 列を追加しました。
 
### <a name="hcmworkerpayrollinfo-record-is-created-without-an-association-to-a-worker-394526"></a>HcmWorkerPayrollInfo レコードが作業者への関連付けなしで作成される (394526)

このリリースには、従業員への参照なしで HCMWorkerPayrollInfo レコードを書き込まないようにする変更が含まれます。

### <a name="able-to-edit-department-when-navigating-from-position-hierarchy-341001"></a>職位階層からの移動時に部門を編集可能 (341001)

セキュリティが編集部門へのアクセスを拒否するよう設定された場合、すべてのシナリオを **部門** フォームに移動する際に編集が無効になります。

## <a name="coming-soon"></a>間もなく公開

次の変更により、新しい Common Data Service ソリューションがまもなく利用可能になります。

| 説明 | 計上額 |
| --- | --- |
| **職務/職位** エンティティの変更 | <ul><li>追加された **報酬地域**</li><li>追加された **財務分析コード**</li></ul> |
| **作業者** エンティティの変更 | <ul><li>追加された **名前の順序**</li><li>追加された **自宅から作業**</li><li>追加された **言語**</li><li>追加された **勤続日数**</li><li>追加された **記念日**</li><li>追加された **元の採用日付**</li></ul> |
| **雇用** エンティティの変更 | <ul><li>追加された **財務分析コード**</li><li>追加された **退職理由**</li><li>**移行日** から名前変更された **退職日**</li><li>追加された **猶予期間**</li></ul> |
| **作業者住所** エンティティの変更 | <ul><li>追加された **番地**</li><li>廃止としてマークされた **住所行 1**、**住所行 2**、および **住所行 3**</li></ul> |
| 新しい変動報酬の設定エンティティ | <ul><li>**変動報酬プラン タイプ**</li><li>**変動報酬プラン**</li><li>**給付ルール**</li><li>**変動報酬プラン レベル**</li></ul> |
| 新しい **作業者カレンダー雇用** エンティティ | <ul><li>追加された **作業カレンダー エンティティ**</li></ul> |
