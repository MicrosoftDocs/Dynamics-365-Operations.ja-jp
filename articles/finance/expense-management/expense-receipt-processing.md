---
title: 経費の領収書
description: このトピックでは、領収書の光学式文字認識 (OCR) 処理に関する情報を提供します。 この機能は、Microsoft Dynamics 365 Finance で経費精算書を作成する際のユーザー エクスペリエンスの向上を目的に設計されています。
author: stevensporen
manager: AnnBe
ms.date: 11/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: stsporen
ms.search.validFrom: 2019-11-20
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 1ead9039de63e2cf4f3a7faddd1702b9614d7f99
ms.sourcegitcommit: 6aceca43c53c4dde46954c0b6b855d488eb44ed2
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/05/2020
ms.locfileid: "3027906"
---
# <a name="public-preview-expense-receipt-processing"></a>パブリックプレビュー: 経費レシートの処理

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]


領収書の光学式文字認識 (OCR) 処理の導入により、経費入力が強化されました。 この機能は、経費精算書を作成する際のユーザー エクスペリエンスの向上を目的に設計されています。

## <a name="key-features"></a>主な機能

- 領収書から販売者名、日付、合計金額を抽出する。
- この機能は、未添付の領収書を未添付の経費トランザクションと照合します。
- ユーザーは、領収書から手動で入力された経費トランザクションを作成できます。

## <a name="usage-examples"></a>使用例

- **経費精算書の作成時に、クレジット カード トランザクションを含む領収書を自動的に添付します。**

    1. **経費管理**ワークスペースを開きます。
    2. **領収書**タブで、未添付の領収書が存在することを確認します。 **領収書**タブで領収書をアップロードすることもできます。
    3. **経費**タブで、未添付の経費が存在することを確認します。 通常、経費管理者は、これらの経費をクレジット カード プロバイダーからインポートします。
    4. **新しい経費精算書**を選択します。 経費精算書を作成するときに、経費、および領収書を含めることができるようになりました。 経費と領収書の両方を追加すると、経費に対する領収書の自動照合がトリガーされます。

- **経費を作成するか、領収書から経費を照合します。**

    1. 経費精算書の**領収書**タブで、**領収書の追加**を選択して領収書を添付します。
    2. アップロードされた領収書の画像の下に**作成**および**照合**オプションが表示されます。

        - **作成**を選択して、手動で入力された経費トランザクションを作成し、領収書から抽出された値を入力します。
        - **照合**を選択した場合、システムは既存の経費と領収書を照合しようとします。

## <a name="installation"></a>インストール

この機能は、**経費精算書の再設計**機能と組み合わせて機能し、経費のエクスペリエンスを簡略化することができます。

これらの高度な経費機能を使用するには、Microsoft Dynamics 365 Finance の経費管理サービス アドインをインストールし、インスタンスの機能を有効にします。 Microsoft Dynamics Lifecycle Services (LCS) のプロジェクトからアドインにアクセスできます。

1. LCS にサインインし、目的の環境を開きます。
2. **完全な詳細**に移動します。
3. **メンテナンス**を選択するか、**環境アドイン** クイック タブまで下にスクロールします。
4. **新しいアドインのインストール**を選択します。
5. **経費管理サービス**を選択します。
6. インストール ガイドに従って、契約条件に同意します。
7. **インストール**を選択します。

**機能の管理**ワークスペースで、次の機能を有効にします。

- 経費レポートの再設計
- レシートからの自動照合および経費の作成

これらの機能をオンにすると、次のアクションが実行されます。

- 既存の**経費管理**ワークスペースは、新しいワークスペースに置き換えられます。
- 経費フィールド表示の新しいメニュー項目が追加されます。
- 以前の**経費精算書**ページは、**経費管理 > 自分の経費 > 経費精算書**に移動して開くことができます。
- ワークフローと承認を行っても、既存の経費精算書ページに移動します。
- 領収書は、Microsoft Azure Cognitive Services によって処理され、メタデータが抽出されて追加されます。
- 一致する未添付の領収書を含む経費精算書を作成できるオプションが追加されました。
- 経費精算書に追加されたオプションを使用すると、領収書から経費明細行を作成したり、既存の領収書を既存の経費明細行と一致させたりすることができます。

再設計された経費精算書の詳細については、[経費精算書の再設計](ExpenseWorkspaceNew.md) を参照してください。

## <a name="frequently-asked-questions"></a>よく寄せられる質問

**Microsoft は、モデルにデータを使用しますか ?**

いいえ、Microsoft は、領収書処理サービス用の一般的な機械学習モデルを構築しています。 このモデルは、アップロードした領収書に基づいていません。

**この機能はどこで使用および処理されますか ?**

現在、米国がサポートされています。

**領収書はどこに移動しますか ?**

財務では、Cognitive Services に連絡してフィールド データを抽出します。 Cognitive Services は、処理が行われている間、最大 24 時間領収書のコピーを保持します。 処理が完了すると、Cognitive Services で領収書が削除されます。 領収書は財務に保管されたままになります。

詳細については、[Form Recognizer の新機能を使用して領収書を理解する](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/) を参照してください。