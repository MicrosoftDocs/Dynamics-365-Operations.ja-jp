---
title: Dynamics 365 Talent の新機能および変更された機能 (2019 年 3 月 26 日)
description: このトピックでは、Microsoft Dynamics 365 Talent の新機能または変更された機能について説明します。
author: Darinkramer
manager: AnnBe
ms.date: 03/26/2019
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
ms.search.validFrom: 2019-03-26
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 17eae6c2aa2a1305b1d6f403c595c022f71da48f
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/17/2020
ms.locfileid: "4529093"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-march-26-2019"></a>Dynamics 365 Talent の新機能および変更された機能 (2019 年 3 月 26 日)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

このトピックでは、Dynamics 365 Talent の新機能または変更された機能について説明します。

## <a name="changes-in-attract"></a>Attract の変更

### <a name="enhancements-to-interview-scheduling"></a>面接のスケジューリングを拡張します
面接のスケジューリングでは、次の機能拡張が使用可能です。

- 採用担当者または採用マネージャーは、面接者にフィードバックを送信するよう手動でアラームをトリガーできるようになりました。 アラーム用の関連付けられている電子メール テンプレートも設定可能です。
- 面接の概要を候補者と共有中は、面接スケジューラは、面接者の名前を非表示にし、インタビューの概要ビューから行を非表示にすることを選択できます。

## <a name="changes-in-onboard"></a>Onboard の変更

### <a name="embedded-images-in-activities"></a>活動の埋め込み画像
画像を直接活動に埋め込むことができるようになりました。 Web から画像をコピーして貼り付けることができるほかに、ローカル ファイル システムから画像をアップロードすることもできます。 活動のサイズは、1 MB に制限されます。 画像が大きすぎる場合は、サイズを変更し、もう一度アップロードしてください。

[![マッピング](./media/embedimages.png)](./media/embedimages.png)

今回のリリースには、Dynamics 365 Talent: Onboard のマイナーなバグ修正が含まれています。

## <a name="changes-in-core-hr"></a>Core HR の変更
**ビルド 8.1.2210**

### <a name="custom-field-support-available-for-select-entities-in-common-data-service"></a>Common Data Service でエンティティに選択可能なカスタム フィールド サポート 

次の Common Data Service エンティティは、Talent で作成した顧客のフィールドに対応するようになりました。

- ワーカー
- 出身民族
- 退役軍人ステータス
- 言語コード
- ジョブ
- 職務タイプ
- 職務権限
- 配置
- 職位タイプ
 
### <a name="employment-history-not-displayed-chronologically"></a>雇用履歴は時系列順に表示されていません
この変更により、雇用履歴ページに会社とは関係なく雇用記録が時系列順で表示されるようになりました。 並び替えのオプションを使用して会社別に並び替えることもできます。

### <a name="fixed-compensation-plans-dont-appear-when-restricting-user-by-company-in-security"></a>会社ごとにセキュリティを制限している場合、固定報酬プランは表示されません。
今回のリリースでは、会社ごとにセキュリティを制限している場合、固定報酬プランが表示されるようになりました。 すべてのセキュリティ設定が遵守され、ユーザーにアクセス許可がある会社に対しては固定プランが表示されます。 

### <a name="cant-delete-job-records-using-open-in-excel-option-in-talent"></a>Talent の Excel で開くオプションを使用してジョブ レコードを削除できない
このリリースでは、Talent の **Excel で開く** オプションを使用して、ジョブ レコードを削除できるようになりました。

### <a name="upgrade-to-common-data-service"></a>Common Data Service へのアップグレード
Common Data Service へのアップグレードの期限が近づいています。 データベースをアップグレードする必要があるかどうかを決定するために、Power Apps 管理者センターにサインインします。 期限およびアップグレードに必要な手順の詳細については、[Common Data Service へのアップグレード](https://docs.microsoft.com/common-data-service/upgradecds/introduction-upgrade-cds) を参照してください。

## <a name="in-preview"></a>プレビュー

プレビュー機能の有効化については、[Microsoft Dynamics 365 Talent のプレビュー機能の利用](./access-preview-feature.md) を参照してください。

### <a name="allow-reason-codes-to-be-specified-on-leave-types"></a>理由コードを休暇タイプに指定できるようにする
組織は、休暇申請に関連する追加情報が必要な場合があります。 この情報を取得するには、従業員は休暇申請に理由コードを含める必要があります。 このリリースでは、休暇タイプに関連付けられている理由コードを指定し、従業員が休暇申請で理由コードを選択できるようになりました。

### <a name="configure-reason-codes-to-be-required-when-submitting-time-off-for-certain-leave-types"></a>特定の休暇タイプの休暇を送信するときに必要となる理由コードを設定する
従業員が休暇を送信するときに、組織は特定の休暇タイプに理由コードを設定することを要求することがあります。 これは、その国/地域の法的な要求事項または会社ポリシーに基づいて必要となる場合があります。 このリリースでは、HR が理由コードを必要とする休暇タイプを指定できるようになりました。 これは、休暇に理由コードが必要なところで、従業員が休暇申請を送信したときに実施されます。

## <a name="coming-soon"></a>間もなく公開

###  <a name="advanced-compensation-security-fixed-and-variable"></a>高度な報酬セキュリティ (固定および変動)
多くの組織では、報酬および福利厚生の管理者は特定の報酬レコードにのみアクセスできます。 これらは、経営幹部または地域の従業員向けのものである可能性があります。 この変更により、HR は組織内のさまざまな従業員グループの報酬プランを管理および維持できます。 固定および変動プランにはセキュリティ ロールを割り当てることができます。これは、プランへのアクセス権とプランに関連する従業員データ (給与または特別償却レコードなど) を決定します。 アクセス権を付与されたロールのみが、これらの従業員の報酬を処理できます。

###  <a name="email-support-for-alerts"></a>アラートの電子メールサポート
Finance and Operations の Platform update 25 を使用すると、あるイベントによってトリガーされたときに、自動的に連絡先に電子メール通知を送信する警告ルールを作成できます。 

### <a name="duplicate-employee-checks-user-interface-changes"></a>重複する従業員チェック : ユーザー インターフェイスの変更
この変更により、名前のフィールドを入力すると重複が検出され、見つかった重複の数がステータスに表示されるようになります。 提供されたリンクを選択して新しいページを開き、検出された一致を使用するかどうかを評価できます。 データ入力の中断を回避するために、重複フォームは自動的に開きません。
