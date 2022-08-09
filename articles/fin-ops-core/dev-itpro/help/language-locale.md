---
title: 製品およびヘルプの言語およびロケール記述子
description: この記事では、財務と運用クライアントと、翻訳された Microsoft Help コンテンツを含む GitHub リポジトリの間の言語名をマップします。
author: edupont04
ms.topic: article
ms.date: 05/11/2020
audience: IT Pro
ms.reviewer: tfehr
ms.search.region: Global
ms.author: edupont
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: Operations
ms.openlocfilehash: 47077c1bc7d8f62dba53e023a34106151a3d0c31
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/29/2022
ms.locfileid: "9066875"
---
# <a name="language-and-locale-descriptors-in-the-product-and-in-help"></a>製品およびヘルプの言語およびロケール記述子

財務と運用アプリが使用するクライアントは、複数の言語とロケールをサポートします。 1 つ以上のロケールのカスタム ヘルプ コンテンツを製品内 **ヘルプ** ウィンドウに追加するには、次の条件が両方とも満たされていることを確認する必要があります:

- 各 HTML ファイルの **ms.locale** プロパティの値は、コンテンツのロケールと一致します。

    たとえば、ドイツ語 (ドイツ) コンテンツには **ms.locale: de-de** の設定が必要です。

- カスタム ヘルプ Web サイトでは、コンテンツはロケールと同じ名前のフォルダーにあります。

    たとえば、ドイツ語 (ドイツ) コンテンツは、**de-de** という名前のフォルダーにある必要があります。

詳細については、[カスタム ヘルプの概要](custom-help-overview.md) と [Azure にカスタム ヘルプを展開](walkthrough-help-azure.md) を参照してください。

## <a name="languages-and-descriptors"></a>言語と記述子

次の表は、財務と運用クライアントと、翻訳された Microsoft Help コンテンツを含む GitHub リポジトリ間の言語名をマップします。

