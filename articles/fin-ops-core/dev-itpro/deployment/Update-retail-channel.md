---
title: Commerce Scale Unit (クラウド) への更新プログラムと拡張機能の適用
description: このトピックでは、クラウドでホストされているコマース チャネル コンポーネントへの更新プログラムと拡張機能を適用する方法について説明します。
author: AamirAllaq
manager: AnnBe
ms.date: 06/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.scope: Retail, Operations
ms.search.region: Global
ms.author: aamiral
ms.search.validFrom: 2018-4-30
ms.dyn365.ops.version: 8
ms.openlocfilehash: 712efb33ea2a96271cc1c0956480cda553e13807
ms.sourcegitcommit: be7e4378c8122c6e7cfc4e7991efbdffee45e006
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2020
ms.locfileid: "3426384"
---
# <a name="apply-updates-and-extensions-to-commerce-scale-unit-cloud"></a>Commerce Scale Unit (クラウド) への更新プログラムと拡張機能の適用

[!include[banner](../includes/banner.md)]

アプリケーション バージョン 8.1.2 以降でレベル 2 サンドボックスまたは運用環境を更新し、Commerce Scale Unit を初期化した場合は、チャネル コンポーネントも更新する必要があります。 このトピックでは、Commerce Scale Unit に更新と拡張を適用する方法について説明します。

Commerce Scale Unit の更新プログラムは累積的なものです。 つまり、適用する更新すべてに、以前のリリースされたすべての変更がが含まれます。 配置可能なコマースの拡張用パッケージを適用することも累積的なプロセスであり、以前に配置された拡張機能のバージョンが置き換えられます。

## <a name="prerequisites"></a>必要条件

続行する前に、まず更新および拡張機能 (該当する場合) を環境に適用する必要があります。 詳細については、[クラウド環境への更新プログラムの適用](apply-deployable-package-system.md)を参照してください。

Commerce Scale Unit を更新するには、それぞれについて次の手順を実行します。

1. **環境の詳細**ページで、**環境機能 > Retail およびコマース**に移動します。
2. **コマース配置設定**ページで、**更新**を選択します。
3. 選択パネルで、更新先のバージョンを選択します。
4. 最新のサービス更新プログラムを適用して最新の機能にアクセスすることも、最新の品質更新プログラムに更新して、現在展開されているサービス更新プログラムの品質改善を適用することもできます。 詳細については、[Lifecycle Services (LCS) から更新プログラムをダウンロード](../migration-upgrade/download-hotfix-lcs.md) を参照してください。
5. また、同時に拡張機能を適用することもできます。 

Commerce Scale Unit に拡張機能を適用するには、次の手順を実行します。

1. **コマース配置設定**ページで、**拡張機能の適用**を選択します。
2. 選択パネルで、適用する拡張機能を選択します。

> [!NOTE]
> まず、Lifecycle Services (LCS) で Commerce の配置可能なパッケージをプロジェクト資産ライブラリにアップロードしてください。すると、LCS の **Commerce の配置設定ページ**でパッケージの配置を選択できるようになります。

**更新の適用**と**拡張機能の適用**の両方の操作には、最大 1 時間のダウンタイムが必要です。 この時間中、次のことが発生します。

- クラウドでホストされている Commerce チャネルは機能しません (POS オフライン機能が有効な場合を除く)。
- オフライン機能が有効になっている POS デバイスの機能が制限されます。
- Commerce Scale Unit に依存しているすべてのE コマース クライアントが中断されます。
- Commerce Scale Units でホストされているチャネルは影響を受けません。
- 本社機能も影響を受けません。

> [!NOTE]
> 拡張機能と更新プログラムを同時に適用するには、1 回のダウンタイムが必要なため、複数のダウンタイムを避ける効果的な方法です。

## <a name="view-history"></a>履歴の表示
最新の操作履歴をスケールユニットで表示するには、**アクション** タブの **履歴** を選択し、**スケール ユニットの履歴**ページを開きます。 このページでは、初期化、サービス更新、品質更新、バージョン、拡張機能の詳細、その他の関連情報など、最近の操作を表示できます。

