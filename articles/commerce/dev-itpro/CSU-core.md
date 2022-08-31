---
title: Commerce Scale Unit (CSU) コアの概要
description: この記事では、Microsoft Dynamics 365 Commerce の Commerce Scale Unit (CSU) Core の概要を説明します。
author: josaw1
ms.date: 04/27/2022
ms.topic: article
audience: Developer
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2022-03-30
ms.dyn365.ops.version: AX 10.0.25
ms.openlocfilehash: b3a13ebc45510a9e81133664bd1ae2a93df5acaf
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9282195"
---
# <a name="introduction-to-commerce-scale-unit-csu-core"></a>Commerce Scale Unit (CSU) コアの概要

[!include [banner](../includes/banner.md)]

この記事では、Microsoft Dynamics 365 Commerce の Commerce Scale Unit (CSU) Core の概要を説明します。

CSU Core は、Dynamics 365 Commerce が提供する、ヘッドレス コマース エンジンをホストする次世代の高性能プラットフォームです。 CSU Core は、既存の CSU と同じ機能を提供しますが、ASP.NET Core と .NET Coreを使用するため、高度に最適化され、パフォーマンスも高くなっています。

## <a name="why-csu-core"></a>CSU Core を使用する理由

CSU Coreは、クロス プラットフォームで高性能なフレームワークである ASP.NET Core を使用して構築されています。

CSU Core には次のメリットがあります。

- 既存の Commerce Scale Unit よりもアプリケーション プログラミング インターフェイス (API) のパフォーマンスが向上しています。
- .NET Core で実行され、.NET バージョン 6 を使用します。
- コマース ソフトウェア開発キット (SDK)、.NET Standard 2.0、および Visual Studio 2022 を使用して作成された拡張機能と下位互換性があります。

## <a name="csu-core-release-plan"></a>CSU Core リリース計画

CSU Core は、Dynamics 365 Commerce バージョン 10.0.22 のリリース時に新しい配置に利用できます。 Commerce バージョン 10.0.22 のリリース時には、すべての新しい配置に既定で使用されます。 オンプレミスまたは CSU の自己ホスト インストーラーは、ASP.NET Core を使用して構築され .NET Core で実行されるものと同じ CSU Core プラットフォームを使用します。

## <a name="deploy-or-migrate-to-csu-core"></a>CSU Core へ配置または移行する

CSU Core は、高パフォーマンスのヘッドレス コマース API と .NET Core の利点を提供します。 Microsoft にホストされている CSU を CSU Core に移行する、または CSU Core の新しいインスタンスを配置するには、サポートされている .NET フレームワークを使用した拡張機能を構築するために、Dynamics 365 Commerce サポート チームに問い合わせてください。

### <a name="extensions"></a>拡張子

ヘッドレス コマースの拡張機能を作成する場合、NET Standard 2.0 をターゲット フレームワークとして使用して構築する必要があります。

#### <a name="validate-your-extension-compatibility-with-csu-core"></a>拡張機能の CSU Core との互換性を検証する

拡張機能テストを実行すると、その拡張機能が CSU コアと互換性があるかどうか検証を行うことができます。 テストを実行するには、次の例のように Retail Server URL を表す **\<MyRetailServerURL\>** を使用したクエリ パラメータ **healthcheck?testname=extensions** を Retail Server URL に追加します。

`https://<MyRetailServerURL>/healthcheck?testname=extensions`

テスト結果には、互換性があるおよび互換性がない拡張機能の状態を示す表が含まれます。

#### <a name="extension-target-framework"></a>拡張機能のターゲット フレームワーク

| 拡張機能コンポーネント | 拡張機能プロジェクトのターゲット フレームワーク | Commerce SDK |
|--- | --- | --- |
| ヘッドレス コマース API | NET Standard 2.0 | バージョン 10.0.23 、またはそれ以降 |
| Commerce Runtime (CRT) | NET Standard 2.0 | バージョン 10.0.23 、またはそれ以降 |

#### <a name="migrate-extensions-to-support-csu-core"></a>拡張機能を CSU Core に移行する

CSU Core で実行するには、Retail SDK を使用して構築された拡張機能は Commerce SDK に移行する必要があります。 CSU Core ランタイムは、ASP .NET Core および .NET Core を使用して構築されます。 したがって、従来の .NET Framework と Retail SDK パッケージを使用して作成された拡張機能は、CSU Core では実行されません。 詳細については、[Retail SDK 拡張機能を Commerce SDK に移行する](retail-sdk/migrate-commerce-sdk.md)を参照してください。