| クライアントの言語/ロケール | 言語/地域名 | GitHub リポジトリの名前 |
|-------------------------------|----------------------|-------------------------|
| ar | アラビア語 (サウジアラビア) | [Dynamics-365-Operations.ar-sa](https://github.com/MicrosoftDocs/Dynamics-365-Operations.ar-sa) |
| ar-ae | アラビア語 (アラブ首長国連邦) | [Dynamics-365-Operations.ar-ae](https://github.com/MicrosoftDocs/Dynamics-365-Operations.ar-sa) |
| cs | チェコ語 | [Dynamics-365-Operations.cs-cz](https://github.com/MicrosoftDocs/Dynamics-365-Operations.cs-cz) |
| da | デンマーク語 | [Dynamics-365-Operations.da-dk](https://github.com/MicrosoftDocs/Dynamics-365-Operations.da-dk/) |
| de | ドイツ語 (ドイツ) | [Dynamics-365-Operations.de-de](https://github.com/MicrosoftDocs/Dynamics-365-Operations.de-de) |
| de-at | ドイツ語 (オーストリア) | [Dynamics-365-Operations.de-de](https://github.com/MicrosoftDocs/Dynamics-365-Operations.de-de) |
| de-ch | ドイツ語 (スイス) | [Dynamics-365-Operations.de-de](https://github.com/MicrosoftDocs/Dynamics-365-Operations.de-de) |
| en-au | 英語 (オーストラリア) | [Dynamics-365-Unified-Operations-Public](https://github.com/MicrosoftDocs/Dynamics-365-Unified-Operations-Public) |
| en-ca | 英語 (カナダ) | [Dynamics-365-Unified-Operations-Public](https://github.com/MicrosoftDocs/Dynamics-365-Unified-Operations-Public) |
| en-gb | 英語 (英国) | [Dynamics-365-Unified-Operations-Public](https://github.com/MicrosoftDocs/Dynamics-365-Unified-Operations-Public) |
| en-ie | 英語 (アイルランド) | [Dynamics-365-Unified-Operations-Public](https://github.com/MicrosoftDocs/Dynamics-365-Unified-Operations-Public) |
| en-in | 英語 (インド) | [Dynamics-365-Unified-Operations-Public](https://github.com/MicrosoftDocs/Dynamics-365-Unified-Operations-Public) |
| en-my | 英語 (マレーシア) | [Dynamics-365-Unified-Operations-Public](https://github.com/MicrosoftDocs/Dynamics-365-Unified-Operations-Public) |
| en-nz | 英語 (ニュージーランド) | [Dynamics-365-Unified-Operations-Public](https://github.com/MicrosoftDocs/Dynamics-365-Unified-Operations-Public) |
| en-sg | 英語 (シンガポール) | [Dynamics-365-Unified-Operations-Public](https://github.com/MicrosoftDocs/Dynamics-365-Unified-Operations-Public) |
| ja-JP | 英語 (米国) | [Dynamics-365-Unified-Operations-Public](https://github.com/MicrosoftDocs/Dynamics-365-Unified-Operations-Public) |
| en-za | 英語 (南アフリカ) | [Dynamics-365-Unified-Operations-Public](https://github.com/MicrosoftDocs/Dynamics-365-Unified-Operations-Public) |
| es | スペイン語 (スペイン) | [Dynamics-365-Operations.es-es](https://github.com/MicrosoftDocs/Dynamics-365-Operations.es-es) |
| es-mx | スペイン語 (メキシコ) | [Dynamics-365-Operations.es-es](https://github.com/MicrosoftDocs/Dynamics-365-Operations.es-es) |
| et | エストニア語 | [Dynamics-365-Operations.et-ee](https://github.com/MicrosoftDocs/Dynamics-365-Operations.et-ee) |
| fi | フィンランド語 | [Dynamics-365-Operations.fi-fi](https://github.com/MicrosoftDocs/Dynamics-365-Operations.fi-fi) |
| fr | フランス語 (フランス) | [Dynamics-365-Operations.fr-fr](https://github.com/MicrosoftDocs/Dynamics-365-Operations.fr-fr) |
| fr-be | フランス語 (ベルギー) | [Dynamics-365-Operations.fr-fr](https://github.com/MicrosoftDocs/Dynamics-365-Operations.fr-fr) |
| fr-ca | フランス語 (カナダ) | [Dynamics-365-Operations.fr-fr](https://github.com/MicrosoftDocs/Dynamics-365-Operations.fr-fr) |
| fr-ch | フランス語 (スイス) | [Dynamics-365-Operations.fr-fr](https://github.com/MicrosoftDocs/Dynamics-365-Operations.fr-fr) |
| hu | ハンガリー語 | [Dynamics-365-Operations.hu-hu](https://github.com/MicrosoftDocs/Dynamics-365-Operations.hu-hu) |
| 完全一致 | アイスランド語 | [Dynamics-365-Operations.is-is](https://github.com/MicrosoftDocs/Dynamics-365-Operations.is-is) |
| it | イタリア | [Dynamics-365-Operations.it-it](https://github.com/MicrosoftDocs/Dynamics-365-Operations.it-it) |
| it-ch | イタリア語 (スイス) | [Dynamics-365-Operations.it-it](https://github.com/MicrosoftDocs/Dynamics-365-Operations.it-it) |
| ja | 日本語 | [Dynamics-365-Operations.ja-jp](https://github.com/MicrosoftDocs/Dynamics-365-Operations.ja-jp) |
| lt | リトアニア語 | [Dynamics-365-Operations.lt-lt](https://github.com/MicrosoftDocs/Dynamics-365-Operations.lt-lt) |
| lv | ラトビア語 | [Dynamics-365-Operations.lv-lv](https://github.com/MicrosoftDocs/Dynamics-365-Operations.lv-lv) |
| nb-no | ノルウェー語ブークモール | [Dynamics-365-Operations.nb-no](https://github.com/MicrosoftDocs/Dynamics-365-Operations.nb-no) |
| nl | オランダ語 (オランダ) | [Dynamics-365-Operations.nl-nl](https://github.com/MicrosoftDocs/Dynamics-365-Operations.nl-nl) |
| nl-be | オランダ語 (ベルギー) | [Dynamics-365-Operations.nl-nl](https://github.com/MicrosoftDocs/Dynamics-365-Operations.nl-nl) |
| pl | ポーランド語 | [Dynamics-365-Operations.pl-pl](https://github.com/MicrosoftDocs/Dynamics-365-Operations.pl-pl) |
| pt-br | ポルトガル語 (ブラジル) | [Dynamics-365-Operations.pt-br](https://github.com/MicrosoftDocs/Dynamics-365-Operations.pt-br) |
| ru | ロシア語 | [Dynamics-365-Operations.ru-ru](https://github.com/MicrosoftDocs/Dynamics-365-Operations.ru-ru) |
| sv | スウェーデン語 | [Dynamics-365-Operations.sv-se](https://github.com/MicrosoftDocs/Dynamics-365-Operations.sv-se) |
| th | タイ語 | [Dynamics-365-Operations.th-th](https://github.com/MicrosoftDocs/Dynamics-365-Operations.th-th) |
| tr | トルコ語 | [Dynamics-365-Operations.tr-tr](https://github.com/MicrosoftDocs/Dynamics-365-Operations.tr-tr) |
| zh-hans | 中国語 | [Dynamics-365-Operations.zh-cn](https://github.com/MicrosoftDocs/Dynamics-365-Operations.zh-cn) |

## <a name="languages-translations-and-adaptations"></a>言語、翻訳、適応

Microsoft teams は、英語 (米国) でコンテンツを作成します。 その後、そのコンテンツは複数の言語に翻訳され、翻訳されたコンテンツは各言語の GitHub の公開リポジトリで利用可能になります。

翻訳の再利用を最大化するために、翻訳サービスは一部の言語を別の言語の派生として扱います。 たとえば、オーストリアのドイツ語とドイツのドイツ語は、非常に密接に関連していると見なされるため、相互の派生として扱われます。 したがって、Dynamics-365-Operations.de-de GitHub リポジトリのファイルを、ドイツ語 (ドイツ) コンテンツとドイツ語 (オーストリア) コンテンツの両方の出発点として使用できます。

製品内の **ヘルプ** ウィンドウを拡張する場合は 、関連するロケールのインデックスを割り当てる必要があります。 詳細については、[言語のフォールバックをカスタマイズする](connect-help-pane.md#customize-language-fallback) を参照してください。

## <a name="see-also"></a>参照

[カスタム ヘルプの概要](custom-help-overview.md)  
[カスタム ヘルプ ツールキット](custom-help-toolkit.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
