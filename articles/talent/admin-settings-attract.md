---
title: "Attract での管理者設定"
description: "このトピックでは、Attract 内のユーザーおよび組織との機能を有効にする方法について説明します。"
author: 
manager: AnnBe
ms.date: 12/07/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.translationtype: HT
ms.sourcegitcommit: be66d9f95551066bb8bc25445c652d4fa59066d4
ms.openlocfilehash: fb7b5e5b98ddb8e0e44fccbb0ddbb05199265414
ms.contentlocale: ja-jp
ms.lasthandoff: 12/07/2018

---

# <a name="admin-settings-in-attract"></a>Attract での管理者設定
[!include[banner](../includes/banner.md)]

Microsoft Dynamics 365 for Talent の管理者センター: Attract には、構成設定、統合オプション、および Attract アプリケーションの設定オプションが含まれています。

## <a name="company-information"></a>会社情報

会社の表示名を入力し、会社のロゴを追加します。 表示名およびロゴは、新人研修エクスペリエンス中に人材募集を使用できます。

## <a name="linkedin-integration"></a>LinkedIn の統合

LinkedIn Recruiter System Connect (RSC) で統合を設定します。 LinkedIn の資格情報を使い、LinkedIn に接続した後は、応募者の LinkedIn プロファイル、アプリケーション、面接フィードバック、および雇用チームのメモを同期できます。 LinkedIn 採用担当者のフル ライセンスが必要です。 LinkedIn Recruiter の詳細については、[Recruiter System Connect (RSC) – よくある質問](https://www.linkedin.com/help/recruiter/answer/90483) を参照してください。

## <a name="user-permissions"></a>ユーザーのアクセス許可

組織内のユーザーにロールを割り当てます。 次のロールを使用できます: **管理者**、**採用担当者**、**採用マネージャー**、および**読み取り専用**。 ユーザーのアクセス許可の詳細は、[セキュリティおよび Attract のロール管理](./security-attract.md) を参照してください。

## <a name="feature-management"></a>機能の管理

新しい機能が追加され、パブリック プレビューでリリースされる可能性があります。 パブリック プレビューの機能は、すべてのサービス要件を満たしていません。 受信することで、外部システムとデータを共有することに合意します。 組織がリリースされた新しい機能を必要としないことを検索する場合があります。 パブリック プレビュー機能は、組織のニーズに応じてオンとオフにできます。

## <a name="template-management"></a>テンプレート管理

プロセス テンプレートには、ジョブの採用プロセスの一部として必要なすべての活動が含まれています。 組織は、すべてのチーム メンバーまたは採用プロセス テンプレートを作成する管理者のどちらかを許可できます。 チーム メンバーが独自の採用プロセス テンプレートの作成を許可するには、テンプレートの管理機能を有効にします。 プロセス テンプレートの詳細については、[Attract のプロセス テンプレート](./process-templates-attract.md) を参照してください。

## <a name="email-template-settings"></a>電子メール テンプレート設定

組織では、さまざまなシナリオの電子メール テンプレートを作成できます。 電子メール テンプレートに含める場合は、ヘッダーの画像を選択することができます。 選択したヘッダーは、すべての電子メール テンプレートに表示されます。 テンプレートのフッターでは、組織のプライバシーに関する声明と通信の使用条件にリンクを追加できます。 詳細については、[Attract の電子メール テンプレート](./email-templates.md) を参照してください。

## <a name="offer-process"></a>オファーのプロセス

ジョブ オファーの承認プロセスをコンフィギュレーションすることができます。 たとえば、候補者に送信する前に、オファーの提示を承認する必要があるかどうか指定することができます。 承認者がオファーの決定に関してコメントを残すように要求することも可能です。

2 つの承認ワークフローを使用できます: **並列**および**順次**。

- **並列** – 承認はすべての承認者へ同時に送信されます。
- **順次** – 承認は特定の順序で承認者へ送信されます。

候補エクスペリエンスに関連するオプションを設定することもできます。 たとえば、1 つのオプションでは、候補者が追加のディスカッションなしのオファーを拒否できるかどうかを指定できます。 **候補者に追加のディスカッションなしのオファーを拒否することを許可**オプションを**いいえ**に設定した場合、候補者は**オファーを辞退**ボタンを使用できます。 このオプションを**はい**に設定した場合、候補者は理由を選択してから**辞退する**を選び、オファーを辞退することができます。

オファーの有効期限を設定し適用することもできます。 **すべてのオファーの有効期限を要求する**オプションを**はい**と設定した場合、指定した時間数または日数の後にオファーの期限は切れます。

オファー管理の詳細については、[オファー管理の設定](./offer-setup.md) を参照してください。

