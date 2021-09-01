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
ms.openlocfilehash: ba87dbf0dd31ad5bb3f1fe9968fcb9b23a8eeb46f7df893bc56897af549f56d2
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6753096"
---
# <a name="code-signing-a-modern-pos-msix-extension-package"></a>Modern POS (MSIX) 拡張機能パッケージへのコード署名

[!include [banner](../../../includes/banner.md)]

このトピックでは、Modern POS (MSIX) 拡張パッケージにコード署名する方法について説明します。 このトピックは、Retail ソフトウェア開発キット (SDK) バージョン 10.0.18 以降に適用されます。

Modern POS 拡張機能の .appx ファイルはすべて、コード署名証明書によって署名する必要があります。 運用には信頼できる機関の証明書を使用することをお勧めします。 ユニバーサル Windows プラットフォーム (UWP) アプリの署名の詳細については、[パーッケージの署名用の証明書を作成する](/windows/uwp/packaging/create-certificate-package-signing)を参照してください。

Modern Pos JavaScript プロジェクト ファイルにコード署名証明書を含めるには、次の XML が示すように、.proj ファイルを編集し、証明書の署名用ノードを含める必要があります。

```XML
<PackageCertificateKeyFile Condition="Exists('.\MPOS_Extension_Certificate.pfx')">MPOS_Extension_Certificate.pfx</PackageCertificateKeyFile>
```

開発目的用の自己署名証明書を使用する場合、証明書を信頼できるルート フォルダーに追加して、コンピュータで手動で信頼済にする必要があります。

ビルド自動化中に、セキュリティで保護された場所やタスクから証明書をダウンロードして、含めることもできます。

ユニバーサル Windows プラットフォーム アプリ パッケージのコード署名の詳細については、次のトピックを参照してください。

+ [ビルド ソリューションのビルド タスクの構成](/windows/uwp/packaging/auto-build-package-uwp-apps#configure-the-build-solution-build-task)
+ [パーッケージの署名用の証明書を作成する](/windows/msix/package/create-certificate-package-signing)

GitHub のサンプルは、ビルド中に自己署名のテスト証明書を生成します。 この証明書は、開発目的でのみ使用されます。 開発シナリオのブロックを解除する場合にのみ使用できます。

> [!WARNING]
> この開発証明書を運用アプリの拡張パッケージに使用することはできません。

生成されたテスト証明書は、プロジェクトの中間出力ディレクトリで使用可能です。

- テスト証明書の既定の場所は、**bld\\x86\\Debug\\MPOS\_Extension\_Certificate.pfx** です。
- 開発マシンに拡張機能パッケージを正常にインストールするには、テスト証明書を **手動で信頼済にする必要** があります。

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
