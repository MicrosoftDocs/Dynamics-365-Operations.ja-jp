---
title: "Microsoft Dynamics 365 翻訳サービス - ユーザー インターフェイス ファイルの翻訳"
description: "このトピックでは、Microsoft Dynamics 365 製品における UI 翻訳サービスの使用方法について説明します。"
author: kfend
manager: AnnBe
ms.date: 03/29/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Operations
ms.custom: 6154
ms.assetid: 
ms.search.region: Global
ms.author: ejchoGIT
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 879eb9f2a63a8514791f74965005ed3e22bc0de7
ms.openlocfilehash: 2977f6f578c86eed3d775d79860d83d9c3890138
ms.contentlocale: ja-jp
ms.lasthandoff: 04/20/2018

---

# <a name="microsoft-dynamics-365-translation-service---user-interface-file-translation"></a>Microsoft Dynamics 365 翻訳サービス - ユーザー インターフェイス ファイルの翻訳

[!include [banner](../includes/banner.md)]

このトピックでは、Microsoft Dynamics 製品またはソリューションのユーザー インターフェイス (UI) ファイルを変換する方法について説明します。

Microsoft Dynamics 365 翻訳サービスに関する詳細については、[Dynamics 365 - 翻訳サービスの概要](translation-service-overview.md) を参照してください。 ドキュメント ファイルを翻訳する方法については、[Dynamics 365 - 翻訳サービス ユーザー ガイド - ドキュメント ファイルの翻訳](use-translation-service-ua.md) を参照してください。

