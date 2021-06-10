---
title: Modern POS (MSIX) 拡張機能パッケージへのコード署名
description: このトピックでは、Modern POS (MSIX) 拡張パッケージにコード署名する方法について説明します。
author: mugunthanm
ms.date: 04/13/2021
ms.topic: article
audience: Developer
ms.reviewer: rhaertle
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 04-13-2020
ms.dyn365.ops.version: AX 10.0.18
ms.openlocfilehash: 56368ca06778dbe7f656befe1f715a15a876f825
ms.sourcegitcommit: d84329f903d359ae042e8c0a4594982a7e06756f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/06/2021
ms.locfileid: "5984297"
---
# <a name="code-signing-a-modern-pos-msix-extension-package"></a>Modern POS (MSIX) 拡張機能パッケージへのコード署名

[!include [banner](../../../includes/banner.md)]

このトピックでは、Modern POS (MSIX) 拡張パッケージにコード署名する方法について説明します。 このトピックは、Retail SDK バージョン 10.0.18 以降に適用されます。

MPOS 拡張子の .appx ファイルはすべて、コード署名証明書によって署名する必要があります。 運用には信頼済みの機関の証明書を使用することをお勧めします。 ユニバーサル Windows プラットフォーム (UWP) アプリの署名の詳細については、[パーッケージの署名用の証明書を作成する](https://docs.microsoft.com/windows/uwp/packaging/create-certificate-package-signing)を参照してください。

ModernPos JavaScript プロジェクト ファイルに署名する証明書を含めるには、.proj ファイルを編集し、証明書の署名用のノードを含める必要があります。

```XML
<PackageCertificateKeyFile Condition="Exists('.\MPOS_Extension_Certificate.pfx')">MPOS_Extension_Certificate.pfx</PackageCertificateKeyFile>
```

開発目的用の自己署名証明書を使用する場合、証明書を信頼されたルート フォルダーに追加して、そのコンピュータで手動で信頼する必要があります。

ビルド自動化中に、セキュリティで保護された場所やセキュリティで保護されたタスクから証明書をダウンロードして、含めることもできます。

ユニバーサル Windows プラットフォーム パッケージのコード署名に関する詳細については、次のリンクを参照してください。

+ [ビルド ソリューションのビルド タスクの構成](https://docs.microsoft.com/windows/uwp/packaging/auto-build-package-uwp-apps#configure-the-build-solution-build-task)
+ [パーッケージの署名用の証明書を作成する](https://docs.microsoft.com/windows/msix/package/create-certificate-package-signing)

GitHub のサンプルは、ビルド中に開発目的でのみ使用できる自己署名のテスト証明書を生成します。 この証明書は、開発シナリオのブロックを解除する場合にのみ使用可能です。

> [!WARNING]
> この開発証明書を運用アプリの拡張パッケージに使用することはできません。

生成されたテスト証明書は、プロジェクトの中間出力ディレクトリで使用可能です。

- 既定では、場所は `bld\x86\Debug\MPOS_Extension_Certificate.pfx` です。
- 開発マシンに拡張機能パッケージを正常にインストールするには、生成されたテスト証明書を手動で信頼する必要があります。

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
