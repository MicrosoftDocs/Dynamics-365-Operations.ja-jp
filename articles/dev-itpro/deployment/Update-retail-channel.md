---
title: "クラウドでホストされている Retail チャネル コンポーネントへの更新プログラムと拡張機能の適用"
description: "このトピックでは、クラウドでホストされている Retail チャネル コンポーネントへの更新プログラムと拡張機能を適用する方法について説明します。"
author: AamirAllaq
manager: AnnBe
ms.date: 12/11/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: IT Pro
ms.reviewer: sericks
ms.search.scope: Retail, Operations
ms.search.region: Global
ms.author: aamiral
ms.search.validFrom: 2018-4-30
ms.dyn365.ops.version: 8
ms.translationtype: HT
ms.sourcegitcommit: d4e5d20d7f632a074cffdbe57e6a31140adf17c5
ms.openlocfilehash: 33a75b82197ce5c7df78fc918fd33d2678ef75bb
ms.contentlocale: ja-jp
ms.lasthandoff: 12/11/2018

---


# <a name="apply-updates-and-extensions-to-cloud-hosted-retail-channel-components"></a>クラウドでホストされている Retail チャネル コンポーネントへの更新プログラムと拡張機能の適用

[!include[banner](../includes/banner.md)]

アプリケーション バージョン 8.1.2 以降でレベル 2 サンドボックスまたは運用環境を更新し、クラウドで Retail チャンル コンポーネントの短縮ダウンタイム更新を有効にした場合は、Retail チャネル コンポーネントも更新する必要があります。 このトピックでは、クラウドでホストされている Retail チャネル コンポーネントへの更新プログラムと拡張機能を適用する方法について説明します。

Retail チャネル コンポーネントの更新は累積的です。 つまり、適用する更新すべてに、以前のリリースされたすべての変更がが含まれます。 Retail の配置可能パッケージを適用することも累積的なプロセスであり、拡張機能の以前に配置されたバージョンが置き換えられます。

## <a name="prerequisites"></a>必要条件

続行する前に、まず更新および拡張機能 (該当する場合) を環境に適用する必要があります。 詳細については、[クラウド環境への更新プログラムの適用](apply-deployable-package-system.md)を参照してください。

クラウドでホストされている Retail チャネル コンポーネントを更新するには、以下を行います。

1. **環境の詳細** ページで、**環境機能 > Retail** に移動します。
2. **Retail 配置設定** ページで、**更新** を選択します。
3. 選択パネルで、更新先のバージョンを選択します。
4. 同時に、拡張機能を適用することもできます。 

クラウドでホストされている Retail チャネルに拡張機能を適用するには、次の操作を行います。

1. **Retail 配置設定** ページで、**拡張機能の適用** を選択します。
2. 選択パネルで、適用する拡張機能を選択します。

> [!NOTE]
> LCS の **Retail の配置設定ページ** で配置を選択する前に、まず、Lifecycle Services (LCS) で Retail の配置可能なパッケージをプロジェクト資産ライブラリにアップロードする必要があります。

更新適用と拡張機能適用の両方の操作には、最大 1 時間のダウンタイムが必要です。 この時間中、次のことが発生します。

- クラウドでホストされている Retail チャンネルは機能しません (POS オフライン機能が有効な場合を除く)。
- オフライン機能が有効になっている POS デバイスの機能が制限されます。
- Retail サーバーに依存しているすべての電子商取引クライアントが中断されます。
- Retail Store Scale Unit でホストされているチャネルも影響を受けません。
- 本社機能も影響を受けません。

> [!NOTE]
> 拡張機能と更新プログラムを同時に適用するには、1 回のダウンタイムが必要なため、複数のダウンタイムを避ける効果的な方法です。

