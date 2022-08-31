---
title: カスタム ヘルプ ツールキット - HtmlLocaleChanger ツール
description: この記事では、財務と運用アプリ用のカスタム ヘルプ ツールキットに含まれている HtmlLocaleChanger ツールについて説明します。
author: edupont04
ms.date: 05/11/2020
ms.topic: article
audience: IT Pro
ms.reviewer: josaw
ms.search.region: Global
ms.author: edupont
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: Operations
ms.openlocfilehash: 3b1f05f963b2ccad3ffc95a96f3792038a332653
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9284490"
---
# <a name="custom-help-toolkit-the-htmllocalechanger-tool"></a>カスタム ヘルプ ツールキット: HtmlLocaleChanger ツール

[!include [banner](../includes/banner.md)]

カスタム ヘルプ ツールキットには、[HtmlFromRepoGenerator ツール](custom-help-toolkit-HtmlFromRepoGenerator.md) ツールによって生成された HTML ファイルを処理できる **HtmlLocaleChanger** ツールが含まれています。

## <a name="use-the-htmllocalechanger-tool-to-align-locales"></a><a name="htmllocale"></a>HtmlLocaleChanger ツールを使用してロケールを調整する

**HtmlLocaleChanger** ツールは、**ms.locale** プロパティに新しい値を設定することにより、HTML ファイルを更新することができます。 たとえば、ドイツ語 (ドイツ) 用の HTML ファイルがあり、同じコンテンツをドイツ語 (オーストリア) で利用できるようにしたいとします。 この場合、ツールを実行して、設定を **ms.locale: de-de** から **ms.locale:de-at** に変更できます。

HtmlLocaleChanger.exe を実行するための構文は次のとおりです。

```
HtmlLocaleChanger.exe --h <path> --l <locale> --v <true|false>
```

パラメータの説明を以下に示します。

| パラメーター | 説明 |
|-----------|-------------|
| h | 処理する HTML ファイルのパスを指定します。 |
| l | HTML ファイルの新しいロケールを指定します。 |
| v | このパラメーターを **true** に設定し、詳細ログを有効にします。 それ以外の場合、**false** に設定します。 |

## <a name="example"></a>例

次の例では、ロケールを **de-at** に変更し、詳細ログを有効にします。

```
HtmlLocaleChanger.exe --h D:\D365-Operations\d365F-O\supply-chain\de --l de-at --v
```

## <a name="see-also"></a>参照

[カスタム ヘルプの概要](custom-help-overview.md)  
[Azure にカスタム ヘルプを展開](walkthrough-help-azure.md)  
[製品およびヘルプの言語およびロケール記述子](language-locale.md)  
[Dynamics AX カスタム ヘルプを Dynamics 365 で使用するために変換](migrate-dynamicsax2012.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
