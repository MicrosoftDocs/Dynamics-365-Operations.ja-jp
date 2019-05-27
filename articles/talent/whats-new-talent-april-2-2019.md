---
title: Dynamics 365 for Talent (2019 年 4 月 2 日) の新機能や変更された機能
description: このトピックでは、Microsoft Dynamics 365 for Talent の新機能または変更された機能について説明します。
author: Darinkramer
manager: AnnBe
ms.date: 04/02/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: andreabichsel
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-04-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 8f488b0bf844fc04f07fedfa447073cdeabacc15
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "1518435"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-april-2-2019"></a>Dynamics 365 for Talent (2019 年 4 月 2 日) の新機能や変更された機能

[!include [banner](includes/banner.md)]

このトピックでは、Dynamics 365 for Talent の新機能または変更された機能について説明します。

## <a name="changes-in-attract"></a>Attract の変更

### <a name="approval-emails-in-attract"></a>Attract の電子メールの承認
新しく承認された電子メールでは承認プロセスへの可視性が向上します。 電子メールは、次のシナリオのいずれかが発生したときに、承認者に送信されます。

- 要求元は、承認のためのジョブを送信します。
- ジョブが拒否または承認されます。
- 承認元が 24 時間内に承認の要求を行なっていません。

新しいテンプレートを使用して承認電子メールのコンテンツをカスタマイズできます。

### <a name="application-and-profile-attachments"></a>アプリケーションとプロファイルの添付ファイル
アプリケーションと人材プールプロファイルの**ドキュメント**タブの改良により、ドキュメント名とタイプの両方が表示されるようになりました。

## <a name="changes-in-onboard"></a>Onboard の変更
今回のリリースには、Dynamics 365 Talent: Onboard のマイナーなバグ修正が含まれています。

## <a name="coming-soon-attract-and-onboard"></a>間もなく公開 (Attract および Onboard)

### <a name="lifecycle-services-lcs-integration-with-report-a-problem"></a>問題の報告と Lifecycle Services (LCS) の統合
Attract と Onboard では、問題をレポートする機能を使用してエンドユーザーによって記録された問題は、顧客の LCS プロジェクトでサポートの問題を自動的に作成するようになりました。 その後、管理者は問題をトリアージし、必要に応じて Microsoft に送信することができます。 これは、Core HR がエンド ユーザーのサポートの問題を処理する方法と一致しています。

## <a name="changes-in-core-hr"></a>Core HR の変更
このセクションに記載された変更は、ビルド番号 8.1.2216 に適用されます。

### <a name="platform-update-25"></a>プラットフォーム update 25
プラットフォーム更新プログラム 25 の詳細については [Dynamics 365 for Finance and Operations プラットフォーム更新プログラム 25 (2019 年 4 月)](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-25) を参照してください。

###  <a name="advanced-compensation-security-fixed-and-variable"></a>高度な報酬セキュリティ (固定および変動)
多くの組織では、報酬および福利厚生の管理者は特定の報酬レコードにのみアクセスできます。 これには、経営幹部または地域の従業員向けのレコードが含まれます。 この変更により、HR は組織内のさまざまな従業員グループの報酬プランを管理および維持できます。 セキュリティ ロールを固定および変動プランに割り当てることができます。 これらのセキュリティ ロールによって、給与または特別償却レコードなどのプランおよび関連する従業員データへのアクセスが決定されるため、それらのロールだけが従業員グループの報酬を処理できます。

### <a name="upgrade-to-common-data-service"></a>Common Data Service へのアップグレード
Common Data Service へのアップグレードの期限に近づいています。 データベースをアップグレードする必要があるかどうかを決定するために、PowerApps 管理者センターにサインインします。 期限およびアップグレードに必要な手順の詳細については、[Common Data Service へのアップグレード](https://docs.microsoft.com/en-us/common-data-service/upgradecds/introduction-upgrade-cds) を参照してください。

## <a name="in-preview"></a>プレビュー

### <a name="allow-reason-codes-to-be-specified-on-leave-types"></a>理由コードを休暇タイプに指定できるようにする
組織は、休暇申請に関する追加情報が必要な場合があります。 休暇タイプに理由コードを指定し、従業員が休暇申請で理由コードを選択できるようになりました。

### <a name="require-reason-codes-for-certain-leave-types-on-time-off-requests"></a>休暇申請で特定の休暇タイプに理由コードが必要
従業員が休暇を送信するときに、組織は特定の休暇タイプに理由コードを要求することがあります。 これは、会社の方針または規制要件が原因である可能性があります。 どの休暇タイプに理由コードが必要かを指定できるようになりました。また、従業員に休暇申請で休暇タイプに理由コードを指定するように要求できます。

## <a name="coming-soon"></a>間もなく公開

### <a name="improvements-to-the-user-interface-for-duplicate-employee-check"></a>重複する従業員チェックのためのユーザー インターフェイスの改良
この変更により、名前のフィールドを入力すると重複が検出され、見つかった重複の数がステータスに表示されるようになります。 提供されたリンクを選択して新しいページを開き、検出された一致を使用するかどうかを評価できます。 データ入力の中断を回避するために、重複フォームは自動的に開きません。

###  <a name="email-support-for-alerts"></a>アラートの電子メールサポート
プラットフォーム更新プログラム 25 を使用すると、あるイベントによってトリガーされたときに、自動的に連絡先に電子メール通知を送信する警告ルールを作成できます。 