## <a name="create-a-translation-request"></a>翻訳要求を作成する
1. Microsoft Dynamics Lifecycle Services (LCS) で、DTS ダッシュボードの**追加**を選択して新しい翻訳要求を作成します。

    ![追加ボタン](./media/dts-request1.png "追加ボタン")

    LCS ホーム ページから、またはプロジェクト内から、DTS ダッシュ ボードを開くことができます。 詳細については、[DTS にアクセス](./translation-service-overview.md#accessing-dts) を参照してください。

2. 要求ための必要な情報を入力します。

    | フィールド | 説明 |
    |-------|-------------|
    | 要求名 | 要求名を入力します。 |
    | ファイル タイプ | **ユーザー インターフェイス** を選択します。 |
    | 製品名 | 製品名を選択します。 LCS プロジェクト内から DTS にアクセスする場合、このフィールドは自動的に入力され、読み取り専用です。 |
    | 製品バージョン | 製品バージョンを選択します。 LCS プロジェクト内から DTS にアクセスする場合、このフィールドではプロジェクトからの既定の製品バージョン情報を表示されます。 ただし、別のバージョンを選択できます。 |
    | ターゲットの国/地域 | 翻訳したファイルをリリースする国または地域を選択します。 |
    | 翻訳元言語、翻訳先言語 | 翻訳対象の言語の組み合わせを選択します。 このフィールドには、選択した製品名とバージョンでサポートされているすべての言語がサポートされています。 **太字**タイプで表示される言語名は、Microsoft Dynamics の製品の一般提供 (GA) 言語です。 したがって、Microsoft で訓練された機械翻訳 (MT) システムは、これらの言語で使用できます。 つまり、MT システムは Microsoft Dynamics の用語でトレーニングされます。 GA 言語以外の場合、MT システムは一般的なドメイン トレーニングを使用します。 |

    > [!NOTE]
    > Microsoft のトレーニングを受けた Microsoft Dynamics 言語資産の MT システムを利用するには、ソース言語またはターゲット言語として **English – United States** を選択する必要があります。 次に例を示します。
    >
    > | 翻訳のソース言語 | 翻訳のターゲット言語 | 使用される MT システム |
    > |-----------------------------|-----------------------------|------------------------|
    > | 英語 – 米国 | 日本語 | Microsoft によるトレーニングされた MT システム |
    > | 日本語 | 英語 – 米国 | Microsoft によるトレーニングされた MT システム |
    > | ドイツ語 | 日本語 | 一般的な MT システムには、ユーザーが XML ローカライズ交換ファイル形式 (XLIFF) を使用する翻訳メモリ (TM) を提供しない限り、10,000 を超える翻訳単位 (TU) があります。 |

3. **作成** を選択します。

## <a name="upload-files"></a>ファイルのアップロード
各セクションでプラス記号 (**+**) を選択し、**ファイルのアップロード** ページを開きます。

### <a name="upload-the-files-to-translate-required"></a>翻訳するファイルをアップロードする (必須)
変換するすべての UI ファイルを含むひとつの ZIP ファイルを作成します。 ファイル タイプが製品でサポートされている場合、zip ファイルに異なるファイル タイプを含めることができます。 サポートされるファイル タイプの詳細については、[サポートされている製品](translation-service-overview.md#supported-products) を参照してください。 DTS はアップロードするソース ファイルを変更しないことに注意してください。 ソースファイルは、対応するターゲット言語でファイルを作成するために使用されます。

### <a name="upload-xliff-translation-memory-files-optional"></a>XLIFF 翻訳メモリファイル (オプション) のアップロード
以前の UI 翻訳要求の XLIFF TM ファイルがある場合、または[整列ツール](use-translation-service-tm.md)を使用し、XLIFF TM を作成した場合、それらをアップロードする前にファイルを zip できます。 その後、製品バージョン間の整合性を保証するために一致する文字列が再利用されます。 XLIFF TM の詳細については、[Microsoft Dynamics 365 翻訳サービス - 翻訳メモリ](use-translation-service-tm.md) を参照してください。

再利用のために XLIFF TM を使用することに加えて、DTS はソース言語またはターゲット言語のいずれかが Microsoft GA 言語である場合やその他の言語が**英語 - 米国**である場合にそれらを使用してカスタム [MT システム](translation-service-overview.md#custom-trained-mt-system)を作成します。 ただし、ソース言語もターゲット言語も Microsoft GA 言語でない場合、および XLIFF TM に 10,000 未満の TU が含まれている場合は、リサイクルの完了後に DTS は一般的なドメイン MT システムを使用します。 この動作は、Microsoft Translator ハブ (MTハブ) によって設定されている要件が原因で発生します。

ファイルのアップロードが終了したら、**送信**を選択して翻訳プロセスを開始します。 要求を送信すると、新しい要求 ID が DTS ダッシュ ボードに作成されます。 要求 ID を選択し、要求の詳細ページで **依頼状況** タブを選択して、依頼の概要とそのステータスを表示します。

![ステータス タブの要求](./media/dts-request-status.png "ステータス タブの要求")

処理時間は、DTS キューに入っている要求の数と、送信するソース ファイルの文字数に依存することに注意してください。

+ XLIFF TM のない UI 翻訳要求は、ファイル サイズに応じて数分で完了できます。
+ UI 翻訳リクエストに XLIFF TM がある場合、必要な時間は、MT システムの種類によって異なります。

    + カスタム MT システムの作成には、2 ~ 3日必要です。
    + 一般的な MT システムを使用している場合、ファイル サイズに応じて要求を数分で実行することができます。

## <a name="after-translation-is-completed"></a>翻訳の完了後
翻訳要求の処理が完了すると、DTS から電子メール通知を受信します。 結果を要求詳細ページの **要求の出力** タブ上に表示することができます。

![出力タブの要求](./media/dts-output.png "出力タブの要求")

UI 翻訳の要求では、翻訳プロセスが完了した後、出力ファイルの 2 つのタイプが使用できます。

+ **翻訳レビュー対象ファイル** – XLIFF ファイルをダウンロードしてレビューし、必要に応じて翻訳を編集します。 ファイルには、ソースとターゲットの言語が並べて表示されます。
+ **ソース形式で翻訳されたファイル** – 翻訳を編集または確認する予定がない場合は、このファイルをダウンロードしてください。 *ネイティブ形式*とは、そのファイルが送信したソースファイルと同じ形式であることを意味します。

### <a name="review-and-edit-the-translations-in-the-xliff-file"></a>XLIFF ファイル内の翻訳を確認し、編集
DTS が提供する XLIFF ファイル内の翻訳をレビューおよび編集して、翻訳出力が製品の品質基準を満たしていることを確認することをお勧めします。 XLIFF ファイルを編集する方法の詳細については、[XLIFF 翻訳メモリの編集](use-translation-service-tm.md#editing-an-xliff-translation-memory) を参照してください。

### <a name="regenerate-output-files"></a>出力ファイルの再生成
翻訳ファイルのレビューと編集が完了したら、出力ファイルをソース ファイル形式で再生成する必要があります。 最新の翻訳 (つまり、ユーザーが編集したバージョンの翻訳) をターゲット言語で UI ファイルに適用することができます。

1. **要求の出力**タブで、**再生成**を選択します。 **再生成 (パートナーによる)** という名前の新しいタブが表示されます。
2. プラス記号 (**+**) を選択し、**ファイルのアップロード** ページを開きます。
3. 編集後の XLIFF ファイルを zip 圧縮してから、**アップロード** を選択します。 **要求の出力**タブの XLIFF ファイルに DTS が提供した名前を変更しないでください。DTS がソース形式で再生成する更新済の出力ファイルは、**要求の出力**タブで提供されているのと同じファイル名を使用します。
4. アップロード アクションを確認するように求められます。 DTS は新しい出力ファイルを **再生成 (パートナーによる)** タブ上に再生成することができます。

![再生成された出力](./media/dts-regenerate-output.png "再生成された出力")

必要に応じて何度でも再生成プロセスを繰り返すことができます。

