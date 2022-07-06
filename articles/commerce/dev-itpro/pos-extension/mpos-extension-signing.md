---
title: Modern POS (MSIX) 拡張機能パッケージへのコード署名
description: この記事では、Modern POS (MSIX) 拡張機能パッケージにコード署名する方法について説明します。
author: mugunthanm
ms.date: 10/21/2021
ms.topic: article
audience: Developer
ms.reviewer: tfehr
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 04-13-2020
ms.dyn365.ops.version: AX 10.0.18
ms.openlocfilehash: 87476d5b140a424f36cc5899e2409515ffe5151e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8882213"
---
# <a name="code-signing-a-modern-pos-msix-extension-package"></a>Modern POS (MSIX) 拡張機能パッケージへのコード署名

[!include [banner](../../../includes/banner.md)]

この記事では、Modern POS (MSIX) 拡張機能パッケージにコード署名する方法について説明します。 この記事は、Retail ソフトウェア開発キット (SDK) バージョン 10.0.18 以降に適用されます。

Modern POS 拡張機能の .appx ファイルはすべて、コード署名証明書によって署名する必要があります。 運用には信頼できる機関の証明書を使用することをお勧めします。 ユニバーサル Windows プラットフォーム (UWP) アプリの署名の詳細については、[パーッケージの署名用の証明書を作成する](/windows/uwp/packaging/create-certificate-package-signing)を参照してください。

Modern Pos JavaScript プロジェクト ファイルにコード署名証明書を含めるには、次の XML が示すように、.proj ファイルを編集し、証明書の署名用ノードを含める必要があります。

```XML
<PackageCertificateKeyFile Condition="Exists('.\MPOS_Extension_Certificate.pfx')">MPOS_Extension_Certificate.pfx</PackageCertificateKeyFile>
```
> [!WARNING]
> パスワードで保護された証明書は、Visual Studio 2017 ではサポートされていませんが、Azure 署名ツールを使用してビルド パイプラインでパスワードで保護された証明書を使用できます。 

開発目的用の自己署名証明書を使用する場合、証明書を信頼できるルート フォルダーに追加して、コンピュータで手動で信頼済にする必要があります。

ビルド自動化中に、セキュリティで保護された場所やタスクから証明書をダウンロードして、含めることもできます。

ユニバーサル Windows アプリ パッケージのコード署名の詳細については、次の記事を参照してください。

+ [ビルド ソリューションのビルド タスクの構成](/windows/uwp/packaging/auto-build-package-uwp-apps#configure-the-build-solution-build-task)
+ [パーッケージの署名用の証明書を作成する](/windows/msix/package/create-certificate-package-signing)

GitHub のサンプルは、ビルド中に自己署名のテスト証明書を生成します。 この証明書は、開発目的でのみ使用されます。 この開発証明書を生産アプリケーション拡張パッケージに使用しないのは、開発シナリオのブロックを解除する方法のみです。

> [!WARNING]
> テスト証明書を生成するために、GitHub に含まれているサンプル のスクリプトは、ドメイン アカウントでのみ機能します。 ドメイン アカウントを使用していない場合、ビルドは失敗します。 ドメイン以外のアカウントを実行している場合は、「PackageCertificateKeyFile」セクションに独自の証明書を生成または含める必要があります。

生成されたテスト証明書は、プロジェクトの中間出力ディレクトリで使用可能です。

- テスト証明書の既定の場所は、**bld\\x86\\Debug\\MPOS\_Extension\_Certificate.pfx** です。
- 開発マシンに拡張機能パッケージを正常にインストールするには、テスト証明書を **手動で信頼済にする必要** があります。

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
