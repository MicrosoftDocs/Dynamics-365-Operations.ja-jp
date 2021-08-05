---
title: 外部およびインライン スクリプト モジュール
description: このトピックでは、外部およびインライン スクリプト モジュールと、これらを Microsoft Dynamics 365 Commerce のテンプレートに追加する方法について説明します。
author: samjarawan
ms.date: 04/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: b56bc3fc26f0c5fefc5a04e77b28acae718057fe
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/06/2021
ms.locfileid: "6344970"
---
# <a name="external-and-inline-script-modules"></a>外部およびインライン スクリプト モジュール

[!include [banner](includes/banner.md)]

このトピックでは、外部およびインライン スクリプト モジュールと、これらを Microsoft Dynamics 365 Commerce のテンプレートに追加する方法について説明します。

外部およびインライン スクリプト モジュールを使用して、クライアント側の JavaScript スクリプトをサイト ページに追加できます。 スクリプトは、インラインの場合、または外部ファイルから呼び出す場合があります。 外部およびインライン スクリプト モジュールは、テンプレートの **HTML Head**、**本文の開始**、または **本文の終了** に追加できます。

次の図は、外部およびインライン スクリプト モジュールが、テンプレートでサポートされているさまざまなスロットに追加された例を示しています。

![テンプレートのさまざまなスロットのスクリプト モジュール。](media/script-modules-1.png)

## <a name="external-script-module-properties"></a>外部スクリプト モジュールのプロパティ

| プロパティ名 | 値 | 説明 |
|---------------|--------|-------------|
| スクリプト ソース | テキスト | スクリプト ファイルの場所の URL です。 |
| スクリプトの非同期実行 | **True** または **False** | このプロパティが **True** に設定されている場合、スクリプトは非同期で実行されます。 |
| スクリプト実行の延期 | **True** または **False** | このプロパティが **True** に設定されている場合、ページの実行が完了するとスクリプトが実行されます。 |

## <a name="inline-script-module-properties"></a>インライン スクリプト モジュールのプロパティ

| プロパティ名 | 値 | 説明 |
|---------------|--------|-------------|
| インライン スクリプト | テキスト | HTML ページの **\<script\>** タグにインラインがインサートされるスクリプト ステートメントのコレクション。 |

## <a name="content-security-policy"></a>コンテンツ セキュリティ ポリシー

コンテンツ セキュリティ ポリシー (CSP) が有効の場合、外部スクリプトが実行されない場合があります。 外部スクリプトを実行するには、最初にそれらのドメイン URL を Commerce サイト ビルダーの **script-src** CSP ディレクティブに追加する必要があります。 詳細については、[コンテンツ セキュリティ ポリシーの管理](manage-csp.md) を参照してください。

## <a name="add-a-script-module-to-a-template"></a>テンプレートへのスクリプト モジュールの追加

作業テンプレートにスクリプト モジュールを追加するには、次の手順に従います。

1. サイトのコマース サイト ビルダで、**テンプレート** を選択します。
1. テンプレートを選択し、**編集** を選択します。
1. **本文の開始** スロットで、省略記号ボタン (**...**) を選択し、**モジュールの追加** を選択します。

    ![新しいモジュールの追加。](media/script-modules-2.png)

1. **モジュールの追加** ダイアログ ボックスで、**外部スクリプト** モジュールまたは **インライン スクリプト** モジュールを選択し、**OK** を選択します。

    ![スクリプト モジュールの追加。](media/script-modules-3.png)

スクリプト モジュールを追加した後、次の図の例のようになります。 これでモジュールが構成され、テンプレートを保存および公開できます。

![追加された内部スクリプト モジュール。](media/script-modules-4.png)

## <a name="additional-resources"></a>追加リソース

[モジュール ライブラリの概要](starter-kit-overview.md)

[既定のページ モジュール](default-page-module.md)

[ページ集計モジュール](page-summary-module.md)

[メタタグ モジュール](metatags-module.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
